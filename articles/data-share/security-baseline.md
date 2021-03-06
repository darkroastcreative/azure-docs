---
title: Azure security baseline for Azure Data Share
description: The Azure Data Share security baseline provides procedural guidance and resources for implementing the security recommendations specified in the Azure Security Benchmark.
author: msmbaldwin
ms.service: data-share
ms.topic: conceptual
ms.date: 11/17/2020
ms.author: mbaldwin
ms.custom: subject-security-benchmark

# Important: This content is machine generated; do not modify this topic directly. Contact mbaldwin for more information.

---

# Azure security baseline for Azure Data Share

This security
baseline applies guidance from the [Azure Security Benchmark version
1.0](../security/benchmarks/overview-v1.md) to Microsoft Azure Data Share. The Azure Security Benchmark
provides recommendations on how you can secure your cloud solutions on Azure.
The content is grouped by the **security controls** defined by the Azure
Security Benchmark and the related guidance applicable to Azure Data Share. **Controls** not applicable to Azure Data Share have been excluded.

 
To see how Azure Data Share completely maps to the Azure
Security Benchmark, see the [full Azure Data Share security baseline mapping
file](https://github.com/MicrosoftDocs/SecurityBenchmarks/tree/master/Azure%20Offer%20Security%20Baselines).

## Logging and monitoring

*For more information, see the [Azure Security Benchmark: Logging and monitoring](../security/benchmarks/security-control-logging-monitoring.md).*

### 2.2: Configure central security log management

**Guidance**: 
Ingest logs related to Azure Data Share via Azure Monitor to aggregate security data generated by endpoint devices, network resources, and other security systems. In Azure Monitor, use Log Analytics workspaces to query and perform analytics, and use Azure Storage accounts for long term and archival storage.

Alternatively, you can enable and on-board this data to Azure Sentinel or a third-party SIEM.

- [How to onboard Azure Sentinel](../sentinel/quickstart-onboard.md) 

- [How to collect platform logs and metrics with Azure Monitor](../azure-monitor/essentials/diagnostic-settings.md) 

- [How to get started with Azure Monitor and third-party SIEM integration](https://azure.microsoft.com/blog/use-azure-monitor-to-integrate-with-siem-tools/) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

### 2.3: Enable audit logging for Azure resources

**Guidance**: Activity logs, which are automatically available, contain all write operations (PUT, POST, DELETE) for your Azure Data Share resources except read operations (GET). Activity logs can be used to find an error when troubleshooting or to monitor how a user in your organization modified a resource.

Enable diagnostic logs for Azure Data Share, specifically the diagnostic logs for MicrosoftDataShareSentShareSnapshotsLog &amp; MicrosoftDataShareReceivedShareSnapshotsLog. These logs will enable you to capture key information like synchronization start time, end time, status and other details. These logs can be critical for later investigating security incidents and performing forensic exercises.

- [How to collect platform logs and metrics with Azure Monitor](../azure-monitor/essentials/diagnostic-settings.md) 

- [Understand logging and different log types in Azure](../azure-monitor/essentials/platform-logs-overview.md)

- [How to configure Diagnostic Settings for the Azure Activity Log](../azure-monitor/essentials/activity-log.md)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 2.5: Configure security log storage retention

**Guidance**: Ensure that any storage accounts or Log Analytics workspaces used for storing Azure Data Share logs has the log retention period set according to your organization's compliance regulations.

- [How to configure Log Analytics Workspace Retention Period](../azure-monitor/logs/manage-cost-storage.md)

- [Storing resource logs in an Azure Storage Account](../azure-monitor/essentials/resource-logs.md#send-to-azure-storage)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 2.6: Monitor and review Logs

**Guidance**: Analyze and monitor logs related to Azure Data Share resources for anomalous behavior and regularly review the results. Use Azure Monitor and a Log Analytics workspace to review logs and perform queries on log data.

Alternatively, you can enable and on-board data to Azure Sentinel or a third-party SIEM.

- [How to onboard Azure Sentinel](../sentinel/quickstart-onboard.md) 

- [Getting started with Log Analytics queries](../azure-monitor/logs/log-analytics-tutorial.md) 

- [How to perform custom queries in Azure Monitor](../azure-monitor/logs/get-started-queries.md) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 2.7: Enable alerts for anomalous activities

**Guidance**: 
Use Azure Security Center with Log Analytics workspace for monitoring and alerting on anomalous activity found in security logs and events. Alternatively, you can enable and on-board data to Azure Sentinel.

- [How to onboard Azure Sentinel](../sentinel/quickstart-onboard.md) 

- [How to manage alerts in Azure Security Center](../security-center/security-center-managing-and-responding-alerts.md) 

- [How to alert on log analytics log data](../azure-monitor/alerts/tutorial-response.md) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

## Identity and access control

*For more information, see the [Azure Security Benchmark: Identity and access control](../security/benchmarks/security-control-identity-access-control.md).*

### 3.4: Use single sign-on (SSO) with Azure Active Directory

**Guidance**: Azure Data Share supports SSO authentication with Azure Active Directory. Reduce the number of identities and credentials users must manage by enabling SSO for the service with your organization's pre-existing identities.

- [Understand SSO with Azure AD](../active-directory/manage-apps/what-is-single-sign-on.md)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 3.5: Use multi-factor authentication for all Azure Active Directory based access

**Guidance**: 
Enable Azure AD MFA and follow Azure Security Center identity and access recommendations.

- [How to enable MFA in Azure](../active-directory/authentication/howto-mfa-getstarted.md) 

- [How to monitor identity and access within Azure Security Center](../security-center/security-center-identity-access.md) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

### 3.6: Use dedicated machines (Privileged Access Workstations) for all administrative tasks

**Guidance**: 
Use a secure, Azure-managed workstation (also known as a Privileged Access Workstation, or PAW) for administrative tasks that require elevated privileges.

- [Understand secure, Azure-managed workstations](https://4sysops.com/archives/understand-the-microsoft-privileged-access-workstation-paw-security-model/)
 

- [How to enable Azure AD MFA](../active-directory/authentication/howto-mfa-getstarted.md)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 3.9: Use Azure Active Directory

**Guidance**: Use Azure Active Directory (Azure AD) as the central authentication and authorization system. Azure AD protects data by using strong encryption for data at rest and in transit. Azure AD also salts, hashes, and securely stores user credentials.

- [How to create and configure an Azure AD instance](../active-directory/fundamentals/active-directory-access-create-new-tenant.md) 

- [Azure Data Share works with general Azure built in roles ](../role-based-access-control/built-in-roles.md#general)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 3.10: Regularly review and reconcile user access

**Guidance**: 
Azure AD provides logs to help discover stale accounts. In addition, use Azure AD identity and access reviews to efficiently manage group memberships, access to enterprise applications, and role assignments. User access can be reviewed on a regular basis to make sure only the right users have continued access.

- [Understand Azure AD reporting](../active-directory/reports-monitoring/index.yml) 

- [How to use Azure AD identity and access reviews](../active-directory/governance/access-reviews-overview.md) 

- [Azure Data Share works with general Azure built in roles ](../role-based-access-control/built-in-roles.md#general)

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

### 3.11: Monitor attempts to access deactivated credentials

**Guidance**: You have access to Azure AD sign-in activity, audit, and risk event log sources, which allow you to integrate with any SIEM/monitoring tool.

You can streamline this process by creating diagnostic settings for Azure AD user accounts and sending the audit logs and sign-in logs to a Log Analytics workspace. You can configure desired alerts within Log Analytics workspace.

- [How to integrate Azure activity logs with Azure Monitor](../active-directory/reports-monitoring/howto-integrate-activity-logs-with-log-analytics.md) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 3.12: Alert on account login behavior deviation

**Guidance**: Use Azure AD Identity Protection features to configure automated responses to detected suspicious actions related to user identities. You can also ingest data into Azure Sentinel for further investigation.

- [How to view Azure AD risky sign-ins](../active-directory/identity-protection/overview-identity-protection.md) 

- [How to configure and enable Identity Protection risk policies](../active-directory/identity-protection/howto-identity-protection-configure-risk-policies.md) 

- [How to onboard Azure Sentinel](../sentinel/quickstart-onboard.md)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

## Data protection

*For more information, see the [Azure Security Benchmark: Data protection](../security/benchmarks/security-control-data-protection.md).*

### 4.6: Use Azure RBAC to manage access to resources

**Guidance**: Use Azure role-based access control (Azure RBAC) to manage access to data and resources related to Azure Data Share resources, otherwise use service-specific access control methods.

- [How to configure RBAC in Azure](../role-based-access-control/role-assignments-portal.md) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

### 4.9: Log and alert on changes to critical Azure resources

**Guidance**: Use Azure Monitor with the Azure Activity Log to create Azure Monitor alerts for when changes take place to critical Azure resources.

- [How to create alerts for Azure Activity Log events](../azure-monitor/alerts/alerts-activity-log.md) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

## Vulnerability management

*For more information, see the [Azure Security Benchmark: Vulnerability management](../security/benchmarks/security-control-vulnerability-management.md).*

### 5.1: Run automated vulnerability scanning tools

**Guidance**: Azure Data Share does not allow for the installation of vulnerability scanning tools for its resources.

In general, follow recommendations from Azure Security Center for performing vulnerability assessments on your Azure virtual machines, container images, and SQL servers.

Use a third-party solution for performing vulnerability assessments on network devices and web applications. When conducting remote scans, do not use a single, perpetual, administrative account. Consider implementing JIT provisioning methodology for the scan account. Credentials for the scan account should be protected, monitored, and used only for vulnerability scanning.

- [How to implement Azure Security Center vulnerability assessment recommendations](../security-center/deploy-vulnerability-assessment-vm.md) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

## Inventory and asset management

*For more information, see the [Azure Security Benchmark: Inventory and asset management](../security/benchmarks/security-control-inventory-asset-management.md).*

### 6.1: Use automated asset discovery solution

**Guidance**: You apply tags to your Azure resources, resource groups, and subscriptions to logically organize them into a taxonomy. Each tag consists of a name and a value pair. For example, you can apply the name "Environment" and the value "Production" to all the resources in production.

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.2: Maintain asset metadata

**Guidance**: Apply tags to your Azure resources, resource groups, and subscriptions to logically organize them into a taxonomy. Each tag consists of a name and a value pair. For example, you can apply the name "Environment" and the value "Production" to all the resources in production.

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.3: Delete unauthorized Azure resources

**Guidance**: Use tagging, management groups, and separate subscriptions where appropriate, to organize and track assets. Reconcile inventory on a regular basis and ensure unauthorized resources are deleted from the subscription in a timely manner.

- [How to create additional Azure subscriptions](../cost-management-billing/manage/create-subscription.md) 

- [How to create Management Groups](../governance/management-groups/create-management-group-portal.md) 

- [How to create and use Tags](../azure-resource-manager/management/tag-resources.md)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.4: Define and maintain an inventory of approved Azure resources

**Guidance**: Create an inventory of approved Azure resources and approved software for compute resources as per your organizational needs.

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.5: Monitor for unapproved Azure resources

**Guidance**: Use Azure Policy to put restrictions on the type of resources that can be created in your subscriptions.
Use Azure Resource Graph to query and discover resources within their subscriptions. Ensure that all Azure resources present in the environment are approved.

- [How to configure and manage Azure Policy](../governance/policy/tutorials/create-and-manage.md) 

- [How to create queries with Azure Graph](../governance/resource-graph/first-query-portal.md) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.7: Remove unapproved Azure resources and software applications

**Guidance**: Remove Azure resources when they are no longer needed, this can be done through the Azure portal, PowerShell or CLI.

- [Azure resource group and resource deletion](../azure-resource-manager/management/delete-resource-group.md?tabs=azure-powershell)

Azure Data Share does not expose the OS or allow you to install 3rd party software applications on its resources.

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 6.9: Use only approved Azure services

**Guidance**: Use Azure Policy to restrict which services you can provision in your environment.

- [How to configure and manage Azure Policy](../governance/policy/tutorials/create-and-manage.md) 

- [How to deny a specific resource type with Azure Policy](../governance/policy/samples/built-in-policies.md#general) 

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

### 6.11: Limit users' ability to interact with Azure Resource Manager

**Guidance**: Use Azure Conditional Access to limit users' ability to interact with Azure Resources Manager by configuring "Block access" for the "Microsoft Azure Management" App.

- [How to configure Conditional Access to block access to Azure Resources Manager](../role-based-access-control/conditional-access-azure-management.md) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

## Secure configuration

*For more information, see the [Azure Security Benchmark: Secure configuration](../security/benchmarks/security-control-secure-configuration.md).*

### 7.5: Securely store configuration of Azure resources

**Guidance**: Use Azure DevOps to securely store and manage your code like custom Azure Policy definitions, Azure Resource Manager templates and desired state configuration scripts. To access the resources you manage in Azure DevOps, you can grant or deny permissions to specific users, built-in security groups, or groups defined in Azure Active Directory (Azure AD) if integrated with Azure DevOps, or Active Directory if integrated with TFS.

- [How to store code in Azure DevOps](/azure/devops/repos/git/gitworkflow?preserve-view=true&view=azure-devops)

- [About permissions and groups in Azure DevOps](/azure/devops/organizations/security/about-permissions) 

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 7.7: Deploy configuration management tools for Azure resources

**Guidance**: Use Azure Policy aliases in the "DataShare" namespace to create custom policies to alert, audit, and enforce system configurations. Additionally, develop a process and pipeline for managing policy exceptions.

- [How to configure and manage Azure Policy](../governance/policy/tutorials/create-and-manage.md) 

- [How to use aliases](../governance/policy/concepts/definition-structure.md#aliases)

**Azure Security Center monitoring**: Not applicable

**Responsibility**: Customer

### 7.12: Manage identities securely and automatically

**Guidance**: Use managed identities to provide Azure services with an automatically-managed identity in Azure AD. Managed identities allow you to authenticate to any service that supports Azure AD authentication, including Key Vault, without any credentials in your code.

- [How to configure managed identities for Azure resources](../active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm.md)

**Azure Security Center monitoring**: Yes

**Responsibility**: Customer

## Next steps

- See the [Azure security benchmark](../security/benchmarks/overview.md)
- Learn more about [Azure security baselines](../security/benchmarks/security-baselines-overview.md)