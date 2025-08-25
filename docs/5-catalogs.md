# Catalogs

[![Component](https://img.shields.io/badge/Component-Catalogs-blue)](https://cloud.ibm.com/docs/data-catalog)
[![Governance](https://img.shields.io/badge/Governance-Data-green)](https://www.ibm.com/products/watsonx-data)

This guide explains how to create and manage catalogs for data governance and masking implementation.

## Creating a Catalog

1. Navigate to Catalogs:

<img width="309" height="430" alt="image" src="https://github.com/user-attachments/assets/90b01339-87b4-4301-9dbf-f15caff10071" />

2. Enable audit and enforce data protection rules:

<img width="1510" height="697" alt="image" src="https://github.com/user-attachments/assets/0a75283c-ccfe-4b60-b0e8-7900a1d1315e" />

## Publishing Assets

1. Select assets to publish from your project:

<img width="1804" height="614" alt="image" src="https://github.com/user-attachments/assets/860953b6-cad5-4c47-9c49-c74eae92fad1" />

2. **important:** Only published assets in the catalog will be affected by Rules

## Verification

Check the catalog to see all assets and connections that will be affected by data protection rules:

<img width="1777" height="837" alt="image" src="https://github.com/user-attachments/assets/e330fb0f-4570-491b-97dd-ab37a92d35ac" />

## Critical Settings

### Enforcement Configuration
- Enable **"Enforce data protection and data location rules"**
- Turn on **"Controls"** for asset metadata reporting
- Configure duplicate asset handling

### Audit Settings
- Enable audit logging
- Configure audit retention
- Set up monitoring

## Best Practices

- Regular catalog review
- Consistent naming conventions
- Proper access management
- Regular enforcement checks
- Documentation maintenance

## References

- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)
- [Data Governance Guide](https://cloud.ibm.com/docs/data-catalog?topic=data-catalog-governance)
