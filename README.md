# Microsoft Sentinel All-in-One

## What does All-in-One do?

Microsoft Sentinel All-in-One automates the following tasks:

- Creates resource group
- Creates Log Analytics workspace
- Installs Microsoft Sentinel on top of the workspace
- Sets workspace retention, daily cap and commitment tiers if desired
- Enables UEBA with the relevant identity providers (AAD and/or AD)
- Enables health diagnostics for Analytics Rules, Data Connectors and Automation Rules
- Installs Content Hub solutions from a predefined list in three categories: 1st party, Essentials and Training
- Enables Data Connectors from this list:
    + Azure Active Directory (with the ability to select which data types will be ingested)
    + Azure Active Directory Identity Protection
    + Azure Activity (from current subscription)
    + Dynamics 365
    + Microsoft 365 Defender
    + Microsoft Defender for Cloud
    + Microsoft Insider Risk Management
    + Microsoft Power BI
    + Microsoft Project
    + Office 365
    + Threat Intelligence Platforms
- Enables analytics rules (Scheduled and NRT) included in the selected Content Hub solutions, with the ability to filter by severity
- Enables analytics rules (Scheduled and NRT) that use any of the selected Data connectors, with the ability to filter by severity

## Prerequisites

- Azure Subscription
- Azure user account with enough permissions to enable the desired connectors. See table at the end of this page for additional permissions. Write permissions to the workspace are **always** needed.
- Some data connectors require the relevant licence in order to be enabled. See table at the end of this page for details.

## Try it now!

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FLittlefish-SOC%2FSentinel-All-In-One%2Ftesting-lm%2Fazuredeploy.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2FLittlefish-SOC%2FSentinel-All-In-One%2Ftesting-lm%2FcreateUiDefinition.json)


## Supported connectors

The following table summarizes permissions, licenses and permissions needed and related cost to enable each Data Connector:

| Data Connector                                 | License         |  Permissions                    | Cost      |
| ---------------------------------------------- | --------------- |---------------------------------|-----------|
| Azure Active Directory (Tenant scope version only) | Any AAD license | Global Admin or Security Admin  | Billed    |
| Azure Active Directory Identity Protection  | AAD Premium 2   | Global Admin or Security Admin  | Free      |
| Azure Activity                                 | None            | Subscription Reader             | Free      |
| Dynamics 365                                   | D365 license    | Global Admin or Security Admin  | Billed    |
| Microsoft 365 Defender                         | M365D license   | Global Admin or Security Admin  | Free      |
| Microsoft Defender for Cloud                   | MDC license     | Security Reader                 | Free      |
| Microsoft Insider Risk Management              | IRM license     | Global Admin or Security Admin  | Free      |
| Microsoft PowerBi                              | PowerBi license | Global Admin or Security Admin  | Billed    |
| Microsoft Project                              | MS Project license | Global Admin or Security Admin | Billed  |
| Office 365                                     | None            | Global Admin or Security Admin  | Free      |
| Threat Intelligence Platforms                  | None            | Global Admin or Security Admin  | Billed    |
