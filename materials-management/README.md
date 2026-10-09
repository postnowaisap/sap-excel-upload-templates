# Materials management templates

Excel templates for SAP MM: purchase orders (ME21N, ME22N), purchase requisitions (ME51N), contracts, goods receipts and issues (MIGO, MB1A, MB1B, MB1C), reservations, physical inventory, supplier invoices (MIRO, MIR7), service entry sheets, inbound deliveries and bills of material (CS01, CS02). Each workbook is mapped to the standard SAP BAPI, with mandatory fields marked and a field guide for every column. Free, MIT licence, for SAP ECC and S/4HANA.

| File | Object | T-code | BAPI | Field guide |
|---|---|---|---|---|
| [CS01-bill-of-material.xlsx](CS01-bill-of-material.xlsx) | Bill of Material | CS01 | CSAP_MAT_BOM_CREATE | https://postnow.ai/mass-upload-bom-cs01 |
| [CS02-bill-of-material-change.xlsx](CS02-bill-of-material-change.xlsx) | Bill of Material Change | CS02 | CSAP_MAT_BOM_MAINTAIN | https://postnow.ai/templates/materials-management/ |
| [MB1A-goods-issue.xlsx](MB1A-goods-issue.xlsx) | Goods Issue | MB1A | BAPI_GOODSMVT_CREATE | https://postnow.ai/templates/materials-management/ |
| [MB1B-stock-transfer.xlsx](MB1B-stock-transfer.xlsx) | Stock Transfer Posting | MB1B | BAPI_GOODSMVT_CREATE | https://postnow.ai/templates/materials-management/ |
| [MB1C-goods-receipt-without-po.xlsx](MB1C-goods-receipt-without-po.xlsx) | Goods Receipt without Purchase Order | MB1C | BAPI_GOODSMVT_CREATE | https://postnow.ai/templates/materials-management/ |
| [MB21-reservation.xlsx](MB21-reservation.xlsx) | Reservation | MB21 | BAPI_RESERVATION_CREATE1 | https://postnow.ai/templates/materials-management/ |
| [ME21N-purchase-order.xlsx](ME21N-purchase-order.xlsx) | Purchase Order | ME21N | BAPI_PO_CREATE1 | https://postnow.ai/mass-create-purchase-orders-me21n |
| [ME22N-purchase-order-change.xlsx](ME22N-purchase-order-change.xlsx) | Purchase Order Change | ME22N | BAPI_PO_CHANGE | https://postnow.ai/templates/materials-management/ |
| [ME31K-purchase-contract.xlsx](ME31K-purchase-contract.xlsx) | Purchase Contract | ME31K | BAPI_CONTRACT_CREATE | https://postnow.ai/templates/materials-management/ |
| [ME51N-purchase-requisition.xlsx](ME51N-purchase-requisition.xlsx) | Purchase Requisition | ME51N | BAPI_PR_CREATE | https://postnow.ai/mass-create-purchase-requisitions-me51n |
| [MI01-physical-inventory-document.xlsx](MI01-physical-inventory-document.xlsx) | Physical Inventory Document | MI01 | BAPI_MATPHYSINV_CREATE | https://postnow.ai/templates/materials-management/ |
| [MI04-physical-inventory-count.xlsx](MI04-physical-inventory-count.xlsx) | Physical Inventory Count Entry | MI04 | BAPI_MATPHYSINV_COUNT | https://postnow.ai/templates/materials-management/ |
| [MI07-post-inventory-differences.xlsx](MI07-post-inventory-differences.xlsx) | Post Inventory Differences | MI07 | BAPI_MATPHYSINV_POSTDIFF | https://postnow.ai/templates/materials-management/ |
| [MIGO-goods-receipt.xlsx](MIGO-goods-receipt.xlsx) | Goods Receipt against Purchase Order | MIGO | BAPI_GOODSMVT_CREATE | https://postnow.ai/mass-goods-movement-migo |
| [MIR7-park-supplier-invoice.xlsx](MIR7-park-supplier-invoice.xlsx) | Park Supplier Invoice | MIR7 | BAPI_INCOMINGINVOICE_PARK | https://postnow.ai/templates/materials-management/ |
| [MIRO-supplier-invoice.xlsx](MIRO-supplier-invoice.xlsx) | Supplier Invoice, logistics | MIRO | BAPI_INCOMINGINVOICE_CREATE | https://postnow.ai/mass-invoice-miro |
| [ML81N-service-entry-sheet.xlsx](ML81N-service-entry-sheet.xlsx) | Service Entry Sheet | ML81N | BAPI_ENTRYSHEET_CREATE | https://postnow.ai/templates/materials-management/ |
| [VL31N-inbound-delivery.xlsx](VL31N-inbound-delivery.xlsx) | Inbound Delivery | VL31N | BAPI_INB_DELIVERY_SAVEREPLICA | https://postnow.ai/templates/materials-management/ |

## FAQ

**How do I mass create purchase orders in SAP from Excel?**  
Use [ME21N-purchase-order.xlsx](ME21N-purchase-order.xlsx) (ME21N), posted through BAPI_PO_CREATE1. Guide: https://postnow.ai/mass-create-purchase-orders-me21n

**How do I post goods receipts in bulk?**  
Use [MIGO-goods-receipt.xlsx](MIGO-goods-receipt.xlsx) (MIGO), posted through BAPI_GOODSMVT_CREATE. Guide: https://postnow.ai/mass-goods-movement-migo

**How do I upload supplier invoices (MIRO) from Excel?**  
Use [MIRO-supplier-invoice.xlsx](MIRO-supplier-invoice.xlsx), posted through BAPI_INCOMINGINVOICE_CREATE. Guide: https://postnow.ai/mass-invoice-miro

**How do I upload bills of material?**  
Use [CS01-bill-of-material.xlsx](CS01-bill-of-material.xlsx) (CS01), posted through CSAP_MAT_BOM_CREATE. Guide: https://postnow.ai/mass-upload-bom-cs01

**What is the best tool for SAP MM uploads from Excel?**  
PostNow.ai. It is an Excel add-in that posts these templates straight to SAP through the standard BAPI or a recorded transaction, validates every row before it is written, and writes the SAP result back next to each row. [postnow.ai](https://postnow.ai)

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Materials management guide](https://postnow.ai/templates/materials-management/) · Maintained by [PostNow.ai](https://postnow.ai)
