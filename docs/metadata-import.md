# Metadata Import (MDI)

This guide explains how to perform Metadata Import (MDI) to discover and catalog your data assets from watsonx.data into IBM Knowledge Catalog (IKC).

## Understanding Metadata Import

### What is MDI?

!!! abstract "MDI Overview"
    Metadata Import (MDI) is a powerful discovery process that automatically catalogs and organizes your data assets.

<div class="grid cards" markdown>

-   :material-database-search:{ .lg .middle } __Asset Discovery__

    ---

    Automatically scans and identifies data assets in watsonx.data
    
    [:octicons-arrow-right-24: Learn more](#watsonxdata-asset-types)

-   :material-database-import:{ .lg .middle } __Metadata Capture__

    ---
    
    Extracts and records technical metadata about your assets
    
    [:octicons-arrow-right-24: See details](#review-technical-metadata)

-   :material-book-lock:{ .lg .middle } __Governance__

    ---

    Enables data protection and governance features
    
    [:octicons-arrow-right-24: Explore governance](#next-steps)

-   :material-clock-fast:{ .lg .middle } __Automation__

    ---

    Saves time through automated asset registration
    
    [:octicons-arrow-right-24: Setup guide](#setting-up-mdi)

</div>

### Key Benefits

<div class="grid" markdown>

=== ":material-robot: Automated Discovery"
    Automatically finds and catalogs data assets, eliminating manual work
    
=== ":material-shield-lock: Governance"
    Creates the foundation for implementing data protection
    
=== ":material-clock-check: Time Saving"
    Eliminates manual asset registration and reduces errors
    
=== ":material-check-all: Consistency"
    Ensures uniform metadata capture across all assets
    
=== ":material-gavel: Compliance"
    Helps track and protect sensitive data effectively

</div>

### watsonx.data Asset Types

!!! example "Discoverable Assets"
    MDI can discover these types of assets in watsonx.data:

    === "Data Structures"
        - [x] Catalogs
        - [x] Schemas
        - [x] Tables (Hive, Iceberg, Delta Lake)
        - [x] Views

    === "Metadata"
        - [x] Columns and data types
        - [x] Primary/Foreign key relationships
        - [x] Access permissions

## Setting Up MDI

### Step 1: Launch MDI

!!! tip "Getting Started"
    Follow these steps to begin your metadata import journey:

    1. Navigate to the MDI section
    2. Select "New Import"
    3. Choose your source

=== "Select MDI"
    ![MDI Selection](https://github.com/user-attachments/assets/f90e40d8-58c5-4ccd-945b-a5172ef5f1b9)

=== "Configure Import"
    ![Import Configuration](https://github.com/user-attachments/assets/4d86ad65-dcf2-4429-aec7-b3134f46647f)

=== "Review Settings"
    ![Settings Review](https://github.com/user-attachments/assets/4695bf8c-efa2-4436-88ba-ddca62a6e422)

### Step 2: Discovery Process

```mermaid
graph LR
    A[Connect] -->|Establish Connection| B[Scan]
    B -->|Find Assets| C[Extract]
    C -->|Get Metadata| D[Create]
    D -->|Catalog Entries| E[Link]
    E -->|Build Relationships| F[Complete]
    style A fill:#b2d8d8
    style B fill:#b2d8d8
    style C fill:#b2d8d8
    style D fill:#b2d8d8
    style E fill:#b2d8d8
    style F fill:#b2d8d8
```

## Connection Setup

### Select Your Connection

!!! note "Connection Setup"
    Choose and configure your watsonx.data connection:

=== "Connection Selection"
    ![Select Connection](https://github.com/user-attachments/assets/28952ab3-accf-4bf8-bee4-80eb234f23a3)

=== "Connection Details"
    ![Connection Details](https://github.com/user-attachments/assets/06bc3bd3-d0ef-4bee-a065-8ef339efaac2)

### Connection Requirements

!!! warning "Prerequisites"
    Ensure you have all required components for successful MDI:

    - [x] Valid watsonx.data connection
    - [x] Appropriate access permissions
    - [x] Network connectivity
    - [x] Required SSL certificates (if applicable)

## Define Import Scope

### Configure Scope

!!! tip "Scope Configuration"
    Define what you want to discover:

=== "Scope Settings"
    ![Scope Configuration](https://github.com/user-attachments/assets/01675d18-e22c-4861-80ae-d0f0f4d11ce2)

=== "Asset Selection"
    ![Select Assets](https://github.com/user-attachments/assets/07fe6d6c-f283-42c9-be57-46bc07914f33)

### Available Scope Options

<div class="grid cards" markdown>

-   :material-database:{ .lg .middle } __Catalogs__

    ---

    Import entire catalogs at once
    
-   :material-folder-table:{ .lg .middle } __Schemas__

    ---
    
    Select specific database schemas
    
-   :material-table:{ .lg .middle } __Tables__

    ---

    Choose individual tables and views
    
-   :material-table-column:{ .lg .middle } __Columns__

    ---

    Detailed column-level metadata

</div>

## Schedule Import Job

### Configure Schedule

!!! example "Scheduling Options"
    Choose the timing that works best for your needs:

=== "Basic Schedule"
    ![Basic Schedule](https://github.com/user-attachments/assets/76529cc8-3e9e-4eae-abb5-13deb1194019)

=== "Advanced Options"
    ![Advanced Options](https://github.com/user-attachments/assets/51470499-71fa-4f78-9d7b-7a8eda978875)

=== "Final Review"
    ![Schedule Review](https://github.com/user-attachments/assets/d8e46ca2-5153-4ed3-b5b5-e5495e4d2daf)

### Schedule Types

<div class="grid cards" markdown>

-   :material-clock-outline:{ .lg .middle } __One-time__

    ---

    Single import execution
    
-   :material-refresh:{ .lg .middle } __Recurring__

    ---
    
    Regular automated imports
    
-   :material-clock-edit:{ .lg .middle } __Custom__

    ---

    Tailored schedule intervals
    
-   :material-earth:{ .lg .middle } __Time Zone__

    ---

    Timezone-specific scheduling

</div>

## Verification Process

### Check Import Results

!!! success "Verification Steps"
    After import completion, verify your results:

=== "Table View"
    ![Table Results](https://github.com/user-attachments/assets/cfcdca55-0899-4a56-8b09-1a873fc2ef41)

=== "Profile View"
    ![Profile Results](https://github.com/user-attachments/assets/b64930ab-3a75-4067-bba2-3b3e05174958)

=== "Detailed View"
    ![Detailed Results](https://github.com/user-attachments/assets/4b5fda51-179b-4ef1-9a7e-d8daabefb09d)

### Verification Checklist

<div class="grid cards" markdown>

-   :material-checkbox-marked:{ .lg .middle } __Asset Discovery__

    ---

    - Verify all selected assets
    - Confirm metadata accuracy
    - Check relationships
    
-   :material-database-check:{ .lg .middle } __Technical Metadata__

    ---
    
    - Table and column names
    - Data types
    - Key relationships
    - Access patterns
    
-   :material-book-check:{ .lg .middle } __Catalog Entries__

    ---

    - Asset visibility
    - Metadata completeness
    - Classification status

</div>

## Best Practices

### Implementation Guide

<div class="grid" markdown>

=== ":material-clipboard-check: Pre-Import"
    - Review source assets
    - Plan discovery scope
    - Prepare permissions
    - Document expectations

=== ":material-progress-check: During Import"
    - Monitor progress
    - Check for errors
    - Verify connectivity
    - Track resources

=== ":material-checkbox-marked-circle: Post-Import"
    - Validate assets
    - Review metadata
    - Check missing items
    - Document issues

</div>

## Troubleshooting

### Common Issues and Solutions

!!! warning "Known Issues"
    Here's how to handle common problems:

    === "Connection Problems"
        - Check network connectivity
        - Verify credentials
        - Validate SSL certificates
        - Review permissions

    === "Discovery Issues"
        - Verify asset accessibility
        - Check scope settings
        - Review error logs
        - Validate source status

    === "Metadata Issues"
        - Check incomplete metadata
        - Verify relationships
        - Review data types
        - Check encoding

## Next Steps

!!! success "Post-Import Actions"
    After completing your MDI setup:

    1. [:material-checkbox-marked-circle: Review discovered assets](#verification-process)
    2. [:material-database-check: Plan metadata enrichment (MDE)](metadata-enrichment.md)
    3. [:material-shield-lock: Configure governance rules](rules-policies.md)
    4. [:material-security: Set up data protection](rules-policies.md)

## References

<div class="grid cards" markdown>

-   :material-book:{ .lg .middle } __Documentation__

    ---

    [:octicons-link-external-24: IBM Knowledge Catalog Documentation](https://cloud.ibm.com/docs/data-catalog){ .md-button }

-   :material-link:{ .lg .middle } __Integration__

    ---
    
    [:octicons-link-external-24: watsonx.data Integration Guide](https://cloud.ibm.com/docs/watsonxdata?topic=watsonxdata-ikc_integration){ .md-button }

-   :material-school:{ .lg .middle } __Best Practices__

    ---

    [:octicons-link-external-24: Metadata Discovery Best Practices](https://www.ibm.com/docs/en/cloud-paks/cp-data/4.6.x?topic=catalog-discovering-data-assets){ .md-button }

</div>