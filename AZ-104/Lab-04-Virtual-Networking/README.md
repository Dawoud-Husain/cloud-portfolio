# Lab 04 - Configure Virtual Networking

**Exam area:** AZ-104 - Configure and manage virtual networking

## Objectives

- Create virtual networks and subnets using the Azure portal
- Create virtual networks and subnets using an ARM template
- Create and configure Application Security Groups (ASG) and Network Security Groups (NSG)
- Configure public Azure DNS zones with record sets
- Configure private Azure DNS zones and link them to virtual networks

## Tasks Completed

### Create a virtual network with subnets using the portal

Created the `CoreServicesVnet` virtual network (address space `10.20.0.0/16`) in the `az-104rg4` resource group with two subnets: `SharedServicesSubnet` (10.20.10.0/24) and `DatabaseSubnet` (10.20.20.0/24).

![Create a virtual network with subnets using the portal](<Lab 04 - Create a virtual network with subnets using the portal.png>)

---

### Create a virtual network and subnets using a template

Deployed a second virtual network and its subnets by providing an ARM template, demonstrating infrastructure-as-code as an alternative to manual portal configuration.

![Create a virtual network and subnets using a template](<Lab 04 -  Create a virtual network and subnets using a template.png>)

---

### Create and configure an Application Security Group and Network Security Group

Created `myNSGSecure` and configured it with inbound and outbound security rules referencing an Application Security Group (ASG) as the source/destination, enabling application-centric network segmentation.

**NSG Created**

![NSG Created](<Lab 04 -Create and configure communication between an Application Security Group and a Network Security Group (NSG Created).png>)

**NSG Inbound Rule** — `AllowASG` rule allowing TCP ports 80 and 443 from the ASG at priority 100.

![NSG Inbound Rule](<Lab 04 -Create and configure communication between an Application Security Group and a Network Security Group (NSG Inbound Rule).png>)

**NSG Outbound Rule**

![NSG Outbound Rule](<Lab 04 -Create and configure communication between an Application Security Group and a Network Security Group (NSG Outbound Rule).png>)

---

### Configure a public DNS zone

Created a public Azure DNS zone and added a record set to demonstrate how Azure DNS can host public-facing DNS records for a custom domain.

**Public Zone Created**

![Public Zone Created](<Lab 04 - Configure public and private Azure DNS zones (Public Zone Created).png>)

**Public DNS Record Set**

![Public DNS Recordset](<Lab 04 - Configure public and private Azure DNS zones (Public DNS Recordset).png>)

---

### Configure a private DNS zone

Created a private DNS zone (`private.contoso.com`), added a DNS record set, and linked it to the `ManufacturingVnet` virtual network so that resources within the VNet can resolve private DNS names.

**Creating the Private DNS Zone**

![Creating Private DNS](<Lab 04 - Configure a private DNS zone (Creating Private DNS).png>)

**Private DNS Record Set**

![Private DNS Recordset](<Lab 04 - Configure a private DNS zone (Recordset).png>)

**Virtual Network Link** — linked `ManufacturingVnet` (az-104rg4) to the private zone via the `manufacturing-link` virtual network link.

![Virtual Network Links](<Lab 04 - Configure a private DNS zone (Virtual network links).png>)
