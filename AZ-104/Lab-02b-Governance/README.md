# Lab 02b - Manage Governance via Azure Policy

**Exam area:** AZ-104 - Manage subscriptions and governance

## Objectives

- Assign tags to Azure resources manually via the portal
- Enforce tagging requirements using Azure Policy
- Apply automatic remediation tagging through a policy assignment
- Configure and test resource locks to prevent accidental deletion or modification

## Tasks Completed

### Assign tags via the Azure portal

Manually applied resource tags to an Azure resource group to support cost tracking, ownership identification, and organizational categorization.

![Assign tags via the Azure portal](<Lab 02b - Assign tags via the Azure portal.png>)

---

### Enforce tagging via an Azure Policy

Assigned a built-in Azure Policy to enforce that a required tag is present on all resources within a scope. Resources that do not comply are flagged for remediation.

![Enforce tagging via an Azure Policy](<Lab 02b - Enforce tagging via an Azure Policy.png>)

---

### Apply tagging via an Azure policy

Configured a policy with a **DeployIfNotExists** or **Modify** effect to automatically apply tags to resources that are missing them, demonstrating automated governance remediation.

![Apply tagging via an Azure policy](<Lab 02b - Apply tagging via an Azure policy.png>)

---

### Configure and test resource locks

Applied a **Delete** lock to a resource group (`az104-rg2`) to prevent accidental deletion while still allowing modifications. Verified the lock behavior by attempting a delete operation.

![Configure and test resource locks](<Lab 02b - Configure and test resource locks.png>)
