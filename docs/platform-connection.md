# Platform Connection and IKC Integration

[![Integration](https://img.shields.io/badge/Integration-IKC-blue)](https://cloud.ibm.com/docs/data-catalog)
[![Service](https://img.shields.io/badge/Service-watsonx.data-blue)](https://www.ibm.com/products/watsonx-data)

This guide explains how to set up the connection between watsonx.data and IBM Knowledge Catalog (IKC).

## Getting Connection Information

### From watsonx.data SaaS

<img width="1410" height="378" alt="image" src="https://github.com/user-attachments/assets/709ee2f3-4f9f-427a-88d1-423284b71f45" />

<img width="385" height="356" alt="image" src="https://github.com/user-attachments/assets/6a30dde7-b1bb-44d1-aba1-ce62004980d1" />

<img width="1435" height="563" alt="image" src="https://github.com/user-attachments/assets/0efd5e29-c842-4d2d-be36-13f551eea31a" />

Or export JSON snippet:

<img width="1484" height="669" alt="image" src="https://github.com/user-attachments/assets/768ddfe1-7625-40b2-910e-4a8edec83258" />

The user format is:
- Username: `ibmlhapikey_<n>@<domain>`
- Password: API key (accessible at https://cloud.ibm.com/iam/apikeys from IAM)

## Adding watsonx.data Connection

1. Go to [Platform Connections](https://eu-de.dataplatform.cloud.ibm.com/data/connections/?context=cpdaas)

<img width="1479" height="627" alt="image" src="https://github.com/user-attachments/assets/b909c00e-0158-407c-9aff-16e1dd267d51" />

<img width="1498" height="777" alt="image" src="https://github.com/user-attachments/assets/d99fb673-3afa-4a17-bdc8-302e80016188" />

<img width="1502" height="465" alt="image" src="https://github.com/user-attachments/assets/6d1501df-f41c-435d-9ef3-170003dda192" />

## IKC Integration Setup

1. In watsonx.data, go to Access Control

<img width="252" height="295" alt="image" src="https://github.com/user-attachments/assets/3e70d2f8-13ae-4e78-a211-d96380b883be" />

2. Navigate to Integrations

<img width="697" height="264" alt="image" src="https://github.com/user-attachments/assets/d8aa3214-4b41-424c-8dfa-0dcc99222e50" />

3. Add the IKC endpoint:

<img width="670" height="378" alt="image" src="https://github.com/user-attachments/assets/8aa77dd3-c772-4a2b-a5af-778f50c1fc2b" />

- For EU (Frankfurt): `https://api.eu-de.dataplatform.cloud.ibm.com`
- Select the catalogs you want to integrate

## References

- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)
- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)