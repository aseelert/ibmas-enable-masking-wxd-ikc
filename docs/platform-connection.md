# Platform Connection and IKC Integration

[![Integration](https://img.shields.io/badge/Integration-IKC-blue)](https://cloud.ibm.com/docs/data-catalog)
[![Service](https://img.shields.io/badge/Service-watsonx.data-blue)](https://www.ibm.com/products/watsonx-data)

This guide explains how to set up the connection between watsonx.data and IBM Knowledge Catalog (IKC).

## Getting Connection Information

### From watsonx.data SaaS

To find your connection information, follow these steps:

1. Log in to your IBM Cloud account
2. Navigate to watsonx.data instance
3. In the left navigation menu, click on "Connection Details"
4. You'll see the main connection information screen:

<img width="1410" height="378" alt="image" src="https://github.com/user-attachments/assets/709ee2f3-4f9f-427a-88d1-423284b71f45" />

5. Click on "Connection Details" to view specific engine information:

<img width="385" height="356" alt="image" src="https://github.com/user-attachments/assets/6a30dde7-b1bb-44d1-aba1-ce62004980d1" />

6. The connection details page shows all necessary parameters:

<img width="1435" height="563" alt="image" src="https://github.com/user-attachments/assets/0efd5e29-c842-4d2d-be36-13f551eea31a" />

### Exporting Connection Details

You can also export the connection details as a JSON snippet:

1. Click on the "Export" button in the top right
2. Select "JSON" format:

<img width="1484" height="669" alt="image" src="https://github.com/user-attachments/assets/768ddfe1-7625-40b2-910e-4a8edec83258" />

### Understanding Connection Parameters

The connection requires several key pieces of information:

1. **User Credentials**:
   - Username format: `ibmlhapikey_<n>@<domain>`
   - Password: API key from IBM Cloud IAM
   - API Key Location: https://cloud.ibm.com/iam/apikeys

2. **Instance Details**:
   - Instance CRN (Cloud Resource Name)
   - Instance ID
   - Instance Name
   - Host/Endpoint URL

3. **Engine Parameters**:
   - Engine ID
   - Engine Host
   - Engine Port
   - SSL Certificate

## Connecting to Dedicated Presto Engines

### Engine Types

watsonx.data supports different types of Presto engines:
1. **Shared Engine**: Default engine shared among instances
2. **Dedicated Engine**: Exclusive engine for your instance
3. **Serverless Engine**: Auto-scaling engine (if available in your region)

### Dedicated Engine Connection

To connect to a dedicated Presto engine:

1. **Find Engine Details**:
   - Go to watsonx.data dashboard
   - Click on "Engines" in the left navigation
   - Select your dedicated engine
   - Note down:
     - Engine Host
     - Engine Port
     - Engine ID
     - SSL settings

2. **SSL Configuration**:
   - Download the SSL certificate if required
   - Place it in a secure location
   - Use the certificate path in your connection

3. **Connection String Format**:
   ```
   presto://<engine-host>:<engine-port>
   ```

4. **Additional Parameters**:
   - SSL Mode: verify-full (recommended)
   - Authentication: IAM
   - Schema: default is 'ibmclusters'

## Adding watsonx.data Connection

1. Go to [Platform Connections](https://eu-de.dataplatform.cloud.ibm.com/data/connections/?context=cpdaas)

<img width="1479" height="627" alt="image" src="https://github.com/user-attachments/assets/b909c00e-0158-407c-9aff-16e1dd267d51" />

2. Click "New Connection" and select "IBM watsonx.data":

<img width="1498" height="777" alt="image" src="https://github.com/user-attachments/assets/d99fb673-3afa-4a17-bdc8-302e80016188" />

3. Fill in the connection details:

<img width="1502" height="465" alt="image" src="https://github.com/user-attachments/assets/6d1501df-f41c-435d-9ef3-170003dda192" />

## IKC Integration Setup

1. In watsonx.data, go to Access Control:

<img width="252" height="295" alt="image" src="https://github.com/user-attachments/assets/3e70d2f8-13ae-4e78-a211-d96380b883be" />

2. Navigate to Integrations:

<img width="697" height="264" alt="image" src="https://github.com/user-attachments/assets/d8aa3214-4b41-424c-8dfa-0dcc99222e50" />

3. Add the IKC endpoint:

<img width="670" height="378" alt="image" src="https://github.com/user-attachments/assets/8aa77dd3-c772-4a2b-a5af-778f50c1fc2b" />

- For EU (Frankfurt): `https://api.eu-de.dataplatform.cloud.ibm.com`
- Select the catalogs you want to integrate

## Troubleshooting Connection Issues

Common issues and solutions:

1. **Connection Timeout**:
   - Check network connectivity
   - Verify engine status
   - Confirm port accessibility

2. **Authentication Failures**:
   - Verify API key is active
   - Check username format
   - Confirm IAM permissions

3. **SSL/TLS Issues**:
   - Verify certificate path
   - Check certificate expiration
   - Confirm SSL mode settings

4. **Engine Connectivity**:
   - Ensure engine is running
   - Check resource allocation
   - Verify network rules/firewalls

## References

- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)
- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)
- [Presto Connection Guide](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-presto-connection)