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
- 
---
### Unit 4: Protect from DDoS attack using Azure DDoS Protection
---
### Unit 5: Filter network traffic using NSG
---
### Unit 6: Exercise: Config network access using NSG
---
### Unit 7: Combine azure services
---
### Unit 8: Knowledge check
---
### Unit 9: Summary
