# Lab 05 - Implement Intersite Connectivity

**Exam area:** AZ-104 - Configure and manage virtual networking

## Objectives

- Deploy virtual machines into separate virtual networks
- Configure virtual network peering between VNets
- Create a custom route table and associate it with a subnet
- Test connectivity between virtual machines using Azure PowerShell and Network Watcher

## Tasks Completed

### Create a core services virtual machine and virtual network

Deployed a virtual machine (`CoreServicesVM`) into the `CoreServicesVM-vnet` virtual network as the first endpoint for testing intersite connectivity.

![Create a core services virtual machine and virtual network](<Lab 05 - Create a core services virtual machine and virtual network.png>)

---

### Create a virtual machine in a different virtual network

Deployed a second virtual machine (`ManufacturingVM`) into the `ManufacturingVnet` virtual network in a separate resource group to simulate connectivity across different network segments.

![Create a virtual machine in a different virtual network](<Lab 05 - Create a virtual machine in a different virtual network.png>)

---

### Configure virtual network peering

Created a bidirectional VNet peering between `CoreServicesVM-vnet` and `ManufacturingVnet` (`ManufacturingVnet-to-CoreServicesVnet`), enabling traffic to flow between the two networks without transiting the public internet.

![Configure virtual network peerings between virtual networks](<Lab 05 - Configure virtual network peerings between virtual networks.png>)

---

### Create a custom route

Created a route table (`rt-CoreServices`) in the `CoreServicesVM_group` resource group with gateway route propagation disabled, then added a custom route and associated it with a subnet to control traffic flow.

**Route Table Created**

![Route Table](<Lab 05 - Create a custom route (Route Table).png>)

**Custom Route Added**

![Route Table Route](<Lab 05 - Create a custom route (Route Table Route).png>)

**Subnet Association**

![Route Table Associate Subnet](<Lab 05 - Create a custom route (Route Table -  Associate Subnet).png>)

---

### Use Azure PowerShell to test connectivity

Used Azure PowerShell (`Test-NetConnection`) to verify TCP connectivity between the `CoreServicesVM` and `ManufacturingVM` across the VNet peering.

![Use Azure PowerShell to test the connection between virtual machines](<Lab 05 - Use Azure PowerShell to test the connection between virtual machines.png>)

---

### Use Network Watcher to test connectivity

Used the Azure Network Watcher **Connection Troubleshoot** tool to diagnose connectivity between the two VMs, reviewing hop-by-hop results including Connectivity Check, NSG diagnostics, and Next Hop outcomes.

![Use Network Watcher to test the connection between virtual machines](<Lab 05 - Use Network Watcher to test the connection between virtual machines.png>)
