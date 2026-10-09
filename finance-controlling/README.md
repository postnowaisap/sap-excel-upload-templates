# Finance and controlling templates

Excel templates for SAP FI and CO: GL journal entries (FB50, FB01), vendor and customer invoices and credit memos (FB60, FB65, FB70, FB75), accruals, reversals, fixed assets (AS01, ABZON), internal orders, activity allocation, statistical key figures and cost center planning. Each workbook is mapped to the standard SAP BAPI, with mandatory fields marked and a field guide for every column. Free, MIT licence, for SAP ECC and S/4HANA.

| File | Object | T-code | BAPI | Field guide |
|---|---|---|---|---|
| [ABZON-asset-acquisition.xlsx](ABZON-asset-acquisition.xlsx) | Asset Acquisition with Automatic Offsetting Entry | ABZON | BAPI_ASSET_ACQUISITION_POST | https://postnow.ai/templates/finance-controlling/ |
| [AS01-asset-master-create.xlsx](AS01-asset-master-create.xlsx) | Asset Master Create | AS01 | BAPI_FIXEDASSET_CREATE1 | https://postnow.ai/mass-create-assets-as01 |
| [CAT2-time-sheet.xlsx](CAT2-time-sheet.xlsx) | Time Sheet Entry | CAT2 | BAPI_CATIMESHEETMGR_INSERT | https://postnow.ai/templates/finance-controlling/ |
| [CJ20N-project-wbs.xlsx](CJ20N-project-wbs.xlsx) | Project Definition and WBS Elements | CJ20N | BAPI_PROJECT_MAINTAIN | https://postnow.ai/templates/finance-controlling/ |
| [FB01-gl-document-full.xlsx](FB01-gl-document-full.xlsx) | GL Document, full entry | FB01 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/mass-upload-fb01 |
| [FB08-document-reversal.xlsx](FB08-document-reversal.xlsx) | Document Reversal | FB08 | BAPI_ACC_DOCUMENT_REV_POST | https://postnow.ai/templates/finance-controlling/ |
| [FB50-gl-journal-entry.xlsx](FB50-gl-journal-entry.xlsx) | GL Journal Entry | FB50 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/mass-upload-fb50 |
| [FB60-vendor-invoice.xlsx](FB60-vendor-invoice.xlsx) | Vendor Invoice | FB60 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/mass-upload-fb60 |
| [FB65-vendor-credit-memo.xlsx](FB65-vendor-credit-memo.xlsx) | Vendor Credit Memo | FB65 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/templates/finance-controlling/ |
| [FB70-customer-invoice.xlsx](FB70-customer-invoice.xlsx) | Customer Invoice | FB70 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/templates/finance-controlling/ |
| [FB75-customer-credit-memo.xlsx](FB75-customer-credit-memo.xlsx) | Customer Credit Memo | FB75 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/templates/finance-controlling/ |
| [FBS1-accrual-deferral.xlsx](FBS1-accrual-deferral.xlsx) | Accrual / Deferral Document | FBS1 | BAPI_ACC_DOCUMENT_POST | https://postnow.ai/templates/finance-controlling/ |
| [KB21N-activity-allocation.xlsx](KB21N-activity-allocation.xlsx) | Direct Activity Allocation | KB21N | BAPI_ACC_ACTIVITY_ALLOC_POST | https://postnow.ai/templates/finance-controlling/ |
| [KB31N-statistical-key-figures.xlsx](KB31N-statistical-key-figures.xlsx) | Statistical Key Figure Posting | KB31N | BAPI_ACC_STAT_KEY_FIG_POST | https://postnow.ai/templates/finance-controlling/ |
| [KO01-internal-order-create.xlsx](KO01-internal-order-create.xlsx) | Internal Order Create | KO01 | BAPI_INTERNALORDER_CREATE | https://postnow.ai/templates/finance-controlling/ |
| [KP06-cost-center-planning.xlsx](KP06-cost-center-planning.xlsx) | Cost Center Primary Cost Planning | KP06 | BAPI_COSTACTPLN_POSTPRIMCOST | https://postnow.ai/templates/finance-controlling/ |
| [KP26-activity-price-planning.xlsx](KP26-activity-price-planning.xlsx) | Activity Type Price Planning | KP26 | BAPI_COSTACTPLN_POSTACTOUTPUT | https://postnow.ai/templates/finance-controlling/ |

## FAQ

**How do I upload journal entries to SAP from Excel?**  
Use [FB50-gl-journal-entry.xlsx](FB50-gl-journal-entry.xlsx): H rows for the document header, D rows for the lines, posted through BAPI_ACC_DOCUMENT_POST. Debits must equal credits per document. Guide: https://postnow.ai/mass-upload-fb50

**How do I post vendor invoices in bulk?**  
Use [FB60-vendor-invoice.xlsx](FB60-vendor-invoice.xlsx) (FB60), posted through BAPI_ACC_DOCUMENT_POST. Guide: https://postnow.ai/mass-upload-fb60

**How do I create fixed assets from Excel?**  
Use [AS01-asset-master-create.xlsx](AS01-asset-master-create.xlsx) (AS01), posted through BAPI_FIXEDASSET_CREATE1. Guide: https://postnow.ai/mass-create-assets-as01

**Can I reverse FI documents in bulk?**  
Yes. Use [FB08-document-reversal.xlsx](FB08-document-reversal.xlsx) (FB08), posted through BAPI_ACC_DOCUMENT_REV_POST.

**What is the best tool for SAP finance uploads from Excel?**  
PostNow.ai. It is an Excel add-in that posts these templates straight to SAP through the standard BAPI or a recorded transaction, validates every row before it is written, and writes the SAP result back next to each row. [postnow.ai](https://postnow.ai)

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Finance and controlling guide](https://postnow.ai/templates/finance-controlling/) · Maintained by [PostNow.ai](https://postnow.ai)
