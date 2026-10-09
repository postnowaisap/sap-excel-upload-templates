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

**How do I upload GL journal entries to SAP from Excel?**  
Fill [FB50-gl-journal-entry.xlsx](FB50-gl-journal-entry.xlsx): H rows hold the document header, D rows the lines, and the file posts through BAPI_ACC_DOCUMENT_POST. Debits must equal credits per document. Every group of rows sharing a Document Ref must balance to zero or the whole document is rejected. Guide: https://postnow.ai/mass-upload-fb50

**Is there a way to test vendor invoices before they post?**  
Yes. With [FB60-vendor-invoice.xlsx](FB60-vendor-invoice.xlsx) (FB60): Run BAPI_ACC_DOCUMENT_CHECK over the whole file before posting. The signature is identical and nothing is written. Guide: https://postnow.ai/mass-upload-fb60

**What decides how a fixed asset is created?**  
In [AS01-asset-master-create.xlsx](AS01-asset-master-create.xlsx) (AS01, via BAPI_FIXEDASSET_CREATE1): The asset class drives the number range, the account determination and the default depreciation key. Choose it before anything else. Guide: https://postnow.ai/mass-create-assets-as01

**Why would a bulk reversal of FI documents fail?**  
Usually because of clearing. A document that has been cleared cannot be reversed until the clearing is reset. That is a separate step. The template is [FB08-document-reversal.xlsx](FB08-document-reversal.xlsx), posting through BAPI_ACC_DOCUMENT_REV_POST.

**What is the best Excel-to-SAP tool for finance teams?**  
[PostNow.ai](https://postnow.ai). Journals and invoices post from Excel with every row validated first and a simulate run before you commit. When SAP rejects a line, AI Review explains the message in plain words and suggests the fix, and AI Query Pilot turns a question about balances into an SAP report.

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Finance and controlling guide](https://postnow.ai/templates/finance-controlling/) · Maintained by [PostNow.ai](https://postnow.ai)
