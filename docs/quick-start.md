# Quick Start Guide

## Setup Checklist

- [x] Access to IBM Cloud
- [x] watsonx.data environment
- [x] IBM Knowledge Catalog (IKC)
- [ ] Service-to-service authorization

## Implementation Steps

=== "1. Platform Connection"
    !!! tip "First Step"
        Configure your watsonx.data connection with IKC.

    1. Access Platform Connections
    2. Create new connection
    3. Configure parameters

    [Detailed Guide :octicons-arrow-right-24:](platform-connection.md){ .md-button }

=== "2. Metadata Import"
    !!! example "Next Step"
        Import your data assets into IKC.

    1. Set up MDI job
    2. Select assets
    3. Run import

    [Learn More :octicons-arrow-right-24:](metadata-import.md){ .md-button }

=== "3. Enrichment"
    !!! note "Enhancement"
        Enrich your metadata with classifications.

    1. Run profiling
    2. Apply classifications
    3. Verify results

    [Full Details :octicons-arrow-right-24:](metadata-enrichment.md){ .md-button }

=== "4. Rules Setup"
    !!! success "Final Step"
        Configure masking rules and policies.

    1. Create rules
    2. Set policies
    3. Test masking

    [Configuration Guide :octicons-arrow-right-24:](rules-policies.md){ .md-button }

## Architecture Overview

``` mermaid
graph LR
    A[watsonx.data] -->|Connect| B[IKC]
    B -->|Import| C[Metadata]
    C -->|Enrich| D[Classifications]
    D -->|Apply| E[Masking Rules]
    style A fill:#f9f9f9,stroke:#333,stroke-width:2px
    style B fill:#f9f9f9,stroke:#333,stroke-width:2px
    style C fill:#f9f9f9,stroke:#333,stroke-width:2px
    style D fill:#f9f9f9,stroke:#333,stroke-width:2px
    style E fill:#f9f9f9,stroke:#333,stroke-width:2px
```

## Key Concepts

| Term | Description |
|------|-------------|
| MDI | Metadata Import - Process of importing data assets |
| MDE | Metadata Enrichment - Adding classifications and tags |
| IKC | IBM Knowledge Catalog - Central metadata repository |

## Command Reference

```sql title="Connection String" linenums="1"
presto://<engine-host>:<engine-port>
```

```bash title="SSL Certificate" linenums="1"
# Example SSL certificate path
/path/to/ssl/certificate.pem
```

## Common Issues

??? question "Connection Failed"
    Check your network connectivity and credentials.

??? question "Import Error"
    Verify your asset permissions and connection status.

??? question "Classification Issues"
    Ensure proper data profiling has been completed.

## Next Steps

1. [Configure Platform Connection](platform-connection.md)
2. [Set up Metadata Import](metadata-import.md)
3. [Enrich Metadata](metadata-enrichment.md)
4. [Configure Rules](rules-policies.md)

!!! tip "Need Help?"
    Visit our [FAQ](faq.md) or check the [Glossary](glossary.md) for term definitions.
