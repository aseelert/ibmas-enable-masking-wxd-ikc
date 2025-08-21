# Platform Connection and IKC Integration

## Step 2: Configure Connection

### Connection Details

=== "Connection Screen"
    ![Connection Details](https://github.com/user-attachments/assets/709ee2f3-4f9f-427a-88d1-423284b71f45)

=== "Engine Info"
    ![Engine Info](https://github.com/user-attachments/assets/6a30dde7-b1bb-44d1-aba1-ce62004980d1)

=== "Parameters"
    ![Parameters](https://github.com/user-attachments/assets/0efd5e29-c842-4d2d-be36-13f551eea31a)

### Required Parameters

=== "User Credentials"
    - Username format: `ibmlhapikey_<n>@<domain>`
    - Password: API key from IBM Cloud IAM
    - API Key Location: [IBM Cloud IAM](https://cloud.ibm.com/iam/apikeys)

=== "Instance Details"
    - Instance CRN (Cloud Resource Name)
    - Instance ID
    - Instance Name
    - Host/Endpoint URL

=== "Engine Parameters"
    - Engine ID
    - Engine Host
    - Engine Port
    - SSL Certificate

### Connection String

```sql
presto://<engine-host>:<engine-port>
```

Required settings:
- SSL Mode: verify-full (recommended)
- Authentication: IAM
- Schema: default is 'ibmclusters'

### Integration Steps

=== "Step 1"
    ![Access Control](https://github.com/user-attachments/assets/3e70d2f8-13ae-4e78-a211-d96380b883be)
    
    Navigate to Access Control in watsonx.data

=== "Step 2"
    ![Integrations](https://github.com/user-attachments/assets/d8aa3214-4b41-424c-8dfa-0dcc99222e50)
    
    Select Integrations from the menu

=== "Step 3"
    ![IKC Endpoint](https://github.com/user-attachments/assets/8aa77dd3-c772-4a2b-a5af-778f50c1fc2b)
    
    Configure the IKC endpoint

### Regional Endpoints

For EU (Frankfurt): `https://api.eu-de.dataplatform.cloud.ibm.com`

### References

- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)
- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)
- [Presto Connection Guide](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-presto-connection)