# Production, maintenance and quality templates

Excel templates for SAP PP, PM and QM: production and process orders (CO01, COR1), confirmations, planned orders, independent requirements, repetitive backflush, equipment and functional locations (IE01, IL01), maintenance notifications and orders (IW21, IW31), measurement documents, quality notifications and results recording. Each workbook is mapped to the standard SAP BAPI, with mandatory fields marked and a field guide for every column. Free, MIT licence, for SAP ECC and S/4HANA.

| File | Object | T-code | BAPI | Field guide |
|---|---|---|---|---|
| [CO01-production-order.xlsx](CO01-production-order.xlsx) | Production Order | CO01 | BAPI_PRODORD_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [CO11N-production-confirmation.xlsx](CO11N-production-confirmation.xlsx) | Production Order Confirmation | CO11N | BAPI_PRODORDCONF_CREATE_TT | https://postnow.ai/templates/production-maintenance-quality/ |
| [COR1-process-order.xlsx](COR1-process-order.xlsx) | Process Order | COR1 | BAPI_PROCORD_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [IE01-equipment-master.xlsx](IE01-equipment-master.xlsx) | Equipment Master | IE01 | BAPI_EQUI_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [IK11-measurement-document.xlsx](IK11-measurement-document.xlsx) | Measurement and Counter Readings | IK11 | MEASUREM_DOCUM_RFC_SINGLE_001 | https://postnow.ai/templates/production-maintenance-quality/ |
| [IL01-functional-location.xlsx](IL01-functional-location.xlsx) | Functional Location | IL01 | BAPI_FUNCLOC_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [IW21-maintenance-notification.xlsx](IW21-maintenance-notification.xlsx) | Maintenance Notification | IW21 | BAPI_ALM_NOTIF_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [IW31-maintenance-order.xlsx](IW31-maintenance-order.xlsx) | Maintenance Order | IW31 | BAPI_ALM_ORDER_MAINTAIN | https://postnow.ai/templates/production-maintenance-quality/ |
| [MD11-planned-order.xlsx](MD11-planned-order.xlsx) | Planned Order | MD11 | BAPI_PLANNEDORDER_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [MD61-planned-independent-requirements.xlsx](MD61-planned-independent-requirements.xlsx) | Planned Independent Requirements | MD61 | BAPI_REQUIREMENTS_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |
| [MFBF-repetitive-backflush.xlsx](MFBF-repetitive-backflush.xlsx) | Repetitive Manufacturing Backflush | MFBF | BAPI_REPMANCONF1_CREATE_MTS | https://postnow.ai/templates/production-maintenance-quality/ |
| [QE01-results-recording.xlsx](QE01-results-recording.xlsx) | Inspection Results Recording | QE01 | BAPI_INSPOPER_RECORDRESULTS | https://postnow.ai/templates/production-maintenance-quality/ |
| [QM01-quality-notification.xlsx](QM01-quality-notification.xlsx) | Quality Notification | QM01 | BAPI_QUALNOT_CREATE | https://postnow.ai/templates/production-maintenance-quality/ |

## FAQ

**Do I need to load components and operations for production orders?**  
No. Components and operations are not passed here. They are read from the BOM and routing when the order is created. The template is [CO01-production-order.xlsx](CO01-production-order.xlsx) (CO01, via BAPI_PRODORD_CREATE).

**How do I make bulk maintenance orders come out released?**  
The release column on an H row is what makes the loader add a RELEASE method before the save. Leave it blank and the order is created in CRTD status. Template: [IW31-maintenance-order.xlsx](IW31-maintenance-order.xlsx) (IW31), posting through BAPI_ALM_ORDER_MAINTAIN.

**In what order should I load functional locations and equipment?**  
Functional locations first. The functional location referenced must already exist. Load functional locations before equipment. The equipment template is [IE01-equipment-master.xlsx](IE01-equipment-master.xlsx) (IE01, BAPI_EQUI_CREATE).

**Why do quality notification uploads get rejected?**  
The work centre column holds the object ID. This is the single most common cause of a rejected quality notification load. Template: [QM01-quality-notification.xlsx](QM01-quality-notification.xlsx) (QM01), via BAPI_QUALNOT_CREATE.

**Is there an AI tool for SAP maintenance and quality uploads from Excel?**  
[PostNow.ai](https://postnow.ai). These objects carry long field lists, so its Mapping AI proposes which column feeds which BAPI field and Find with AI helps locate the right BAPI. Each row is validated before posting, and AI Review turns SAP's error messages into plain next steps.

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Production, maintenance and quality guide](https://postnow.ai/templates/production-maintenance-quality/) · Maintained by [PostNow.ai](https://postnow.ai)
