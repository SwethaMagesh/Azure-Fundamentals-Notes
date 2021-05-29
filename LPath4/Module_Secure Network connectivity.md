# [Secure Network Connectivity](https://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn.az-900-describe-general-security-network-security-features)
## Module has 9 units
### Unit 1: Intro
>- Web defacement is an attack in which bad actors delete or modify the content on the site, replacing it with their own messages.
- DDoS < Defacement < Breach
- **OBJECTIVES**: 
  - Identify the layers that make up a **defense in depth strategy**.
  - Explain how **Azure Firewall** enables you to control what traffic is allowed on the network.
  - Configure **network security groups** to filter network traffic to and from Azure resources within a Microsoft Azure virtual network.
  - Explain how **Azure DDoS Protection** helps protect your Azure resources from DDoS attacks.
---
### Unit 2: What is defense in depth?
- prevent unauthorised access
- Mechanism to slow advance of attack


![image](https://user-images.githubusercontent.com/43994542/119969754-950fb400-bfcc-11eb-8f53-217a8b2f1b9f.png)


- Even if one layer is breached, one more layer is present to enforce security
    1. Physical : At datacenter
    2. Id and access: SSO and multi factor authentication
    3. Perimeter: DDoS n firewalls to prevent attacks
    4. Network: Deny by default - Prevent attack to spread to other resources
    5. Compute: secure Access to VM
    6. Application: App SDLC - introduce security
    7. DATA: DB, disc in VM, SaaS, cloud storage

- **Security Posture:** 
  - confidentiality , integrity (hash or fingerprint) , and availability (DDoS) , known collectively as CIA

---
### Unit 3: Protect Vnets using Azure firewall
- **Firewall**
  - Rules specify **IP**, sometimes (port and protocol too)
  - On prem firewall **disadvantages**: LICENSING + Maintainence from IT staff
  - Azure for both onprem n cloud

![image](https://user-images.githubusercontent.com/43994542/120073588-987f6a00-c0b6-11eb-9d96-9037c770ae78.png)

- **Azure firewall**
  - stateful firewall
    - analyses the complete context of network n not individual packet
  - availability , scalable
  - **Create, enforce policies, log too**
  - **static IP for Vnet resources** - to identify ur vnet 
  - **Azure monitor connected** to log and analyse
  - **Inbound Destination Network Address Translation (DNAT)** support.

- **What can I configure with Azure Firewall?**
- App rules to define FQDNs - they can be accessed from a subnet
- Network rules to define src address, protocol, dest port and dest address
- NAT rules to define destination IP and ports 

- **Azure application gateway** - WAF - Web app firewall
-  WAF - centralised, inbound protection for ur web app from common exploits and vulnerabilities
-  Azure **Front door** n Azure **Content Delivery Network** = also provide WAF services


---
### Unit 4: Protect from DDoS attack using Azure DDoS Protection
- Azure DDoS Protection (Standard service tier)
  - **DDoS attack:** attack to exhause app resources - app is slow or unresponsive for legitimate users
  - Mostly websites but **possible for all public resources on internet**
  - Azure DDoS protection + secure app design practice => protect from DDoS
  - Azure DDoS does: discarding DDoS traffic at the Azure network edge,

  ![image](https://user-images.githubusercontent.com/43994542/120074065-b51ca180-c0b8-11eb-84e7-470aeaec6bad.png)

  - Azure DDoS identifies n blocks DDoS traffic
  - A cleverly designed DDoS attack can cause you to increase your resource allocation, which incurs unneeded expense. **During Automatic scaling**
  - **DDoS Protection Standard** : only customer usage
    - Credit if scaled out due to DDoS
- **What service tiers are available to DDoS Protection**
- BASIC
- STANDARD : ML algo,  specific to Azure VNET resources

- **What kinds of attacks can DDoS Protection help prevent**
- Volumetric attack
- Protocol attack
- Resource layer attack (only with WAF)


---
### Unit 5: Filter network traffic using NSG
- 
---
### Unit 6: Exercise: Config network access using NSG
---
### Unit 7: Combine azure services
---
### Unit 8: Knowledge check
---
### Unit 9: Summary
