# [ Protect against security threats in Azure](https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn.az-900-describe-general-security-network-security-features)
## Module has 8 units
### Unit 1: Intro
- Tailwind Traders runs a mix of workloads on Azure and in its datacenter. The company needs to ensure that all of its systems meet a minimum level of security, and that its information is protected from attacks. The company also needs a way to collect and act on security events from across its digital estate.
- **OBJECTIVES**
  - Strengthen your **security posture** and protect against threats by using Azure Security Center.
  - Collect and act on **security data from many different sources** by using Azure Sentinel.
  - Store and access **sensitive information such as passwords and encryption keys** securely in Azure Key Vault.
  - Manage **dedicated physical servers** to host your Azure VMs for Windows and Linux by using Azure Dedicated Host.
---
### Unit 2: Protect against security threats - Azure Security Center
>**Security posture** refers to an organization's overall cybersecurity strength and how well it can predict, prevent and respond to ever-changing cyberthreats.
- Azure Security Center is a monitoring service that provides visibility of your security posture across all of your services, **both on Azure and on-premises**
- **Features**
  - Both onprem n cloud
  - Recommendations
  - Automatic setting for new resources
  - ML to detect malware
  - Identify vulnerabilities, prevent attacks, analyse post breech
  - Give security score to improve security posture
- **Azure Security center**
![image](https://user-images.githubusercontent.com/43994542/119927819-d46fdd80-bf97-11eb-991d-ca2d99f03c84.png)
- **Resource security hygiene section**
  - To help prioritize remediation actions, **recommendations are categorized as low, medium, and high**
- **Security score**
  -  security controls, or groups of related security recommendations
  -  increase score by remediating the recommendations for a single resource within control
  -  Compare with benchmark, establish KPI
  -  report current posture , improve for future

- **Protect against threats**
  - **Just in time VM access**
    - Specific ports of VM only when admin requests access
  - **Adaptive app control**
    - Only authorised app runs. ML to detect whether unauthorised app runs in BG
  - **Adaptive Network hardening**
    - Compare traffic pattern with NSG setting - recommend changes
  - **File Integrity monitoring** 
    - Important file changes monitored : like registry setting, app, and others involved in sec attacks

- **Respond to security alerts**
  - Centralised view to all security alerts: **Security center**
  - dismiss false alerts,
  - investigate them further,
  - remediate alerts manually, or 
  - use an automated response with a workflow automation.
    - **Logic app + security center connector**
    - triggered by threat detection alert or recommendation
    - action: Mail or msg in teams channel
  
 

---
### Unit 3: Detect and respond  - Azure Sentinel
- **Security information and event management (SIEM)**
  - This aggregates from various sources
  - sources must support **Open standard logging format**
  - Threat detection and response
  - EG: Azure Sentinel - MS cloudbased SIEM system
    - intelligent security analytics and threat analysis.
- **CAPABILITIES**:
  - Collect data all user, dev and both onprem n cloud
  - Use AI
  - Respond rapid by workflow or orchestration
  - Detect prev undetected threats
1. **Connect Data** : MS solutions / Other service n solutions / Industry standard sources : _Syslog, REST API, CEF_
2. **Detect Threat** : Custom (set by u and run on schedule) + Built in analytics ( common security + ML based algo from MS proprietary algos)
3. **Investigate n Respond** : investigate specific alerts or incidents (a group of related alerts); 
    - Investigation GRAPH - directly connected entities to investigate
    - **Azure Monitor Workbooks** to automate responses to threats.
      - Run manual or automatically
      - EG: Malicious IP access: 1. IT Ticketing system   `An issue tracking system is a computer software package that manages and maintains lists of issues` 2. Teams / Slack msg to Security analyst. 3. Block/ Ignore option for Network admin 
 
---
### Unit 4: Store and manage secrets - Azure key vault
- sensitive information such as passwords, encryption keys, and certificates
- Azure Key vault: access control and logging capabilities + single central location for an app
- A **hardware security module (HSM)** is a physical computing device that safeguards and manages digital data
- **Azure Key vault**
  - Store tokens, passwords, certificates, API keys, and other secrets.
  - Encryption keys
  - SSL/TLS certificates
  - either thru s/w or FIPS level 2 HSM 
- **Benefits**
  - Centralise app secret : less chance or leak
  - Secure storage : industry-standard algorithms, key lengths, and HSMs
  - Monitor n control access
  - Simple administration of app secrets: Specially certificates from Public CA
  - Integrate with other azure services

---
### Unit 5: Exercise: Manage pwd in Key Vault
- can use Azure portal, the Azure CLI, or Azure PowerShell
- Prog Lang from app also
- HERE:
  - CREATE n ACCESS using portal
  - Access using CLI
- Vault URI field shows the URI that your application can use to access your vault from the REST API.
![image](https://user-images.githubusercontent.com/43994542/119966874-617f5a80-bfc9-11eb-82ce-3e13f462b5e7.png)

---
### Unit 6: Host VM on dedicated hosts - Azure Dedicated Host
- Some organizations must follow regulatory compliance that requires them to be **the only customer using the physical machine that hosts their virtual machines**. 

-   ![image](https://user-images.githubusercontent.com/43994542/119967352-e5394700-bfc9-11eb-9605-bcb4670d6c50.png)

- **BENEFITS**:
  - choose VM size, series on that host
  - Compliance by getting isolated server
  - Get visibility and control over Infrastructure!

- **AVAILABILITY** 
  - High availability: u provision **host group** (many hosts) 
  - You can control when regular maintenance happens in 35 day rolling window. 
- **PRICING**: 
  - Charge per dedicated host: Irrespective of no of VMs
  - Host price based on VM family, region
  - Software licensing, storage, and network usage are billed separately from the host and VMs. 
---
### Unit 7: Knowledge check
![image](https://user-images.githubusercontent.com/43994542/119968406-0e0e0c00-bfcb-11eb-946f-10d838d95970.png)

---
### Unit 8: Summary
  - Azure Security Center provides visibility of your security posture across all of your services, both on Azure and on-premises.
  - Azure Sentinel aggregates security data from many different sources, and provides additional capabilities for threat detection and response.
  - Azure Key Vault stores your applications' secrets, such as passwords, encryption keys, and certificates, in a single, central location.
  - Azure Dedicated Host provides dedicated physical servers to host your Azure VMs for Windows and Linux.

---

