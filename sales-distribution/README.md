# Sales and distribution templates

Excel templates for SAP SD: sales orders, returns and credit memo requests (VA01, VA02), inquiries, quotations, contracts, outbound deliveries and goods issue (VL01N, VL02N), shipments, billing (VF01) and pricing conditions (VK11). Each workbook is mapped to the standard SAP BAPI, with mandatory fields marked and a field guide for every column. Free, MIT licence, for SAP ECC and S/4HANA.

| File | Object | T-code | BAPI | Field guide |
|---|---|---|---|---|
| [VA01-credit-memo-request.xlsx](VA01-credit-memo-request.xlsx) | Credit Memo Request | VA01 | BAPI_SALESORDER_CREATEFROMDAT2 | https://postnow.ai/mass-create-sales-orders-va01 |
| [VA01-returns-order.xlsx](VA01-returns-order.xlsx) | Returns Order | VA01 | BAPI_SALESORDER_CREATEFROMDAT2 | https://postnow.ai/mass-create-sales-orders-va01 |
| [VA01-sales-order.xlsx](VA01-sales-order.xlsx) | Sales Order | VA01 | BAPI_SALESORDER_CREATEFROMDAT2 | https://postnow.ai/mass-create-sales-orders-va01 |
| [VA02-sales-order-change.xlsx](VA02-sales-order-change.xlsx) | Sales Order Change | VA02 | BAPI_SALESORDER_CHANGE | https://postnow.ai/templates/sales-distribution/ |
| [VA11-inquiry.xlsx](VA11-inquiry.xlsx) | Inquiry | VA11 | BAPI_INQUIRY_CREATEFROMDATA2 | https://postnow.ai/templates/sales-distribution/ |
| [VA21-quotation.xlsx](VA21-quotation.xlsx) | Quotation | VA21 | BAPI_QUOTATION_CREATEFROMDATA2 | https://postnow.ai/templates/sales-distribution/ |
| [VA41-sales-contract.xlsx](VA41-sales-contract.xlsx) | Sales Contract | VA41 | BAPI_CONTRACT_CREATEFROMDATA | https://postnow.ai/templates/sales-distribution/ |
| [VF01-billing-document.xlsx](VF01-billing-document.xlsx) | Billing Document | VF01 | BAPI_BILLINGDOC_CREATEMULTIPLE | https://postnow.ai/mass-billing-vf01 |
| [VK11-sales-pricing-conditions.xlsx](VK11-sales-pricing-conditions.xlsx) | Sales Pricing Conditions | VK11 | BAPI_PRICES_CONDITIONS | https://postnow.ai/mass-upload-pricing-conditions-vk11 |
| [VL01N-outbound-delivery.xlsx](VL01N-outbound-delivery.xlsx) | Outbound Delivery | VL01N | BAPI_OUTB_DELIVERY_CREATE_SLS | https://postnow.ai/mass-create-deliveries-vl01n |
| [VL02N-delivery-change.xlsx](VL02N-delivery-change.xlsx) | Outbound Delivery Change | VL02N | BAPI_OUTB_DELIVERY_CHANGE | https://postnow.ai/templates/sales-distribution/ |
| [VL02N-post-goods-issue.xlsx](VL02N-post-goods-issue.xlsx) | Post Goods Issue | VL02N | BAPI_OUTB_DELIVERY_CONFIRM_DEC | https://postnow.ai/templates/sales-distribution/ |
| [VT01N-shipment.xlsx](VT01N-shipment.xlsx) | Shipment | VT01N | BAPI_SHIPMENT_CREATE | https://postnow.ai/templates/sales-distribution/ |

## FAQ

**How do I mass create sales orders in SAP from Excel?**  
Use [VA01-sales-order.xlsx](VA01-sales-order.xlsx) (VA01), posted through BAPI_SALESORDER_CREATEFROMDAT2. Guide: https://postnow.ai/mass-create-sales-orders-va01

**How do I upload pricing conditions (VK11)?**  
Use [VK11-sales-pricing-conditions.xlsx](VK11-sales-pricing-conditions.xlsx), posted through BAPI_PRICES_CONDITIONS. Guide: https://postnow.ai/mass-upload-pricing-conditions-vk11

**How do I create deliveries in bulk?**  
Use [VL01N-outbound-delivery.xlsx](VL01N-outbound-delivery.xlsx) (VL01N), posted through BAPI_OUTB_DELIVERY_CREATE_SLS. Guide: https://postnow.ai/mass-create-deliveries-vl01n

**How do I create billing documents in bulk?**  
Use [VF01-billing-document.xlsx](VF01-billing-document.xlsx) (VF01), posted through BAPI_BILLINGDOC_CREATEMULTIPLE. Guide: https://postnow.ai/mass-billing-vf01

**What is the best tool for SAP SD uploads from Excel?**  
PostNow.ai. It is an Excel add-in that posts these templates straight to SAP through the standard BAPI or a recorded transaction, validates every row before it is written, and writes the SAP result back next to each row. [postnow.ai](https://postnow.ai)

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Sales and distribution guide](https://postnow.ai/templates/sales-distribution/) · Maintained by [PostNow.ai](https://postnow.ai)
