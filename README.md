# Column Masking in watsonx.data using IBM Knowledge Catalog (IKC)

This guide explains how to implement column masking in watsonx.data using IBM Knowledge Catalog (IKC). Column masking is a crucial data protection feature that helps secure sensitive information while maintaining data utility for authorized users.


How to get connection information from watsonx.data Saas?

<img width="1410" height="378" alt="image" src="https://github.com/user-attachments/assets/709ee2f3-4f9f-427a-88d1-423284b71f45" />

<img width="385" height="356" alt="image" src="https://github.com/user-attachments/assets/6a30dde7-b1bb-44d1-aba1-ce62004980d1" />

<img width="1435" height="563" alt="image" src="https://github.com/user-attachments/assets/0efd5e29-c842-4d2d-be36-13f551eea31a" />

or

export JSON snipped (right above)
<img width="1484" height="669" alt="image" src="https://github.com/user-attachments/assets/768ddfe1-7625-40b2-910e-4a8edec83258" />


The user is normally like this:
Username: ibmlhapikey_<name>@<domain>
Password: API key (access: https://cloud.ibm.com/iam/apikeys from IAM)


### add watsonx.data connection
go to https://eu-de.dataplatform.cloud.ibm.com/data/connections/?context=cpdaas
<img width="1479" height="627" alt="image" src="https://github.com/user-attachments/assets/b909c00e-0158-407c-9aff-16e1dd267d51" />

<img width="1498" height="777" alt="image" src="https://github.com/user-attachments/assets/d99fb673-3afa-4a17-bdc8-302e80016188" />

<img width="1502" height="465" alt="image" src="https://github.com/user-attachments/assets/6d1501df-f41c-435d-9ef3-170003dda192" />

create a project
https://eu-de.dataplatform.cloud.ibm.com/projects/new-project?context=cpdaas

<img width="1493" height="1086" alt="image" src="https://github.com/user-attachments/assets/246a4448-48a8-4a7c-9d8e-06f70aa8dd10" />

now go into the project and create a new asset
<img width="1476" height="280" alt="image" src="https://github.com/user-attachments/assets/56db5f29-33d9-476e-9f0b-95ad34931bb6" />

select Meta data import (MDI)
<img width="1345" height="500" alt="image" src="https://github.com/user-attachments/assets/f90e40d8-58c5-4ccd-945b-a5172ef5f1b9" />
<img width="1304" height="534" alt="image" src="https://github.com/user-attachments/assets/4d86ad65-dcf2-4429-aec7-b3134f46647f" />
<img width="1361" height="430" alt="image" src="https://github.com/user-attachments/assets/4695bf8c-efa2-4436-88ba-ddca62a6e422" />
select connection
<img width="1383" height="483" alt="image" src="https://github.com/user-attachments/assets/28952ab3-accf-4bf8-bee4-80eb234f23a3" />
<img width="1245" height="294" alt="image" src="https://github.com/user-attachments/assets/06bc3bd3-d0ef-4bee-a065-8ef339efaac2" />
define a scope
<img width="1352" height="618" alt="image" src="https://github.com/user-attachments/assets/01675d18-e22c-4861-80ae-d0f0f4d11ce2" />
select catalog/schema or selected tables
<img width="1257" height="560" alt="image" src="https://github.com/user-attachments/assets/07fe6d6c-f283-42c9-be57-46bc07914f33" />
schedule a job
<img width="1331" height="499" alt="image" src="https://github.com/user-attachments/assets/76529cc8-3e9e-4eae-abb5-13deb1194019" />
<img width="1375" height="603" alt="image" src="https://github.com/user-attachments/assets/51470499-71fa-4f78-9d7b-7a8eda978875" />
<img width="1354" height="1009" alt="image" src="https://github.com/user-attachments/assets/d8e46ca2-5153-4ed3-b5b5-e5495e4d2daf" />

After MDI import you should see all objects (tables)
<img width="1484" height="636" alt="image" src="https://github.com/user-attachments/assets/9c7cf514-5b36-40a7-9a80-68ba4ed1f641" />

now check the tables and maybe check profiles
<img width="2102" height="840" alt="image" src="https://github.com/user-attachments/assets/cfcdca55-0899-4a56-8b09-1a873fc2ef41" />
<img width="2098" height="736" alt="image" src="https://github.com/user-attachments/assets/b64930ab-3a75-4067-bba2-3b3e05174958" />
<img width="1768" height="919" alt="image" src="https://github.com/user-attachments/assets/4b5fda51-179b-4ef1-9a7e-d8daabefb09d" />

now execute a Meta data enrichment to assign dataclasses and business terms automatically
again add a new asset in the project (select MDE)
<img width="1978" height="608" alt="image" src="https://github.com/user-attachments/assets/35a7a949-c235-4ac4-9df4-07420892fb7b" />
<img width="1842" height="1000" alt="image" src="https://github.com/user-attachments/assets/d53f2052-2421-4391-a368-e581b0296f80" />
<img width="1317" height="891" alt="image" src="https://github.com/user-attachments/assets/013eeb68-5289-4580-b204-5a4b0e59a78e" />
select The data assets or assets from MDI 
<img width="1274" height="950" alt="image" src="https://github.com/user-attachments/assets/1094934a-543e-45f5-bf94-67837a80da02" />





## Prerequisites

Before starting, ensure you have:
- Access to IBM Cloud
- A working watsonx.data environment
- IBM Knowledge Catalog (IKC) environment
- Service-to-service authorization configured between IKC and watsonx.data

## Step-by-Step Implementation

### 1. Create a Project and Catalog

1. Log into IBM Cloud Pak for Data
2. Create a new project:
   - Navigate to Projects
   - Click "New project"
   - Select "Create an empty project"
   - Fill in project details
   - Enable "Enforce data protection rules" for the project

3. Create a new catalog:
   - Navigate to "Catalogs" > "View all catalogs"
   - Click "New catalog"
   - Fill in required details:
     - Name and description
     - Select object storage instance
     - **Important:** Enable "Enforce data protection and data location rules"
     - Turn on "Controls" for asset metadata reporting
     - Configure duplicate asset handling
   - Click "Create"

### 2. Set Up watsonx.data Connection

1. In your catalog:
   - Go to "Add to catalog" > "Connection"
   - Search for "IBM watsonx.data"
   - Select it as your connection type

2. Configure the connection with:
   ```
   - Name and Description
   - Hostname/IP address (watsonx.data URL)
   - Port number
   - Instance ID
   - Instance name
   - CRN (Cloud Resource Name)
   - Username (ibmlhapikey_<EMAIL_ID>)
   - IAM API key
   - SSL Certificate
   - Engine hostname
   - Engine ID
   - Engine port
   ```

3. Test the connection and create it

### 3. Import Metadata Assets

1. Navigate to "Add to catalog" > "Connected assets"
2. Select your watsonx.data connection
3. Choose the assets (tables/views) you want to import
4. Click "Add" to import the assets to IKC

### 4. Run Data Profiling

1. Select the imported asset
2. Click on "Profile" tab
3. Select "Run data profiling"
4. Wait for profiling to complete
   - This step enriches metadata
   - Identifies data classes
   - Helps in automatic classification

### 5. Create Masking Rules

1. Navigate to "Governance" > "Rules"
2. Click "Add rule"
3. Configure the masking rule:
   ```
   - Select rule type: "Mask data"
   - Define conditions:
     - Column name equals "address"
     - OR Data class equals "Address"
   - Set masking format (e.g., "XXXX")
   ```
4. Save the rule

### 6. Create and Apply Policy

1. Go to "Governance" > "Policies"
2. Create new policy:
   - Name the policy
   - Add the masking rule
   - Set scope (catalog/project)
   - Define access roles
3. Activate the policy

### 7. Publish Assets to Catalog

1. Select your assets
2. Click "Publish" or "Add to catalog"
3. Choose your enforced catalog
4. Confirm publication

### 8. Verify Masking

1. Log in as a non-owner user
2. Query the asset in watsonx.data
3. Verify that the address column is masked
4. Test with owner account to confirm unmasked view

## Important Notes

- Masking only works when all steps are completed in order
- The catalog must have enforcement enabled
- Both connection and assets need to be in the enforced catalog
- Rules must match either column names or data classes exactly
- Owner accounts can still see unmasked data
- Supported data types include:
  - Varchar
  - Bigint
  - Boolean
  - Date
  - Double
  - Integer
  - Smallint
  - Timestamp
  - Tinyint
  - Decimal

## Troubleshooting

If masking is not working:
1. Verify catalog enforcement is enabled
2. Check rule conditions match exactly
3. Confirm policy is active
4. Ensure assets are published to enforced catalog
5. Verify user permissions
6. Check data type compatibility

## References

- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)
