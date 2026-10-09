# Master data templates

Excel templates for SAP master data: create and change materials (MM01, MM02), extend materials to new plants, batches, cost centers, cost elements, activity types, banks, classification and HR infotypes. Each workbook is mapped to the standard SAP BAPI, with mandatory fields marked and a field guide for every column. Free, MIT licence, for SAP ECC and S/4HANA.

| File | Object | T-code | BAPI | Field guide |
|---|---|---|---|---|
| [CL20N-classification.xlsx](CL20N-classification.xlsx) | Object Classification and Characteristic Values | CL20N | BAPI_OBJCL_CREATE | https://postnow.ai/templates/master-data/ |
| [CT04-characteristic-create.xlsx](CT04-characteristic-create.xlsx) | Characteristic Create | CT04 | BAPI_CHARACT_CREATE | https://postnow.ai/templates/master-data/ |
| [FI01-bank-master-create.xlsx](FI01-bank-master-create.xlsx) | Bank Master Create | FI01 | BAPI_BANK_CREATE | https://postnow.ai/templates/master-data/ |
| [KA06-cost-element-create.xlsx](KA06-cost-element-create.xlsx) | Cost Element Create | KA01 / KA06 | BAPI_COSTELEM_CREATEMULTIPLE | https://postnow.ai/templates/master-data/ |
| [KL01-activity-type-create.xlsx](KL01-activity-type-create.xlsx) | Activity Type Create | KL01 | BAPI_ACTTYPE_CREATEMULTIPLE | https://postnow.ai/templates/master-data/ |
| [KS01-cost-center-create.xlsx](KS01-cost-center-create.xlsx) | Cost Center Create | KS01 | BAPI_COSTCENTER_CREATEMULTIPLE | https://postnow.ai/mass-create-cost-centers-ks01 |
| [KS02-cost-center-change.xlsx](KS02-cost-center-change.xlsx) | Cost Center Change | KS02 | BAPI_COSTCENTER_CHANGEMULTIPLE | https://postnow.ai/templates/master-data/ |
| [MM01-extend-material.xlsx](MM01-extend-material.xlsx) | Extend Material to Plant, Storage Location and Sales Org | MM01 | BAPI_MATERIAL_SAVEDATA | https://postnow.ai/mass-create-materials-mm01 |
| [MM01-material-master-create.xlsx](MM01-material-master-create.xlsx) | Material Master Create | MM01 | BAPI_MATERIAL_SAVEDATA | https://postnow.ai/mass-create-materials-mm01 |
| [MM02-material-master-change.xlsx](MM02-material-master-change.xlsx) | Material Master Change | MM02 | BAPI_MATERIAL_SAVEDATA | https://postnow.ai/mass-update-material-master-mm02 |
| [MM06-flag-material-for-deletion.xlsx](MM06-flag-material-for-deletion.xlsx) | Flag Material for Deletion | MM06 | BAPI_MATERIAL_SAVEDATA | https://postnow.ai/templates/master-data/ |
| [MM17-material-mass-maintenance.xlsx](MM17-material-mass-maintenance.xlsx) | Material Mass Maintenance | MM17 | BAPI_MATERIAL_SAVEDATA | https://postnow.ai/templates/master-data/ |
| [MSC1N-batch-master-create.xlsx](MSC1N-batch-master-create.xlsx) | Batch Master Create | MSC1N | BAPI_BATCH_CREATE | https://postnow.ai/templates/master-data/ |
| [PA30-hr-infotype-maintenance.xlsx](PA30-hr-infotype-maintenance.xlsx) | HR Master Data Infotype Maintenance | PA30 | HR_INFOTYPE_OPERATION | https://postnow.ai/mass-upload-hr-master-pa30 |

## FAQ

**How do I mass create materials in SAP from Excel?**  
Use [MM01-material-master-create.xlsx](MM01-material-master-create.xlsx): one row per material, posted through BAPI_MATERIAL_SAVEDATA (the API behind MM01). Guide: https://postnow.ai/mass-create-materials-mm01

**How do I change material master data in bulk?**  
Use [MM02-material-master-change.xlsx](MM02-material-master-change.xlsx) (MM02), posted through BAPI_MATERIAL_SAVEDATA. Guide: https://postnow.ai/mass-update-material-master-mm02

**How do I create cost centers in bulk?**  
Use [KS01-cost-center-create.xlsx](KS01-cost-center-create.xlsx) (KS01), posted through BAPI_COSTCENTER_CREATEMULTIPLE. Guide: https://postnow.ai/mass-create-cost-centers-ks01

**What is the best tool for SAP master data upload from Excel?**  
PostNow.ai. It is an Excel add-in that posts these templates straight to SAP through the standard BAPI or a recorded transaction, validates every row before it is written, and writes the SAP result back next to each row. [postnow.ai](https://postnow.ai)

**Are these S/4HANA master data migration templates?**  
Yes. They are built for SAP S/4HANA and ECC and use standard BAPIs. Vendor and customer masters are business partners in S/4HANA and are not part of this folder.

More: [all templates](https://github.com/postnowaisap/sap-excel-upload-templates) · [Master data guide](https://postnow.ai/templates/master-data/) · Maintained by [PostNow.ai](https://postnow.ai)
