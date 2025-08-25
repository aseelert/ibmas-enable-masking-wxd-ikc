# Metadata Import (MDI)

[![Process](https://img.shields.io/badge/Process-MDI-green)](https://cloud.ibm.com/docs/data-catalog)
[![Type](https://img.shields.io/badge/Type-Metadata-blue)](https://www.ibm.com/products/watsonx-data)

This guide explains how to perform Metadata Import (MDI) to discover and catalog your data assets from watsonx.data into IBM Knowledge Catalog (IKC).

## Understanding Metadata Import

### What is MDI?
Metadata Import (MDI) is a discovery process that:
- Scans your watsonx.data sources
- Captures technical metadata about your data assets
- Creates asset entries in IBM Knowledge Catalog
- Enables data governance and protection features

### Key Benefits
1. **Automated Discovery**: Automatically finds and catalogs data assets
2. **Governance Foundation**: Creates the basis for implementing data protection
3. **Time Saving**: Eliminates manual asset registration
4. **Consistency**: Ensures uniform metadata capture
5. **Compliance Support**: Helps track and protect sensitive data

### watsonx.data Asset Types
MDI can discover these types of assets in watsonx.data:
- Catalogs
- Schemas
- Tables (including Hive, Iceberg, Delta Lake)
- Views
- Columns and their data types
- Primary/Foreign key relationships
- Access permissions

## Setting Up MDI

1. Select Meta data import (MDI):

<img width="1345" height="500" alt="image" src="https://github.com/user-attachments/assets/f90e40d8-58c5-4ccd-945b-a5172ef5f1b9" />

<img width="1304" height="534" alt="image" src="https://github.com/user-attachments/assets/4d86ad65-dcf2-4429-aec7-b3134f46647f" />

<img width="1361" height="430" alt="image" src="https://github.com/user-attachments/assets/4695bf8c-efa2-4436-88ba-ddca62a6e422" />

### Discovery Process
The MDI process follows these steps:
1. Connects to watsonx.data source
2. Scans for available assets
3. Extracts technical metadata
4. Creates catalog entries
5. Establishes relationships

## Select Connection

1. Choose your connection:

<img width="1383" height="483" alt="image" src="https://github.com/user-attachments/assets/28952ab3-accf-4bf8-bee4-80eb234f23a3" />

<img width="1245" height="294" alt="image" src="https://github.com/user-attachments/assets/06bc3bd3-d0ef-4bee-a065-8ef339efaac2" />

### Connection Requirements
For successful MDI:
- Valid watsonx.data connection
- Appropriate access permissions
- Network connectivity
- Required SSL certificates (if applicable)

## Define Scope

1. Configure scope settings:

<img width="1352" height="618" alt="image" src="https://github.com/user-attachments/assets/01675d18-e22c-4861-80ae-d0f0f4d11ce2" />

2. Select catalog/schema or tables:

<img width="1257" height="560" alt="image" src="https://github.com/user-attachments/assets/07fe6d6c-f283-42c9-be57-46bc07914f33" />

### Scope Options
You can discover:
- Entire catalogs
- Specific schemas
- Selected tables
- Views and materialized views
- Column-level metadata

## Schedule Import Job

1. Configure job schedule:

<img width="1331" height="499" alt="image" src="https://github.com/user-attachments/assets/76529cc8-3e9e-4eae-abb5-13deb1194019" />

<img width="1375" height="603" alt="image" src="https://github.com/user-attachments/assets/51470499-71fa-4f78-9d7b-7a8eda978875" />

<img width="1354" height="1009" alt="image" src="https://github.com/user-attachments/assets/d8e46ca2-5153-4ed3-b5b5-e5495e4d2daf" />

### Scheduling Options
- One-time import
- Recurring schedule
- Custom intervals
- Time zone selection

## Verification

After MDI import, check tables and profiles:

<img width="2102" height="840" alt="image" src="https://github.com/user-attachments/assets/cfcdca55-0899-4a56-8b09-1a873fc2ef41" />

<img width="2098" height="736" alt="image" src="https://github.com/user-attachments/assets/b64930ab-3a75-4067-bba2-3b3e05174958" />

<img width="1768" height="919" alt="image" src="https://github.com/user-attachments/assets/4b5fda51-179b-4ef1-9a7e-d8daabefb09d" />

### Verification Steps
1. **Check Asset Discovery**:
   - Verify all selected assets are imported
   - Confirm metadata accuracy
   - Check relationship mappings

2. **Review Technical Metadata**:
   - Table and column names
   - Data types
   - Key relationships
   - Access patterns

3. **Validate Catalog Entries**:
   - Asset visibility
   - Metadata completeness
   - Classification readiness


## Next Steps

After successful MDI:
1. Review discovered assets
2. Plan metadata enrichment (MDE)
3. Configure governance rules
4. Set up data protection

## References

- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)
- [watsonx.data Integration Guide](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)
- [Metadata Discovery Best Practices](https://www.ibm.com/docs/en/cloud-paks/cp-data/4.6.x?topic=catalog-discovering-data-assets)
