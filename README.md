# Column Masking in watsonx.data using IBM Knowledge Catalog (IKC)

This guide explains how to implement column masking in watsonx.data using IBM Knowledge Catalog (IKC). Column masking is a crucial data protection feature that helps secure sensitive information while maintaining data utility for authorized users.

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
