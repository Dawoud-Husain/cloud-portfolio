# Lab 02a - Manage Subscriptions and RBAC

**Exam area:** AZ-104 - Manage subscriptions and governance

## Objectives

- Implement Azure Management Groups to organize subscriptions
- Review and assign built-in Azure RBAC roles
- Create a custom RBAC role with specific permissions
- Monitor role assignments using the Activity Log

## Tasks Completed

### Implement Management Groups

Created a management group (`az104-mg`) to provide a governance scope above the subscription level, enabling policy and access control to be applied hierarchically.

![Implement Management Groups](<Lab 02a - Implement Management Groups.png>)

---

### Review and assign a built-in Azure role

Reviewed the available built-in roles and assigned the **Virtual Machine Contributor** role to the Help Desk security group, scoped to the `az104-mg` management group.

![Review and assign a built-in Azure role](<Lab 02a - Review and assign a built-in Azure role.png>)

---

### Create a custom RBAC role

Created a custom RBAC role with a tailored set of permissions, demonstrating how to go beyond built-in roles to meet least-privilege requirements.

![Create a custom RBAC role](<Lab 02a - Create a custom RBAC role.png>)

---

### Monitor role assignments with the Activity Log

Used the Azure Activity Log to audit and review role assignment changes made within the scope of the management group.

![Monitor role assignments with the Activity Log](<Lab 02a - Monitor role assignments with the Activity Log.png>)
