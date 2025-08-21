# Column Masking in watsonx.data using IBM Knowledge Catalog (IKC)

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-watsonx.data-blue)](https://www.ibm.com/products/watsonx-data)
[![Documentation](https://img.shields.io/badge/Documentation-IBM%20Cloud-blue)](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration)

This guide explains how to implement column masking in watsonx.data using IBM Knowledge Catalog (IKC). Column masking is a crucial data protection feature that helps secure sensitive information while maintaining data utility for authorized users.

## Prerequisites

Before starting, ensure you have:
- Access to IBM Cloud
- A working watsonx.data environment
- IBM Knowledge Catalog (IKC) environment
- Service-to-service authorization configured between IKC and watsonx.data

## Documentation Sections

1. [Platform Connection and IKC Integration](docs/platform-connection.md)
   - Setting up watsonx.data connection
   - Configuring IKC integration
   - Connection parameters and authentication

2. [Metadata Import (MDI)](docs/metadata-import.md)
   - Creating and configuring MDI jobs
   - Importing assets and tables
   - Scheduling and monitoring imports

3. [Metadata Enrichment (MDE)](docs/metadata-enrichment.md)
   - Running data profiling
   - Automatic classification
   - Data quality analysis

4. [Projects](docs/projects.md)
   - Creating projects
   - Project configuration
   - Asset management

5. [Catalogs](docs/catalogs.md)
   - Creating and configuring catalogs
   - Publishing assets
   - Managing enforcement settings

6. [Rules and Policies](docs/rules-policies.md)
   - Creating masking rules
   - Policy configuration
   - Enforcement and verification

## Quick Navigation

| Section | Description |
|---------|-------------|
| [Platform Connection](docs/platform-connection.md) | Set up connections between watsonx.data and IKC |
| [MDI](docs/metadata-import.md) | Import metadata from your data sources |
| [MDE](docs/metadata-enrichment.md) | Enrich metadata with classifications and profiling |
| [Projects](docs/projects.md) | Manage your data projects |
| [Catalogs](docs/catalogs.md) | Organize and govern your data assets |
| [Rules & Policies](docs/rules-policies.md) | Configure data protection rules |

## Support

For more information and support, please refer to:
- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata)
- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.