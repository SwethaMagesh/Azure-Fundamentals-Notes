# Explore Azure Compute Services
## *Module 2 - 9 units*

[Microsoft Docs for Module 2](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/)
[Microsoft Docs for LP2](https://docs.microsoft.com/en-us/learn/paths/az-900-describe-core-azure-services/)
---
### UNIT 1: Introduction
- *Imagine you're dev lead in Tailwind Traders*
    - Company specialises in hardware manufacturing
    - Website has full near capacity load when peak periods
    - *Dept budget is tight, no free servers to scale out, new equipment - don't know how many new servers are needed, don't want to waste time to procure, set up and install software on servers*
    - Aim: *Obtain resources without too much administration or config*
    - Best solution: *Azure - pay only for the compute resources that's needed*
- **Learning objective**
    ```
    Azure Virtual Machines
    Azure App Service
    Azure Container Instances
    Azure Kubernetes Service
    Azure Functions
    Windows Virtual Desktop
    ```


---
### UNIT 2: Overview of Azure Compute services
- *Intro*
    - On-demand computing service
    - *solutions for development and testing, running applications, and extending your datacenter*
    - Resources: *disks, processors, memory, networking, OS*
    - Available on-demand in minutes, seconds
    - *Service support:* ` Linux, Windows Server, SQL Server, Oracle, IBM, and SAP.`
    - *Prominent service support:*
        ```
        Azure Virtual Machines
        Azure Container Instances
        Azure App Service
        Azure Functions (or serverless computing)
        ``` 
- ***Virtual Machines*** - IaaS
- Software emulations of physical computers
- has *virtual processor, memory, storage, and networking resources*
- Used even for remote desktop client, control like infront of it
- Services: create and use VMs in cloud
    

---
***VM Scale Sets*** 
- Deploy and Manage Identical VMs 
- ***True Autoscale*** - No preprovision required
- For *large scale services - big compute, big data, containerised workloads etc.*
- VM added or removed according to demand
    - ***maybe manual or automated or combination of both***
---
***Containers nd Kubernetes***  
- Compute resources to manage and deploy containers
- Containers
    - *light weight, virtualised app env*
    - Designed for quick create, scale and stop dynamically
    - We can run multiple instances of a containerized app on a single host machine
---
***App service*** - PaaS
- Quickly build, deploy, scale **enterprise grade WEB, MOBILE or API apps**
- Any platform
- We get fully managed platform 
- Adv: Performance, Scalability, Security, Compliance requirements

---
***Functions*** 
- When concerned only about code and not *platform or infra*
- USE WHEN ***you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service*** 
- completed quickly within seconds or less
---
### UNIT 3: When to use Azure VM
- *Typically used:* When total control over OS or env needed
    - Customise all S/W on VM 
    - When running custom S/W or custom hosting configurations
