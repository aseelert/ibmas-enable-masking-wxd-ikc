# Platform Connection

## Step 2: Configure Connection

!!! info "Connection Details"
    === "Connection Screen"
        Navigate to the Connection Details screen
        ![Connection Details](https://github.com/user-attachments/assets/709ee2f3-4f9f-427a-88d1-423284b71f45)

    === "Engine Info"
        View Engine Information
        ![Engine Info](https://github.com/user-attachments/assets/6a30dde7-b1bb-44d1-aba1-ce62004980d1)

    === "Parameters"
        Configure Parameters
        ![Parameters](https://github.com/user-attachments/assets/0efd5e29-c842-4d2d-be36-13f551eea31a)

    ??? tip "Need Help?"
        If you need assistance:
        1. Check the [documentation](https://cloud.ibm.com/docs/watsonxdata)
        2. Contact [support](https://www.ibm.com/support/home)

## Connection Parameters

!!! info "Required Parameters"
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

## Connection String

```sql
presto://<engine-host>:<engine-port>
```

Required settings:
- SSL Mode: verify-full (recommended)
- Authentication: IAM
- Schema: default is 'ibmclusters'