# Lab 06 - Implement Traffic Management

**Exam area:** AZ-104 - Configure and manage virtual networking

## Objectives

- Provision infrastructure using an ARM template
- Configure an Azure Load Balancer to distribute traffic across backend VMs
- Configure an Azure Application Gateway for path-based HTTP routing

## Tasks Completed

### Use a template to provision an infrastructure

Deployed the lab infrastructure (virtual network, subnets, and backend virtual machines) using an Azure Resource Manager template, establishing the environment required for both the Load Balancer and Application Gateway tasks.

![Use a template to provision an infrastructure](<Lab 06 - Use a template to provision an infrastructure.png>)

---

### Configure an Azure Load Balancer

#### Deploy the Load Balancer

Created a public Azure Load Balancer (`az104-06-lb4`) with a frontend IP, backend pool containing the lab VMs, and a health probe targeting port 80.

![Deploying Load Balancer](<Lab 06 - Configure an Azure Load Balancer (deploying lb).png>)

#### Add a Load Balancing Rule

Added a load balancing rule to forward inbound TCP port 80 traffic from the frontend IP to the backend pool, enabling round-robin distribution across the backend VMs.

![Load Balancer Rule](<Lab 06 - Configure an Azure Load Balancer (lb rule).png>)

---

### Configure an Azure Application Gateway

#### Add a Dedicated Subnet

Added a dedicated `appgwsubnet` subnet to the virtual network to satisfy the Application Gateway requirement of an exclusive subnet.

![Adding Subnet for Application Gateway](<Lab 06 - Configure an Azure Application Gateway (adding subnet).png>)

#### Deploy the Application Gateway

Created an Azure Application Gateway (`az104-06-appgw5`) with an HTTP listener, backend pools mapped to individual VM targets, and path-based routing rules to direct requests to specific backends based on URL path.

![Adding Application Gateway](<Lab 06 - Configure an Azure Application Gateway (adding app gateway).png>)
