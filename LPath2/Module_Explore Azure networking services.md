# [Explore Azure networking services]()
## Module 6 - has 7 units
### Unit : 1 Introduction
---
### Unit : 2 Azure VNet fundamentals
---
### Unit : 3 Azure vnet Settings
---
### Unit : 4 AzureVPN Gateways fundamentals
- **Policy based VPNs**
  - Statically specify which IP to which tunnel
  - Scenarios like - Compatibility with legacy on prem VPNs 
  - Static routes, - Source and dest of tunneled network 
    - Not declared in routing tables because it is in policy
- **Route-based VPNs**
  - Defining which IP for which tunnel is cumbersome
  - _IPSec tunnels are modeled as a network interface or virtual tunnel interface_
  - Routing (Static or dynamic) decides which tunnel interface to use.
  - **preferred connection method for on-premises devices**
    - more resilient to topology changes such as the creation of new subnets.
  - _Uses any-to-any (wildcard) traffic selectors_
  - Dynamic routing - unlike policy based where src and dest are predefined
    - Data packets are encrypted based on network routing tables

    ```
    Used when we need connections like....
    - Connections between virtual networks
    - Point-to-site connections
    - Multisite connections
    - Coexistence with an Azure ExpressRoute gateway
    ```
---
**VPN Gateway sizes**
- determined by SKU ( stock keeping units) or size u deploy
![image](https://user-images.githubusercontent.com/43994542/119467618-4e6b5100-bd63-11eb-842b-cc9cbdffd39d.png)
> A Basic VPN gateway should only be used for Dev/Test workloads. In addition, it's unsupported to migrate from Basic to the VpnGW1/2/3/Az SKUs at a later time without having to remove the gateway and redeploy.
---
**Deploy VPN Gateways**
- you'll need some Azure and on-premises resources.
- **Required Azure resources**
  1. VNet - focus on address space - no overlap
  1. GatewaySubnet - at least a /27 address mask
  1. Public IP -  Basic-SKU dynamic public IP address -  `This IP address is dynamic, but it won't change unless you delete and re-create the VPN gateway.`
  1. Local Network Gateway 
      - configuration includes the **on-premises VPN device's public IPv4 address** and the **on-premises routable networks**.
  1. VNet Gateway
      - Create the virtual network gateway to route traffic between the virtual network and the on-premises datacenter or other virtual networks.
      - either a VPN or ExpressRoute gateway
  1. Connection
    - Create a connection resource to create a logical connection between the VPN gateway and the local network gateway.
  ![image](https://user-images.githubusercontent.com/43994542/119468940-8d4dd680-bd64-11eb-8483-abb2eae80080.png)

- **Required on prem resources** - to connect to VPN gateway
    1. VPN with policy or route based VPN gateway support
    1. Public facing IPv4 address

---
**_HIGH AVAILABILITY SCENARIOS_**
	- fault tolerant config
- **Active/ Standby**
	- By default - 2 instances - one active and one standby (even if only one in VPN gateway resource is visible)
	- When active disrupted - standby takes over
		-  Connections are interrupted during this failover, but they're typically restored within a few seconds for planned maintenance and within 90 seconds for unplanned disruptions 
- **Active/ Active**
	- With support for the BGP routing protocol, you can also deploy VPN gateways in an active/active configuration
	- unique public IP address to each instance
	-  create separate tunnels from the on-premises device to each IP address.
	-  EXTEND the high availability by deploying **an additional VPN device on-premises**.
-  **Expressroute failover**
	-  High-availability option is to configure **a VPN gateway** as a secure failover path for ExpressRoute connections
	-  Expressroute not immune to phy things - like cable or outages to locations
	-  VPN gateway that uses the internet as an alternative method of connectivity
		- Ensures connections always exists. 

- **Zone redundant gateways**
	- VPN gateways and ExpressRoute gateways can be deployed in a zone-redundant configuration - **AVAILABILITY ZONE SUPPORT NEEDED**
	- physically and logically separates gateways within a region
	- protects from zone level failures
	- **require different gateway SKUs and use Standard public IP addresses instead of Basic public IP addresses.**

---

### Unit : 5 Azure ExpressRoute
- extend your on-premises networks into the Microsoft cloud over a private connection with the help of a connectivity provider
- u can connect to Microsoft Azure, Microsoft 365
- Connectivity can be from an **any-to-any (IP VPN) network, a point-to-point Ethernet network, or a virtual cross-connection** (virtual cc _: Colocated providers can normally offer both Layer 2 and Layer 3 connections between your infrastructure, which might be located in the colocation facility, and the Microsoft cloud_) through a connectivity provider at a colocation facility.
- more reliability, faster speeds, consistent latencies, and higher security than internet based connectivity
![image](https://user-images.githubusercontent.com/43994542/119472168-9ee4ad80-bd67-11eb-8bda-7c2bd78d5db2.png)

- Focus on Data link layer 2 and Network layer 3 of OSI
- **Features and benefits**
- Layer 3 connect b/w on prem and Microsoft Cloud
- Connect to MS cloud across all regions
	```
	Microsoft Office 365
	Microsoft Dynamics 365
	Azure compute services, such as Azure Virtual Machines
	Azure cloud services, such as Azure Cosmos DB and Azure Storage
	```
- Expressroute premium addon
- Dynamic route via BGP
- Redundancy in every peering location - > reliability
- SLA uptime
- QoS support for skype for business

- **ExpressRoute Global Reach**
> You can enable ExpressRoute Global Reach to exchange data across your on-premises sites by connecting your ExpressRoute circuits. For example, assume that you have a private datacenter in California connected to ExpressRoute in Silicon Valley. You have another private datacenter in Texas connected to ExpressRoute in Dallas. With ExpressRoute Global Reach, you can connect your private datacenters through two ExpressRoute circuits. Your cross-datacenter traffic will travel through the Microsoft network.
![image](https://user-images.githubusercontent.com/43994542/119475068-6c887f80-bd6a-11eb-9651-50976179fcac.png)

---
### Unit : 6 Knowledge check
![image](https://user-images.githubusercontent.com/43994542/119475528-dc970580-bd6a-11eb-8a91-4674e52eac52.png)

---
### Unit : 7 Summary
- benefits and usage of Azure Virtual Network, Azure VPN Gateway, and Azure ExpressRoute.
- You can now apply this information to help your business use Azure's networking resources to configure its network infrastructure.
---
