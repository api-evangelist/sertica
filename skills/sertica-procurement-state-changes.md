---
name: Change procurement state safely in SERTICA
description: Use SERTICA's can*/allow* precondition operations to test a purchase-order, requisition or invoice transition before performing it, and know which transitions can be taken back.
api: openapi/sertica-web-api-openapi.json
operations:
  - PurchaseOrderAllowCancelOrder
  - PurchaseOrderCancelOrder
  - RequisitionCanApproveForPurchase
  - RequisitionCanReject
  - RequisitionCancel
  - CanBeReversed
  - CreateReversal
  - CanBeApproved
  - CanBeRejected
  - RfqAllowSendToSupplier
  - CancelShipment
  - UndoReceiveWarehouseShipment
---

# Change procurement state safely in SERTICA

SERTICA's procurement chain runs Requisition → Request For Quote → Purchase Order →
Shipment → Invoice, with approval gates at nearly every step. These are consequential
writes: they send email to suppliers, commit spend, and move stock.

Authenticate first — see `sertica-authenticate.md`.

## Always ask before you act

SERTICA publishes 35 read-only **precondition** operations that answer whether a transition
is permitted for the current user, in the current state, right now. This is the closest
thing the API has to a dry run, and it is the single most useful safety affordance in the
contract. Call the probe, then act only on a positive answer.

| Probe | Guards |
|---|---|
| `PurchaseOrderAllowCancelOrder` — `GET /PurchaseOrders/{purchaseOrderNo}/allowCancelOrder` | `PurchaseOrderCancelOrder` |
| `AllowReceivePurchaseOrder` — `GET /PurchaseOrders/{purchaseOrderNo}/allowReceive` | receiving a PO |
| `AllowSendReminder` — `GET /PurchaseOrders/{purchaseOrderNo}/allowsendreminder` | sending a supplier reminder |
| `AllowPriceApproval` / `AllowForwardForPriceApproval` | price approval steps |
| `RequisitionCanApproveForPurchase` — `POST /Requisitions/{requisitionNo}/canapproveforpurchase` | approving for purchase |
| `RequisitionCanApproveForRfq` — `POST /Requisitions/{requisitionNo}/canapproveforrfq` | approving for RFQ |
| `RequisitionCanReject` — `POST /Requisitions/{requisitionNo}/canreject` | rejecting a requisition |
| `RfqAllowSendToSupplier` — `GET /RequestForQuotes/{requestForQuoteNo}/allowSendToSupplier` | `sendToSupplier` — sends real email |
| `CanBeApproved` / `CanBePreApproved` / `CanBeRejected` — `GET /ImInvoices/{invoiceNo}/…` | invoice approval steps |
| `CanBeReversed` — `GET /ImInvoices/{invoiceNo}/canBeReversed` | `CreateReversal` |

A probe tells you whether the call would be **allowed**. It does not simulate the result and
it does not tell you what would change.

## What can be taken back

| Action | Reversal | Window |
|---|---|---|
| Purchase order placed | `PurchaseOrderCancelOrder` — `POST /PurchaseOrders/{purchaseOrderNo}/cancelorder` | **not published** |
| Requisition raised | `RequisitionCancel` — `POST /Requisitions/{requisitionNo}/cancel` | **not published** |
| Invoice posted | `CreateReversal` — `POST /ImInvoices/{invoiceNo}/createReversal` | **not published** |
| Shipment sent | `CancelShipment` — `POST /Shipments/{shipmentNo}/cancel` | **not published** |
| Shipment received | `UndoReceiveWarehouseShipment` — `POST /Shipments/{shipmentNo}/unreceive` | **not published** |

SERTICA states no time limit for any of these. Do not tell a user a reversal will still be
possible later — the honest answer is that the API will tell you at the time, via the
matching probe, and not before.

Sending an RFQ to a supplier (`sendToSupplier`) and mailing a purchase order have **no**
reversal operation. Once the email leaves, the API cannot recall it. Treat those as
terminal and put a human in front of them.

## Retries

There is no idempotency key. If `PurchaseOrderCancelOrder` times out, do **not** re-send —
call `PurchaseOrderAllowCancelOrder` again and read the purchase order back to see what
state it landed in.

## Errors

`400` carries a `ValidationResult` naming the offending field; `403` names the missing user
right in its description; `500` is unhandled and is not something to retry.
