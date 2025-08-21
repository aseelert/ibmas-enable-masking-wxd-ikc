---
layout: default
title: Home
nav_order: 1
---

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

## Implementation Flow

Follow these steps in order to set up data protection:

1. [Platform Connection and IKC Integration](docs/platform-connection.md)
   - Setting up watsonx.data connection
   - Configuring IKC integration
   - Connection parameters and authentication
   - Presto engine configuration

2. [Catalogs](docs/catalogs.md)
   - Creating and configuring catalogs
   - Enabling enforcement
   - Setting up audit logging
   - Managing access controls

3. [Projects](docs/projects.md)
   - Creating projects
   - Project configuration
   - Asset management
   - Collaboration settings

4. [Metadata Import (MDI)](docs/metadata-import.md)
   - Discovering data assets
   - Configuring import jobs
   - Scheduling and monitoring
   - Verification steps

5. [Metadata Enrichment (MDE)](docs/metadata-enrichment.md)
   - Running data profiling
   - Automatic classification
   - Business term assignment
   - Quality analysis

6. [Rules and Policies](docs/rules-policies.md)
   - Creating masking rules
   - Policy configuration
   - Enforcement setup
   - Testing and verification

## Quick Navigation

| Step | Purpose | Key Outcomes |
|------|----------|-------------|
| [1. Connection](docs/platform-connection.md) | Establish connectivity | Working connection between watsonx.data and IKC |
| [2. Catalogs](docs/catalogs.md) | Set up governance foundation | Enforced catalog ready for assets |
| [3. Projects](docs/projects.md) | Create working environment | Organized space for data work |
| [4. MDI](docs/metadata-import.md) | Discover data assets | Assets imported and cataloged |
| [5. MDE](docs/metadata-enrichment.md) | Enrich metadata | Classified and profiled data |
| [6. Rules](docs/rules-policies.md) | Implement protection | Active data masking |

## Implementation Checklist

- [ ] Connection established and tested
- [ ] Catalog created with enforcement enabled
- [ ] Project set up with proper settings
- [ ] Assets discovered through MDI
- [ ] Metadata enriched through MDE
- [ ] Protection rules created and tested
- [ ] Policies published and enforced

## Support

For more information and support, please refer to:
- [IBM watsonx.data Documentation](https://cloud.ibm.com/docs/watsonxdata)
- [IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.