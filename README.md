# SERTICA

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SERTICA is a maritime fleet and ship management system from RINA (originally built by Logimatic in Denmark, first code written in 1989), used to run planned maintenance, procurement, HSQE, crewing, performance, logbooks and vessel reporting across a fleet. It is deployed as a per-customer site rather than a shared multi-tenant service, and it publishes a genuinely large machine-readable contract: the SERTICA Web API is an OpenAPI 3.0.4 document with 2,743 paths, 3,340 operations and 1,104 schemas, served publicly at https://docs.sertica.com/api/swagger/v1/swagger.json and browsable in a live Swagger UI. It is a REST/JSON API authenticated with a 24-hour JWT obtained by posting a SERTICA user login to /Auth, with authorization expressed as per-user SERTICA user rights rather than OAuth scopes. Beyond CRUD it carries the statutory maritime surface - MARPOL Oil, Garbage and Ballast Water electronic record books with signing and printout operations, SFI-coded components, ISM management-system documents, and PunchOut/ShipServ procurement integration.

**Areas:** Maritime · Shipping · Fleet Management · Maintenance · Procurement · Asset Management · Compliance · Enterprise Software

## SERTICA on APIs.io

Everything profiled for SERTICA is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/sertica/](https://apis.io/providers/sertica/)** — or go straight to one of the APIs or properties below.

### APIs (254)

- [SERTICA Accounting Dimensions API](https://apis.io/apis/sertica/sertica-accountingdimensions-api/) — The AccountingDimensions API from SERTICA — 12 operation(s) for accountingdimensions.
- [SERTICA Accounting Dimensions Cache API](https://apis.io/apis/sertica/sertica-accountingdimensionscache-api/) — The AccountingDimensionsCache API from SERTICA — 7 operation(s) for accountingdimensionscache.
- [SERTICA Accounts API](https://apis.io/apis/sertica/sertica-accounts-api/) — The Accounts API from SERTICA — 8 operation(s) for accounts.
- [SERTICA Activity Groups API](https://apis.io/apis/sertica/sertica-activitygroups-api/) — The ActivityGroups API from SERTICA — 8 operation(s) for activitygroups.
- [SERTICA Address Categories API](https://apis.io/apis/sertica/sertica-addresscategories-api/) — The AddressCategories API from SERTICA — 8 operation(s) for addresscategories.
- [SERTICA Address Classifications API](https://apis.io/apis/sertica/sertica-addressclassifications-api/) — The AddressClassifications API from SERTICA — 8 operation(s) for addressclassifications.
- [SERTICA Addresses API](https://apis.io/apis/sertica/sertica-addresses-api/) — The Addresses API from SERTICA — 25 operation(s) for addresses.
- [SERTICA AI Client API](https://apis.io/apis/sertica/sertica-aiclient-api/) — The AiClient API from SERTICA — 1 operation(s) for aiclient.
- [SERTICA Analytics API](https://apis.io/apis/sertica/sertica-analytics-api/) — The Analytics API from SERTICA — 19 operation(s) for analytics.
- [SERTICA Analytics Custom Menus API](https://apis.io/apis/sertica/sertica-analyticscustommenus-api/) — The AnalyticsCustomMenus API from SERTICA — 3 operation(s) for analyticscustommenus.
- [SERTICA Analytics Custom Templates API](https://apis.io/apis/sertica/sertica-analyticscustomtemplates-api/) — The AnalyticsCustomTemplates API from SERTICA — 12 operation(s) for analyticscustomtemplates.
- [SERTICA Analytics Excel Templates API](https://apis.io/apis/sertica/sertica-analyticsexceltemplates-api/) — The AnalyticsExcelTemplates API from SERTICA — 15 operation(s) for analyticsexceltemplates.
- [SERTICA Analytics Resources API](https://apis.io/apis/sertica/sertica-analyticsresources-api/) — The AnalyticsResources API from SERTICA — 6 operation(s) for analyticsresources.
- [SERTICA Analytics Subscriptions API](https://apis.io/apis/sertica/sertica-analyticssubscriptions-api/) — The AnalyticsSubscriptions API from SERTICA — 6 operation(s) for analyticssubscriptions.
- [SERTICA Analytics Template User Rights API](https://apis.io/apis/sertica/sertica-analyticstemplateuserrights-api/) — The AnalyticsTemplateUserRights API from SERTICA — 4 operation(s) for analyticstemplateuserrights.
- [SERTICA Analytics User Menus API](https://apis.io/apis/sertica/sertica-analyticsusermenus-api/) — The AnalyticsUserMenus API from SERTICA — 2 operation(s) for analyticsusermenus.
- [SERTICA Approval Setups API](https://apis.io/apis/sertica/sertica-approvalsetups-api/) — The ApprovalSetups API from SERTICA — 9 operation(s) for approvalsetups.
- [SERTICA Approval Web Excluded Units API](https://apis.io/apis/sertica/sertica-approvalwebexcludedunits-api/) — The ApprovalWebExcludedUnits API from SERTICA — 2 operation(s) for approvalwebexcludedunits.
- [SERTICA Auth API](https://apis.io/apis/sertica/sertica-auth-api/) — The Auth API from SERTICA — 16 operation(s) for auth.
- [SERTICA Available Grid Layouts API](https://apis.io/apis/sertica/sertica-availablegridlayouts-api/) — The AvailableGridLayouts API from SERTICA — 8 operation(s) for availablegridlayouts.
- [SERTICA Available Job List Web Search API](https://apis.io/apis/sertica/sertica-availablejoblistwebsearch-api/) — The AvailableJobListWebSearch API from SERTICA — 8 operation(s) for availablejoblistwebsearch.
- [SERTICA Brb Operations API](https://apis.io/apis/sertica/sertica-brboperations-api/) — The BrbOperations API from SERTICA — 18 operation(s) for brboperations.
- [SERTICA Brb Receivers API](https://apis.io/apis/sertica/sertica-brbreceivers-api/) — The BrbReceivers API from SERTICA — 10 operation(s) for brbreceivers.
- [SERTICA Budget Accrual Exports API](https://apis.io/apis/sertica/sertica-budgetaccrualexports-api/) — The BudgetAccrualExports API from SERTICA — 6 operation(s) for budgetaccrualexports.
- [SERTICA Budgets API](https://apis.io/apis/sertica/sertica-budgets-api/) — The Budgets API from SERTICA — 9 operation(s) for budgets.
- [SERTICA Calculate Purchase Order API](https://apis.io/apis/sertica/sertica-calculatepurchaseorder-api/) — The CalculatePurchaseOrder API from SERTICA — 5 operation(s) for calculatepurchaseorder.
- [SERTICA Carriers API](https://apis.io/apis/sertica/sertica-carriers-api/) — The Carriers API from SERTICA — 16 operation(s) for carriers.
- [SERTICA Certificate Documents API](https://apis.io/apis/sertica/sertica-certificatedocuments-api/) — The CertificateDocuments API from SERTICA — 11 operation(s) for certificatedocuments.
- [SERTICA Certificate Group Rules API](https://apis.io/apis/sertica/sertica-certificategrouprules-api/) — The CertificateGroupRules API from SERTICA — 8 operation(s) for certificategrouprules.
- [SERTICA Certificate Locations API](https://apis.io/apis/sertica/sertica-certificatelocations-api/) — The CertificateLocations API from SERTICA — 9 operation(s) for certificatelocations.
- [SERTICA Certificate Notification Settings API](https://apis.io/apis/sertica/sertica-certificatenotificationsettings-api/) — The CertificateNotificationSettings API from SERTICA — 9 operation(s) for certificatenotificationsettings.
- [SERTICA Certificates API](https://apis.io/apis/sertica/sertica-certificates-api/) — The Certificates API from SERTICA — 20 operation(s) for certificates.
- [SERTICA Certificate Tree API](https://apis.io/apis/sertica/sertica-certificatetree-api/) — The CertificateTree API from SERTICA — 2 operation(s) for certificatetree.
- [SERTICA Change Request Criticalities API](https://apis.io/apis/sertica/sertica-changerequestcriticalities-api/) — The ChangeRequestCriticalities API from SERTICA — 8 operation(s) for changerequestcriticalities.
- [SERTICA Change Request Documents API](https://apis.io/apis/sertica/sertica-changerequestdocuments-api/) — The ChangeRequestDocuments API from SERTICA — 13 operation(s) for changerequestdocuments.
- [SERTICA Change Request Sources API](https://apis.io/apis/sertica/sertica-changerequestsources-api/) — The ChangeRequestSources API from SERTICA — 8 operation(s) for changerequestsources.
- [SERTICA Class Codes API](https://apis.io/apis/sertica/sertica-classcodes-api/) — The ClassCodes API from SERTICA — 9 operation(s) for classcodes.
- [SERTICA Class Societies API](https://apis.io/apis/sertica/sertica-classsocieties-api/) — The ClassSocieties API from SERTICA — 8 operation(s) for classsocieties.
- [SERTICA Combined User Roles API](https://apis.io/apis/sertica/sertica-combineduserroles-api/) — The CombinedUserRoles API from SERTICA — 7 operation(s) for combineduserroles.
- [SERTICA Communication Languages API](https://apis.io/apis/sertica/sertica-communicationlanguages-api/) — The CommunicationLanguages API from SERTICA — 8 operation(s) for communicationlanguages.
- [SERTICA Companies API](https://apis.io/apis/sertica/sertica-companies-api/) — The Companies API from SERTICA — 15 operation(s) for companies.
- [SERTICA Component Locations API](https://apis.io/apis/sertica/sertica-componentlocations-api/) — The ComponentLocations API from SERTICA — 8 operation(s) for componentlocations.
- [SERTICA Component Maps API](https://apis.io/apis/sertica/sertica-componentmaps-api/) — The ComponentMaps API from SERTICA — 13 operation(s) for componentmaps.
- [SERTICA Component Photos API](https://apis.io/apis/sertica/sertica-componentphotos-api/) — The ComponentPhotos API from SERTICA — 15 operation(s) for componentphotos.
- [SERTICA Components API](https://apis.io/apis/sertica/sertica-components-api/) — The Components API from SERTICA — 40 operation(s) for components.
- [SERTICA Component Types API](https://apis.io/apis/sertica/sertica-componenttypes-api/) — The ComponentTypes API from SERTICA — 9 operation(s) for componenttypes.
- [SERTICA Controlled Copies API](https://apis.io/apis/sertica/sertica-controlledcopies-api/) — The ControlledCopies API from SERTICA — 11 operation(s) for controlledcopies.
- [SERTICA Controlled Copy Revision Documents API](https://apis.io/apis/sertica/sertica-controlledcopyrevisiondocuments-api/) — The ControlledCopyRevisionDocuments API from SERTICA — 13 operation(s) for controlledcopyrevisiondocuments.
- [SERTICA Counters API](https://apis.io/apis/sertica/sertica-counters-api/) — The Counters API from SERTICA — 15 operation(s) for counters.
- [SERTICA Counter Types API](https://apis.io/apis/sertica/sertica-countertypes-api/) — The CounterTypes API from SERTICA — 8 operation(s) for countertypes.
- [SERTICA Currencies API](https://apis.io/apis/sertica/sertica-currencies-api/) — The Currencies API from SERTICA — 9 operation(s) for currencies.
- [SERTICA Data Transactions API](https://apis.io/apis/sertica/sertica-datatransactions-api/) — The DataTransactions API from SERTICA — 6 operation(s) for datatransactions.
- [SERTICA Data Warehouse Analytics Templates API](https://apis.io/apis/sertica/sertica-datawarehouseanalyticstemplates-api/) — The DataWarehouseAnalyticsTemplates API from SERTICA — 14 operation(s) for datawarehouseanalyticstemplates.
- [SERTICA Data Warehouse Connections API](https://apis.io/apis/sertica/sertica-datawarehouseconnections-api/) — The DataWarehouseConnections API from SERTICA — 9 operation(s) for datawarehouseconnections.
- [SERTICA Delivery Conditions API](https://apis.io/apis/sertica/sertica-deliveryconditions-api/) — The DeliveryConditions API from SERTICA — 8 operation(s) for deliveryconditions.
- [SERTICA Delivery Costs API](https://apis.io/apis/sertica/sertica-deliverycosts-api/) — The DeliveryCosts API from SERTICA — 8 operation(s) for deliverycosts.
- [SERTICA Departments API](https://apis.io/apis/sertica/sertica-departments-api/) — The Departments API from SERTICA — 8 operation(s) for departments.
- [SERTICA Destinations API](https://apis.io/apis/sertica/sertica-destinations-api/) — The Destinations API from SERTICA — 8 operation(s) for destinations.
- [SERTICA Device API](https://apis.io/apis/sertica/sertica-device-api/) — The Device API from SERTICA — 1 operation(s) for device.
- [SERTICA Document Classes API](https://apis.io/apis/sertica/sertica-documentclasses-api/) — The DocumentClasses API from SERTICA — 8 operation(s) for documentclasses.
- [SERTICA Document Mail Templates API](https://apis.io/apis/sertica/sertica-documentmailtemplates-api/) — The DocumentMailTemplates API from SERTICA — 8 operation(s) for documentmailtemplates.
- [SERTICA Documents API](https://apis.io/apis/sertica/sertica-documents-api/) — The Documents API from SERTICA — 28 operation(s) for documents.
- [SERTICA Document Transactions API](https://apis.io/apis/sertica/sertica-documenttransactions-api/) — The DocumentTransactions API from SERTICA — 5 operation(s) for documenttransactions.
- [SERTICA Document Tree API](https://apis.io/apis/sertica/sertica-documenttree-api/) — The DocumentTree API from SERTICA — 3 operation(s) for documenttree.
- [SERTICA Document Weblinks API](https://apis.io/apis/sertica/sertica-documentweblinks-api/) — The DocumentWeblinks API from SERTICA — 3 operation(s) for documentweblinks.
- [SERTICA Electronic Logbook API](https://apis.io/apis/sertica/sertica-electroniclogbook-api/) — The ElectronicLogbook API from SERTICA — 1 operation(s) for electroniclogbook.
- [SERTICA Embarkations API](https://apis.io/apis/sertica/sertica-embarkations-api/) — The Embarkations API from SERTICA — 9 operation(s) for embarkations.
- [SERTICA Environmental Items API](https://apis.io/apis/sertica/sertica-environmentalitems-api/) — The EnvironmentalItems API from SERTICA — 11 operation(s) for environmentalitems.
- [SERTICA Equipments API](https://apis.io/apis/sertica/sertica-equipments-api/) — The Equipments API from SERTICA — 9 operation(s) for equipments.
- [SERTICA Evaluation Answers API](https://apis.io/apis/sertica/sertica-evaluationanswers-api/) — The EvaluationAnswers API from SERTICA — 9 operation(s) for evaluationanswers.
- [SERTICA Evaluation Question Object Links API](https://apis.io/apis/sertica/sertica-evaluationquestionobjectlinks-api/) — The EvaluationQuestionObjectLinks API from SERTICA — 22 operation(s) for evaluationquestionobjectlinks.
- [SERTICA Evaluation Questions API](https://apis.io/apis/sertica/sertica-evaluationquestions-api/) — The EvaluationQuestions API from SERTICA — 13 operation(s) for evaluationquestions.
- [SERTICA Excel Import API](https://apis.io/apis/sertica/sertica-excelimport-api/) — The ExcelImport API from SERTICA — 4 operation(s) for excelimport.
- [SERTICA Expected Faults API](https://apis.io/apis/sertica/sertica-expectedfaults-api/) — The ExpectedFaults API from SERTICA — 8 operation(s) for expectedfaults.
- [SERTICA External Calendars API](https://apis.io/apis/sertica/sertica-externalcalendars-api/) — The ExternalCalendars API from SERTICA — 1 operation(s) for externalcalendars.
- [SERTICA Financial Followup Node Responses API](https://apis.io/apis/sertica/sertica-financialfollowupnoderesponses-api/) — The FinancialFollowupNodeResponses API from SERTICA — 2 operation(s) for financialfollowupnoderesponses.
- [SERTICA Flags API](https://apis.io/apis/sertica/sertica-flags-api/) — The Flags API from SERTICA — 8 operation(s) for flags.
- [SERTICA Form Browser API](https://apis.io/apis/sertica/sertica-formbrowser-api/) — The FormBrowser API from SERTICA — 3 operation(s) for formbrowser.
- [SERTICA Form Documents API](https://apis.io/apis/sertica/sertica-formdocuments-api/) — The FormDocuments API from SERTICA — 13 operation(s) for formdocuments.
- [SERTICA Forms API](https://apis.io/apis/sertica/sertica-forms-api/) — The Forms API from SERTICA — 33 operation(s) for forms.
- [SERTICA Forms Signature API](https://apis.io/apis/sertica/sertica-formssignature-api/) — The FormsSignature API from SERTICA — 13 operation(s) for formssignature.
- [SERTICA Form Template Documents API](https://apis.io/apis/sertica/sertica-formtemplatedocuments-api/) — The FormTemplateDocuments API from SERTICA — 15 operation(s) for formtemplatedocuments.
- [SERTICA Form Template Help Image Documents API](https://apis.io/apis/sertica/sertica-formtemplatehelpimagedocuments-api/) — The FormTemplateHelpImageDocuments API from SERTICA — 15 operation(s) for formtemplatehelpimagedocuments.
- [SERTICA Form Template Tables API](https://apis.io/apis/sertica/sertica-formtemplatetables-api/) — The FormTemplateTables API from SERTICA — 9 operation(s) for formtemplatetables.
- [SERTICA Fuel Types API](https://apis.io/apis/sertica/sertica-fueltypes-api/) — The FuelTypes API from SERTICA — 8 operation(s) for fueltypes.
- [SERTICA Function Areas API](https://apis.io/apis/sertica/sertica-functionareas-api/) — The FunctionAreas API from SERTICA — 10 operation(s) for functionareas.
- [SERTICA Garbage Receivers API](https://apis.io/apis/sertica/sertica-garbagereceivers-api/) — The GarbageReceivers API from SERTICA — 10 operation(s) for garbagereceivers.
- [SERTICA Grb Operations API](https://apis.io/apis/sertica/sertica-grboperations-api/) — The GrbOperations API from SERTICA — 18 operation(s) for grboperations.
- [SERTICA Grid Column Layouts API](https://apis.io/apis/sertica/sertica-gridcolumnlayouts-api/) — The GridColumnLayouts API from SERTICA — 2 operation(s) for gridcolumnlayouts.
- [SERTICA Grid Layouts API](https://apis.io/apis/sertica/sertica-gridlayouts-api/) — The GridLayouts API from SERTICA — 9 operation(s) for gridlayouts.
- [SERTICA Group Codes API](https://apis.io/apis/sertica/sertica-groupcodes-api/) — The GroupCodes API from SERTICA — 7 operation(s) for groupcodes.
- [SERTICA Im Invoices API](https://apis.io/apis/sertica/sertica-iminvoices-api/) — The ImInvoices API from SERTICA — 53 operation(s) for iminvoices.
- [SERTICA Inspection Areas API](https://apis.io/apis/sertica/sertica-inspectionareas-api/) — The InspectionAreas API from SERTICA — 7 operation(s) for inspectionareas.
- [SERTICA Inspection Job Histories API](https://apis.io/apis/sertica/sertica-inspectionjobhistories-api/) — The InspectionJobHistories API from SERTICA — 8 operation(s) for inspectionjobhistories.
- [SERTICA Inspection Jobs API](https://apis.io/apis/sertica/sertica-inspectionjobs-api/) — The InspectionJobs API from SERTICA — 9 operation(s) for inspectionjobs.
- [SERTICA Inspection Lists API](https://apis.io/apis/sertica/sertica-inspectionlists-api/) — The InspectionLists API from SERTICA — 14 operation(s) for inspectionlists.
- [SERTICA Inspection List Types API](https://apis.io/apis/sertica/sertica-inspectionlisttypes-api/) — The InspectionListTypes API from SERTICA — 7 operation(s) for inspectionlisttypes.
- [SERTICA Invoice Documents API](https://apis.io/apis/sertica/sertica-invoicedocuments-api/) — The InvoiceDocuments API from SERTICA — 15 operation(s) for invoicedocuments.
- [SERTICA Ios Data Sync API](https://apis.io/apis/sertica/sertica-iosdatasync-api/) — The IosDataSync API from SERTICA — 1 operation(s) for iosdatasync.
- [SERTICA Item Group Selection API](https://apis.io/apis/sertica/sertica-itemgroupselection-api/) — The ItemGroupSelection API from SERTICA — 2 operation(s) for itemgroupselection.
- [SERTICA Item Group Selection Tree API](https://apis.io/apis/sertica/sertica-itemgroupselectiontree-api/) — The ItemGroupSelectionTree API from SERTICA — 3 operation(s) for itemgroupselectiontree.
- [SERTICA Item Locations API](https://apis.io/apis/sertica/sertica-itemlocations-api/) — The ItemLocations API from SERTICA — 11 operation(s) for itemlocations.
- [SERTICA Item Location Tree API](https://apis.io/apis/sertica/sertica-itemlocationtree-api/) — The ItemLocationTree API from SERTICA — 3 operation(s) for itemlocationtree.
- [SERTICA Item Photos API](https://apis.io/apis/sertica/sertica-itemphotos-api/) — The ItemPhotos API from SERTICA — 15 operation(s) for itemphotos.
- [SERTICA Items API](https://apis.io/apis/sertica/sertica-items-api/) — The Items API from SERTICA — 39 operation(s) for items.
- [SERTICA Item Tree API](https://apis.io/apis/sertica/sertica-itemtree-api/) — The ItemTree API from SERTICA — 3 operation(s) for itemtree.
- [SERTICA Item Warehouse Histories API](https://apis.io/apis/sertica/sertica-itemwarehousehistories-api/) — The ItemWarehouseHistories API from SERTICA — 3 operation(s) for itemwarehousehistories.
- [SERTICA Item Warehouses API](https://apis.io/apis/sertica/sertica-itemwarehouses-api/) — The ItemWarehouses API from SERTICA — 3 operation(s) for itemwarehouses.
- [SERTICA Job Groups API](https://apis.io/apis/sertica/sertica-jobgroups-api/) — The JobGroups API from SERTICA — 9 operation(s) for jobgroups.
- [SERTICA Job History Data Entries API](https://apis.io/apis/sertica/sertica-jobhistorydataentries-api/) — The JobHistoryDataEntries API from SERTICA — 4 operation(s) for jobhistorydataentries.
- [SERTICA Job History Data Entry Documents API](https://apis.io/apis/sertica/sertica-jobhistorydataentrydocuments-api/) — The JobHistoryDataEntryDocuments API from SERTICA — 5 operation(s) for jobhistorydataentrydocuments.
- [SERTICA Job List Web Search API](https://apis.io/apis/sertica/sertica-joblistwebsearch-api/) — The JobListWebSearch API from SERTICA — 9 operation(s) for joblistwebsearch.
- [SERTICA Job Mail Templates API](https://apis.io/apis/sertica/sertica-jobmailtemplates-api/) — The JobMailTemplates API from SERTICA — 8 operation(s) for jobmailtemplates.
- [SERTICA Job Recommendations API](https://apis.io/apis/sertica/sertica-jobrecommendations-api/) — The JobRecommendations API from SERTICA — 11 operation(s) for jobrecommendations.
- [SERTICA Job Request Mail Templates API](https://apis.io/apis/sertica/sertica-jobrequestmailtemplates-api/) — The JobRequestMailTemplates API from SERTICA — 8 operation(s) for jobrequestmailtemplates.
- [SERTICA Job Requests API](https://apis.io/apis/sertica/sertica-jobrequests-api/) — The JobRequests API from SERTICA — 17 operation(s) for jobrequests.
- [SERTICA Job Request Template Logos API](https://apis.io/apis/sertica/sertica-jobrequesttemplatelogos-api/) — The JobRequestTemplateLogos API from SERTICA — 15 operation(s) for jobrequesttemplatelogos.
- [SERTICA Job Request Templates API](https://apis.io/apis/sertica/sertica-jobrequesttemplates-api/) — The JobRequestTemplates API from SERTICA — 15 operation(s) for jobrequesttemplates.
- [SERTICA Job Responsibles API](https://apis.io/apis/sertica/sertica-jobresponsibles-api/) — The JobResponsibles API from SERTICA — 6 operation(s) for jobresponsibles.
- [SERTICA Jobs API](https://apis.io/apis/sertica/sertica-jobs-api/) — The Jobs API from SERTICA — 61 operation(s) for jobs.
- [SERTICA Job Sequences API](https://apis.io/apis/sertica/sertica-jobsequences-api/) — The JobSequences API from SERTICA — 10 operation(s) for jobsequences.
- [SERTICA License API](https://apis.io/apis/sertica/sertica-license-api/) — The License API from SERTICA — 4 operation(s) for license.
- [SERTICA Liquid Types API](https://apis.io/apis/sertica/sertica-liquidtypes-api/) — The LiquidTypes API from SERTICA — 8 operation(s) for liquidtypes.
- [SERTICA Localization Languages API](https://apis.io/apis/sertica/sertica-localizationlanguages-api/) — The LocalizationLanguages API from SERTICA — 8 operation(s) for localizationlanguages.
- [SERTICA Localization Texts API](https://apis.io/apis/sertica/sertica-localizationtexts-api/) — The LocalizationTexts API from SERTICA — 13 operation(s) for localizationtexts.
- [SERTICA Log API](https://apis.io/apis/sertica/sertica-log-api/) — The Log API from SERTICA — 12 operation(s) for log.
- [SERTICA Logbook Documents API](https://apis.io/apis/sertica/sertica-logbookdocuments-api/) — The LogbookDocuments API from SERTICA — 11 operation(s) for logbookdocuments.
- [SERTICA Logbook Events API](https://apis.io/apis/sertica/sertica-logbookevents-api/) — The LogbookEvents API from SERTICA — 16 operation(s) for logbookevents.
- [SERTICA Lube Oil Types API](https://apis.io/apis/sertica/sertica-lubeoiltypes-api/) — The LubeOilTypes API from SERTICA — 8 operation(s) for lubeoiltypes.
- [SERTICA Mail Accounts API](https://apis.io/apis/sertica/sertica-mailaccounts-api/) — The MailAccounts API from SERTICA — 9 operation(s) for mailaccounts.
- [SERTICA Management System Approved Plan Documents API](https://apis.io/apis/sertica/sertica-managementsystemapprovedplandocuments-api/) — The ManagementSystemApprovedPlanDocuments API from SERTICA — 15 operation(s) for managementsystemapprovedplandocuments.
- [SERTICA Management System Browser API](https://apis.io/apis/sertica/sertica-managementsystembrowser-api/) — The ManagementSystemBrowser API from SERTICA — 9 operation(s) for managementsystembrowser.
- [SERTICA Management System Change Requests API](https://apis.io/apis/sertica/sertica-managementsystemchangerequests-api/) — The ManagementSystemChangeRequests API from SERTICA — 26 operation(s) for managementsystemchangerequests.
- [SERTICA Management System Document Acknowledgements API](https://apis.io/apis/sertica/sertica-managementsystemdocumentacknowledgements-api/) — The ManagementSystemDocumentAcknowledgements API from SERTICA — 6 operation(s) for managementsystemdocumentacknowledgements.
- [SERTICA Management System Document Documents API](https://apis.io/apis/sertica/sertica-managementsystemdocumentdocuments-api/) — The ManagementSystemDocumentDocuments API from SERTICA — 14 operation(s) for managementsystemdocumentdocuments.
- [SERTICA Management System Documents API](https://apis.io/apis/sertica/sertica-managementsystemdocuments-api/) — The ManagementSystemDocuments API from SERTICA — 13 operation(s) for managementsystemdocuments.
- [SERTICA Management System Publish API](https://apis.io/apis/sertica/sertica-managementsystempublish-api/) — The ManagementSystemPublish API from SERTICA — 11 operation(s) for managementsystempublish.
- [SERTICA Management System RO Cs API](https://apis.io/apis/sertica/sertica-managementsystemrocs-api/) — The ManagementSystemROCs API from SERTICA — 6 operation(s) for managementsystemrocs.
- [SERTICA Management Systems API](https://apis.io/apis/sertica/sertica-managementsystems-api/) — The ManagementSystems API from SERTICA — 21 operation(s) for managementsystems.
- [SERTICA Management System Sections API](https://apis.io/apis/sertica/sertica-managementsystemsections-api/) — The ManagementSystemSections API from SERTICA — 10 operation(s) for managementsystemsections.
- [SERTICA Management System Template Documents API](https://apis.io/apis/sertica/sertica-managementsystemtemplatedocuments-api/) — The ManagementSystemTemplateDocuments API from SERTICA — 13 operation(s) for managementsystemtemplatedocuments.
- [SERTICA Master Data Management API](https://apis.io/apis/sertica/sertica-masterdatamanagement-api/) — The MasterDataManagement API from SERTICA — 4 operation(s) for masterdatamanagement.
- [SERTICA Master Data Management Tasks API](https://apis.io/apis/sertica/sertica-masterdatamanagementtasks-api/) — The MasterDataManagementTasks API from SERTICA — 5 operation(s) for masterdatamanagementtasks.
- [SERTICA Master Data Management Tree Structure API](https://apis.io/apis/sertica/sertica-masterdatamanagementtreestructure-api/) — The MasterDataManagementTreeStructure API from SERTICA — 5 operation(s) for masterdatamanagementtreestructure.
- [SERTICA Master Data Management Unit Tree Structure API](https://apis.io/apis/sertica/sertica-masterdatamanagementunittreestructure-api/) — The MasterDataManagementUnitTreeStructure API from SERTICA — 1 operation(s) for masterdatamanagementunittreestructure.
- [SERTICA Master Unit API](https://apis.io/apis/sertica/sertica-masterunit-api/) — The MasterUnit API from SERTICA — 1 operation(s) for masterunit.
- [SERTICA MDM Unit API](https://apis.io/apis/sertica/sertica-mdmunit-api/) — The MDMUnit API from SERTICA — 1 operation(s) for mdmunit.
- [SERTICA Measurements API](https://apis.io/apis/sertica/sertica-measurements-api/) — The Measurements API from SERTICA — 15 operation(s) for measurements.
- [SERTICA Measuring Units API](https://apis.io/apis/sertica/sertica-measuringunits-api/) — The MeasuringUnits API from SERTICA — 8 operation(s) for measuringunits.
- [SERTICA Odsrb Operations API](https://apis.io/apis/sertica/sertica-odsrboperations-api/) — The OdsrbOperations API from SERTICA — 16 operation(s) for odsrboperations.
- [SERTICA Odsrb Receivers API](https://apis.io/apis/sertica/sertica-odsrbreceivers-api/) — The OdsrbReceivers API from SERTICA — 10 operation(s) for odsrbreceivers.
- [SERTICA Operation Type Configurations API](https://apis.io/apis/sertica/sertica-operationtypeconfigurations-api/) — The OperationTypeConfigurations API from SERTICA — 7 operation(s) for operationtypeconfigurations.
- [SERTICA Options API](https://apis.io/apis/sertica/sertica-options-api/) — The Options API from SERTICA — 13 operation(s) for options.
- [SERTICA Options Dynamic Report Templates API](https://apis.io/apis/sertica/sertica-optionsdynamicreporttemplates-api/) — The OptionsDynamicReportTemplates API from SERTICA — 15 operation(s) for optionsdynamicreporttemplates.
- [SERTICA Options Globals API](https://apis.io/apis/sertica/sertica-optionsglobals-api/) — The OptionsGlobals API from SERTICA — 3 operation(s) for optionsglobals.
- [SERTICA Options Office Dynamic Report Templates API](https://apis.io/apis/sertica/sertica-optionsofficedynamicreporttemplates-api/) — The OptionsOfficeDynamicReportTemplates API from SERTICA — 15 operation(s) for optionsofficedynamicreporttemplates.
- [SERTICA Options Office Label Templates API](https://apis.io/apis/sertica/sertica-optionsofficelabeltemplates-api/) — The OptionsOfficeLabelTemplates API from SERTICA — 15 operation(s) for optionsofficelabeltemplates.
- [SERTICA Options Offices API](https://apis.io/apis/sertica/sertica-optionsoffices-api/) — The OptionsOffices API from SERTICA — 11 operation(s) for optionsoffices.
- [SERTICA Orb Noons API](https://apis.io/apis/sertica/sertica-orbnoons-api/) — The OrbNoons API from SERTICA — 11 operation(s) for orbnoons.
- [SERTICA Orb Operations API](https://apis.io/apis/sertica/sertica-orboperations-api/) — The OrbOperations API from SERTICA — 19 operation(s) for orboperations.
- [SERTICA Packing Units API](https://apis.io/apis/sertica/sertica-packingunits-api/) — The PackingUnits API from SERTICA — 8 operation(s) for packingunits.
- [SERTICA Ports API](https://apis.io/apis/sertica/sertica-ports-api/) — The Ports API from SERTICA — 8 operation(s) for ports.
- [SERTICA Posting Periods API](https://apis.io/apis/sertica/sertica-postingperiods-api/) — The PostingPeriods API from SERTICA — 12 operation(s) for postingperiods.
- [SERTICA Postponement Reasons API](https://apis.io/apis/sertica/sertica-postponementreasons-api/) — The PostponementReasons API from SERTICA — 9 operation(s) for postponementreasons.
- [SERTICA Priorities API](https://apis.io/apis/sertica/sertica-priorities-api/) — The Priorities API from SERTICA — 8 operation(s) for priorities.
- [SERTICA Procedures API](https://apis.io/apis/sertica/sertica-procedures-api/) — The Procedures API from SERTICA — 9 operation(s) for procedures.
- [SERTICA Projects API](https://apis.io/apis/sertica/sertica-projects-api/) — The Projects API from SERTICA — 10 operation(s) for projects.
- [SERTICA Purchase Groups API](https://apis.io/apis/sertica/sertica-purchasegroups-api/) — The PurchaseGroups API from SERTICA — 8 operation(s) for purchasegroups.
- [SERTICA Purchase Order Approvals API](https://apis.io/apis/sertica/sertica-purchaseorderapprovals-api/) — The PurchaseOrderApprovals API from SERTICA — 4 operation(s) for purchaseorderapprovals.
- [SERTICA Purchase Order Delivery Costs API](https://apis.io/apis/sertica/sertica-purchaseorderdeliverycosts-api/) — The PurchaseOrderDeliveryCosts API from SERTICA — 4 operation(s) for purchaseorderdeliverycosts.
- [SERTICA Purchase Order Positions API](https://apis.io/apis/sertica/sertica-purchaseorderpositions-api/) — The PurchaseOrderPositions API from SERTICA — 4 operation(s) for purchaseorderpositions.
- [SERTICA Purchase Types API](https://apis.io/apis/sertica/sertica-purchasetypes-api/) — The PurchaseTypes API from SERTICA — 10 operation(s) for purchasetypes.
- [SERTICA Purifiers API](https://apis.io/apis/sertica/sertica-purifiers-api/) — The Purifiers API from SERTICA — 8 operation(s) for purifiers.
- [SERTICA Receivers API](https://apis.io/apis/sertica/sertica-receivers-api/) — The Receivers API from SERTICA — 10 operation(s) for receivers.
- [SERTICA Reject Reasons API](https://apis.io/apis/sertica/sertica-rejectreasons-api/) — The RejectReasons API from SERTICA — 9 operation(s) for rejectreasons.
- [SERTICA Reminders API](https://apis.io/apis/sertica/sertica-reminders-api/) — The Reminders API from SERTICA — 7 operation(s) for reminders.
- [SERTICA Request For Quotes API](https://apis.io/apis/sertica/sertica-requestforquotes-api/) — The RequestForQuotes API from SERTICA — 30 operation(s) for requestforquotes.
- [SERTICA Requisition Positions API](https://apis.io/apis/sertica/sertica-requisitionpositions-api/) — The RequisitionPositions API from SERTICA — 5 operation(s) for requisitionpositions.
- [SERTICA Requisitions API](https://apis.io/apis/sertica/sertica-requisitions-api/) — The Requisitions API from SERTICA — 46 operation(s) for requisitions.
- [SERTICA Resources API](https://apis.io/apis/sertica/sertica-resources-api/) — The Resources API from SERTICA — 8 operation(s) for resources.
- [SERTICA Roles API](https://apis.io/apis/sertica/sertica-roles-api/) — The Roles API from SERTICA — 9 operation(s) for roles.
- [SERTICA Screen Layouts API](https://apis.io/apis/sertica/sertica-screenlayouts-api/) — The ScreenLayouts API from SERTICA — 3 operation(s) for screenlayouts.
- [SERTICA Seals API](https://apis.io/apis/sertica/sertica-seals-api/) — The Seals API from SERTICA — 12 operation(s) for seals.
- [SERTICA Seal Storage Locations API](https://apis.io/apis/sertica/sertica-sealstoragelocations-api/) — The SealStorageLocations API from SERTICA — 8 operation(s) for sealstoragelocations.
- [SERTICA Seal Types API](https://apis.io/apis/sertica/sertica-sealtypes-api/) — The SealTypes API from SERTICA — 8 operation(s) for sealtypes.
- [SERTICA Sections API](https://apis.io/apis/sertica/sertica-sections-api/) — The Sections API from SERTICA — 17 operation(s) for sections.
- [SERTICA Shipments API](https://apis.io/apis/sertica/sertica-shipments-api/) — The Shipments API from SERTICA — 25 operation(s) for shipments.
- [SERTICA Shipment Ways API](https://apis.io/apis/sertica/sertica-shipmentways-api/) — The ShipmentWays API from SERTICA — 8 operation(s) for shipmentways.
- [SERTICA Soundings API](https://apis.io/apis/sertica/sertica-soundings-api/) — The Soundings API from SERTICA — 11 operation(s) for soundings.
- [SERTICA Sounding Statuses API](https://apis.io/apis/sertica/sertica-soundingstatuses-api/) — The SoundingStatuses API from SERTICA — 8 operation(s) for soundingstatuses.
- [SERTICA Sounding Table Documents API](https://apis.io/apis/sertica/sertica-soundingtabledocuments-api/) — The SoundingTableDocuments API from SERTICA — 11 operation(s) for soundingtabledocuments.
- [SERTICA Sounding Tables API](https://apis.io/apis/sertica/sertica-soundingtables-api/) — The SoundingTables API from SERTICA — 8 operation(s) for soundingtables.
- [SERTICA Standard Texts API](https://apis.io/apis/sertica/sertica-standardtexts-api/) — The StandardTexts API from SERTICA — 9 operation(s) for standardtexts.
- [SERTICA Sub Seal Point Component Types API](https://apis.io/apis/sertica/sertica-subsealpointcomponenttypes-api/) — The SubSealPointComponentTypes API from SERTICA — 8 operation(s) for subsealpointcomponenttypes.
- [SERTICA Sub Seal Points API](https://apis.io/apis/sertica/sertica-subsealpoints-api/) — The SubSealPoints API from SERTICA — 10 operation(s) for subsealpoints.
- [SERTICA Substances API](https://apis.io/apis/sertica/sertica-substances-api/) — The Substances API from SERTICA — 8 operation(s) for substances.
- [SERTICA Suggested Actions API](https://apis.io/apis/sertica/sertica-suggestedactions-api/) — The SuggestedActions API from SERTICA — 6 operation(s) for suggestedactions.
- [SERTICA Tank Operation Configurations API](https://apis.io/apis/sertica/sertica-tankoperationconfigurations-api/) — The TankOperationConfigurations API from SERTICA — 10 operation(s) for tankoperationconfigurations.
- [SERTICA Tanks API](https://apis.io/apis/sertica/sertica-tanks-api/) — The Tanks API from SERTICA — 14 operation(s) for tanks.
- [SERTICA Technical Accounts API](https://apis.io/apis/sertica/sertica-technicalaccounts-api/) — The TechnicalAccounts API from SERTICA — 10 operation(s) for technicalaccounts.
- [SERTICA Transaction Queue API](https://apis.io/apis/sertica/sertica-transactionqueue-api/) — The TransactionQueue API from SERTICA — 4 operation(s) for transactionqueue.
- [SERTICA Tree Structure API](https://apis.io/apis/sertica/sertica-treestructure-api/) — The TreeStructure API from SERTICA — 3 operation(s) for treestructure.
- [SERTICA Unit Companies API](https://apis.io/apis/sertica/sertica-unitcompanies-api/) — The UnitCompanies API from SERTICA — 10 operation(s) for unitcompanies.
- [SERTICA Unit Groups API](https://apis.io/apis/sertica/sertica-unitgroups-api/) — The UnitGroups API from SERTICA — 9 operation(s) for unitgroups.
- [SERTICA Units API](https://apis.io/apis/sertica/sertica-units-api/) — The Units API from SERTICA — 19 operation(s) for units.
- [SERTICA Unit Shipments API](https://apis.io/apis/sertica/sertica-unitshipments-api/) — The UnitShipments API from SERTICA — 18 operation(s) for unitshipments.
- [SERTICA Users API](https://apis.io/apis/sertica/sertica-users-api/) — The Users API from SERTICA — 20 operation(s) for users.
- [SERTICA VAT API](https://apis.io/apis/sertica/sertica-vat-api/) — The VAT API from SERTICA — 8 operation(s) for vat.
- [SERTICA Vessel Report Browser API](https://apis.io/apis/sertica/sertica-vesselreportbrowser-api/) — The VesselReportBrowser API from SERTICA — 3 operation(s) for vesselreportbrowser.
- [SERTICA Vessel Report Field List Template Revision Caches API](https://apis.io/apis/sertica/sertica-vesselreportfieldlisttemplaterevisioncaches-api/) — The VesselReportFieldListTemplateRevisionCaches API from SERTICA — 2 operation(s) for vesselreportfieldlisttemplaterevisioncaches.
- [SERTICA Vessel Report Field List Templates API](https://apis.io/apis/sertica/sertica-vesselreportfieldlisttemplates-api/) — The VesselReportFieldListTemplates API from SERTICA — 9 operation(s) for vesselreportfieldlisttemplates.
- [SERTICA Vessel Reports API](https://apis.io/apis/sertica/sertica-vesselreports-api/) — The VesselReports API from SERTICA — 36 operation(s) for vesselreports.
- [SERTICA Vessel Report Scripts API](https://apis.io/apis/sertica/sertica-vesselreportscripts-api/) — The VesselReportScripts API from SERTICA — 4 operation(s) for vesselreportscripts.
- [SERTICA Vessel Report Sequence Instances API](https://apis.io/apis/sertica/sertica-vesselreportsequenceinstances-api/) — The VesselReportSequenceInstances API from SERTICA — 12 operation(s) for vesselreportsequenceinstances.
- [SERTICA Vessel Report Sequences API](https://apis.io/apis/sertica/sertica-vesselreportsequences-api/) — The VesselReportSequences API from SERTICA — 10 operation(s) for vesselreportsequences.
- [SERTICA Vessel Report Signature API](https://apis.io/apis/sertica/sertica-vesselreportsignature-api/) — The VesselReportSignature API from SERTICA — 13 operation(s) for vesselreportsignature.
- [SERTICA Vessel Report Table Revision Caches API](https://apis.io/apis/sertica/sertica-vesselreporttablerevisioncaches-api/) — The VesselReportTableRevisionCaches API from SERTICA — 2 operation(s) for vesselreporttablerevisioncaches.
- [SERTICA Vessel Report Tables API](https://apis.io/apis/sertica/sertica-vesselreporttables-api/) — The VesselReportTables API from SERTICA — 10 operation(s) for vesselreporttables.
- [SERTICA Vessel Report Type Field Definitions API](https://apis.io/apis/sertica/sertica-vesselreporttypefielddefinitions-api/) — The VesselReportTypeFieldDefinitions API from SERTICA — 1 operation(s) for vesselreporttypefielddefinitions.
- [SERTICA Vessel Report Type Groups API](https://apis.io/apis/sertica/sertica-vesselreporttypegroups-api/) — The VesselReportTypeGroups API from SERTICA — 10 operation(s) for vesselreporttypegroups.
- [SERTICA Vessel Report Type Revision Caches API](https://apis.io/apis/sertica/sertica-vesselreporttyperevisioncaches-api/) — The VesselReportTypeRevisionCaches API from SERTICA — 2 operation(s) for vesselreporttyperevisioncaches.
- [SERTICA Vessel Report Types API](https://apis.io/apis/sertica/sertica-vesselreporttypes-api/) — The VesselReportTypes API from SERTICA — 16 operation(s) for vesselreporttypes.
- [SERTICA Vessel Types API](https://apis.io/apis/sertica/sertica-vesseltypes-api/) — The VesselTypes API from SERTICA — 8 operation(s) for vesseltypes.
- [SERTICA Voyage Reports API](https://apis.io/apis/sertica/sertica-voyagereports-api/) — The VoyageReports API from SERTICA — 21 operation(s) for voyagereports.
- [SERTICA Vrs API Configurations API](https://apis.io/apis/sertica/sertica-vrsapiconfigurations-api/) — The VrsApiConfigurations API from SERTICA — 8 operation(s) for vrsapiconfigurations.
- [SERTICA Vrs API Scripts API](https://apis.io/apis/sertica/sertica-vrsapiscripts-api/) — The VrsApiScripts API from SERTICA — 8 operation(s) for vrsapiscripts.
- [SERTICA Warehouses API](https://apis.io/apis/sertica/sertica-warehouses-api/) — The Warehouses API from SERTICA — 10 operation(s) for warehouses.
- [SERTICA Web Dashboard Content API](https://apis.io/apis/sertica/sertica-webdashboardcontent-api/) — The WebDashboardContent API from SERTICA — 12 operation(s) for webdashboardcontent.
- [SERTICA Web Dashboard Page Backgrounds API](https://apis.io/apis/sertica/sertica-webdashboardpagebackgrounds-api/) — The WebDashboardPageBackgrounds API from SERTICA — 15 operation(s) for webdashboardpagebackgrounds.
- [SERTICA Web Dashboard Pages API](https://apis.io/apis/sertica/sertica-webdashboardpages-api/) — The WebDashboardPages API from SERTICA — 17 operation(s) for webdashboardpages.
- [SERTICA Web Dashboards API](https://apis.io/apis/sertica/sertica-webdashboards-api/) — The WebDashboards API from SERTICA — 13 operation(s) for webdashboards.
- [SERTICA Webhooks API](https://apis.io/apis/sertica/sertica-webhooks-api/) — The Webhooks API from SERTICA — 20 operation(s) for webhooks.
- [SERTICA Web Task List Configurations API](https://apis.io/apis/sertica/sertica-webtasklistconfigurations-api/) — The WebTaskListConfigurations API from SERTICA — 7 operation(s) for webtasklistconfigurations.
- [SERTICA Analytics Reports API](https://apis.io/apis/sertica/sertica-analytics-reports-api/) — The Analytics Reports API from SERTICA — 10 operation(s) for analytics reports.
- [SERTICA Certificate Groups API](https://apis.io/apis/sertica/sertica-certificate-groups-api/) — The Certificate Groups API from SERTICA — 11 operation(s) for certificate groups.
- [SERTICA Country Codes API](https://apis.io/apis/sertica/sertica-country-codes-api/) — The Country Codes API from SERTICA — 8 operation(s) for country codes.
- [SERTICA Document Groups API](https://apis.io/apis/sertica/sertica-document-groups-api/) — The Document Groups API from SERTICA — 8 operation(s) for document groups.
- [SERTICA Document Types API](https://apis.io/apis/sertica/sertica-document-types-api/) — The Document Types API from SERTICA — 8 operation(s) for document types.
- [SERTICA Event Reports API](https://apis.io/apis/sertica/sertica-event-reports-api/) — The Event Reports API from SERTICA — 9 operation(s) for event reports.
- [SERTICA External Items API](https://apis.io/apis/sertica/sertica-external-items-api/) — The External Items API from SERTICA — 6 operation(s) for external items.
- [SERTICA Form Templates API](https://apis.io/apis/sertica/sertica-form-templates-api/) — The Form Templates API from SERTICA — 22 operation(s) for form templates.
- [SERTICA Item groups API](https://apis.io/apis/sertica/sertica-item-groups-api/) — The Item groups API from SERTICA — 8 operation(s) for item groups.
- [SERTICA Item Types API](https://apis.io/apis/sertica/sertica-item-types-api/) — The Item Types API from SERTICA — 8 operation(s) for item types.
- [SERTICA Job Histories API](https://apis.io/apis/sertica/sertica-job-histories-api/) — The Job Histories API from SERTICA — 31 operation(s) for job histories.
- [SERTICA Job Templates API](https://apis.io/apis/sertica/sertica-job-templates-api/) — The Job Templates API from SERTICA — 12 operation(s) for job templates.
- [SERTICA Measurement Locations API](https://apis.io/apis/sertica/sertica-measurement-locations-api/) — The Measurement Locations API from SERTICA — 8 operation(s) for measurement locations.
- [SERTICA Measurement Types API](https://apis.io/apis/sertica/sertica-measurement-types-api/) — The Measurement Types API from SERTICA — 8 operation(s) for measurement types.
- [SERTICA Payment Conditions API](https://apis.io/apis/sertica/sertica-payment-conditions-api/) — The Payment Conditions API from SERTICA — 8 operation(s) for payment conditions.
- [SERTICA Purchase Orders API](https://apis.io/apis/sertica/sertica-purchase-orders-api/) — The Purchase Orders API from SERTICA — 65 operation(s) for purchase orders.
- [SERTICA Scheduled Tasks API](https://apis.io/apis/sertica/sertica-scheduled-tasks-api/) — The Scheduled Tasks API from SERTICA — 14 operation(s) for scheduled tasks.
- [SERTICA User Groups API](https://apis.io/apis/sertica/sertica-user-groups-api/) — The User Groups API from SERTICA — 14 operation(s) for user groups.
- [SERTICA User rights API](https://apis.io/apis/sertica/sertica-user-rights-api/) — The User rights API from SERTICA — 2 operation(s) for user rights.
- [SERTICA User Settings API](https://apis.io/apis/sertica/sertica-user-settings-api/) — The User Settings API from SERTICA — 6 operation(s) for user settings.
- [SERTICA Value Lists API](https://apis.io/apis/sertica/sertica-value-lists-api/) — The Value Lists API from SERTICA — 9 operation(s) for value lists.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Sertica Webhooks](https://apis.io/asyncapis/sertica/sertica-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [sertica](https://apis.io/servers/sertica/sertica/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Sertica Agentic Access](https://apis.io/agentic-access/sertica/sertica-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Sertica Web Api Overlay](https://apis.io/overlays/sertica/sertica-web-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Sertica Authentication](https://apis.io/security/sertica/sertica-authentication/)
- [Sertica Domain Security](https://apis.io/security/sertica/sertica-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Sertica Plans Pricing](https://apis.io/plans/sertica/sertica-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Sertica Rate Limits](https://apis.io/rate-limits/sertica/sertica-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Sertica Finops](https://apis.io/finops/sertica/sertica-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.sertica.com/)
- [Documentation](https://support.sertica.com/hc/en-us/articles/28558470734109-SERTICA-Application-Programming-Interface)
- [Getting started](https://support.sertica.com/hc/en-us/articles/28558504030365-Example-Get-component-data)
- [API reference](https://docs.sertica.com/api/swagger/index.html)
- [Support](https://support.sertica.com/hc/en-us)
- [Blog](https://www.sertica.com/blog/)
- [Privacy policy](https://www.sertica.com/privacy-policy/)

## API Evangelist rating

**Kin Score 45.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 53.2 |
| Contract governance | 4.5 |
| Operational transparency | 23.7 |
| Developer ergonomics | 56.5 |
| Access clarity | 10.5 |

**Agent readiness 30.4** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | mostly (partial credit) |

**Regulatory alignment 20.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/sertica/](https://apis.io/providers/sertica/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for SERTICA: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/sertica/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
