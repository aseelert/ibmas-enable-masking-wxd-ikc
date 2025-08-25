# Rules and Policies

[![Component](https://img.shields.io/badge/Component-Rules%20%26%20Policies-blue)](https://cloud.ibm.com/docs/data-catalog)
[![Security](https://img.shields.io/badge/Security-Data%20Protection-red)](https://www.ibm.com/products/watsonx-data)

This guide explains how to create and manage data protection rules and policies for implementing column masking.

## Creating Protection Rules

1. Navigate to Rules:

<img width="323" height="680" alt="image" src="https://github.com/user-attachments/assets/5fdb0147-28cb-484c-9ee4-553d5187327a" />

2. Add a new protection rule:

<img width="1295" height="226" alt="image" src="https://github.com/user-attachments/assets/4a19dbfd-28a2-4f7a-a8df-b04e42091b2b" />

<img width="1222" height="1038" alt="image" src="https://github.com/user-attachments/assets/6dd25675-1bc5-4278-9354-87ce3fd6e03d" />

3. Configure rule (this example uses column address and redacts it with X):

<img width="1710" height="1062" alt="image" src="https://github.com/user-attachments/assets/685dad90-9ebe-4802-b281-d73d675fb75b" />

<img width="1727" height="1073" alt="image" src="https://github.com/user-attachments/assets/e7aa479c-198f-4195-ab5e-31239683b80e" />

## Creating Policies

1. Navigate to Policies:

<img width="302" height="668" alt="image" src="https://github.com/user-attachments/assets/aa800d05-8e20-49d9-95ca-7a7a13f82bbd" />

2. Add a new policy and choose from categories:

<img width="1743" height="1073" alt="image" src="https://github.com/user-attachments/assets/09468e4f-1667-48cb-97dc-61b1f36ea0ec" />

3. Add protection rule:

<img width="1764" height="1024" alt="image" src="https://github.com/user-attachments/assets/89bdb6ea-f6d2-4e72-afba-c32646392ff9" />

<img width="1734" height="323" alt="image" src="https://github.com/user-attachments/assets/c88229a0-aec3-4d2b-89a5-bb20c8da5b39" />

4. Publish the policy:

<img width="1728" height="211" alt="image" src="https://github.com/user-attachments/assets/db32c99a-ac3c-4ffe-8c3c-b8b44f1a6065" />

## Supported Data Types

The following data types can be masked:
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

### Common Issues
1. Masking not working:
   - Check catalog enforcement
   - Verify rule conditions
   - Confirm policy status
   - Check asset publication
   - Verify permissions
   - Validate data types

## References

- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)
- [Data Protection Guide](https://cloud.ibm.com/docs/data-catalog?topic=data-catalog-protection)
