# Explore Azure Compute Services
## *Module 2 - 9 units*

- [Microsoft Docs for Module 2](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/)
- [Microsoft Docs for LP2](https://docs.microsoft.com/en-us/learn/paths/az-900-describe-core-azure-services/)
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
- *Flexibility - no need to buy and maintain physical hardware.*
    - *We need to configure, update and manage the s/w on VM*
- **Selecting a preconfigured VM image** is most important
    - image is a template to create VM
    - Template already has OS and other s/w like  *dev tools, web hosting env etc*
---
***Eg. when to use VM*** 
```
- Test and development
    - quick to create different OS n app configurations
    - easy to delete when we don't need them
- Run app on cloud
    - Economic benefits - to run app on public cloud vs Traditional infra
    - Shut down VMs quick, when we don't need them
    - Start up VMs to meet sudden increase in need
- Extend Datacenter to cloud
    - Create Virtual Network in Azure
    - Add VMs to Virtual network
    - Less expensive to deploy than on on-prem (EG: SHAREPOINT like apps)
- Disaster Recovery
    - IaaS based approach to disaster recovery
    - If primary datacenter fails, create VMs on azure for critical apps, then shut down after primary datacenter resumes
```
---
***MOVE TO CLOUD WITH VMs*** 
- LIFT N SHIFT
    - *Move a phy server to cloud*
    - Just create image for phy server and host it on VM with little or no changes
    - Must maintain VM though, - *update the OS and software it runs*

***SCALE VMs in AZURE*** 
    1. VM Scale Sets
    1. Azure Batch

**VM Scale Sets**
: Group of identical load balanced VMs. - High *availability*
- Eg. for scientist to upload and process Astronomy images
- Normally duplicate VM => *config additional service to route requests between multiple instances* 
- VM Scale sets do that automatically in response to *demand or schedule*
- Service: *Big data, compute, container workloads*

**Azure Batch**
: Highly parallel and High performance computing batch jobs - scaling tens, hundreds or thousands of VMs

- BATCH does
    - Starts a pool of compute VMs
    - Installs apps n staging data
    - Runs jobs with as many tasks as you have
    - Identify failure
    - Requeue work
    - Scales down as soon as work is complete
- *Service: you need raw computing power or supercomputer-level compute power*

---
### UNIT 4: When to use Azure Container Instances or Azure Kubernetes Service
- *INTRO*
    - VM cons => Limited to single OS per VM
    - Multiple instances of an app on single host machine => Containers
- ***Containers*** 
    - Virtualisation Environment
    - We can run ***multiple containers on a single host (phy or virtual)*** like multiple VM on a single phy host
    - Most popular container engine: ***docker*** supported by Azure

| VM | Container |
|---|---|
|An instance of an OS that you can connect to and manage  | Lightweight, designed to create, scale and stop dynamically |
| it's possible to create and deploy virtual machines as application demand increases | allow you to respond to changes on demand - quick to restart on crash |

--- 
Video on comparison of VM, containers

|VM|Containers|
|---|---|
|Takes long start up time (APP PLUS OS) | Quick to start|
|Virtualised on hardware abstractions - CPU, storage, RAM| Virtualised on OS layer|
|When you need ***complete control*** |When you need ***portability, performance*** |
||Easy to develop. Has Orchestrator like Kubernetes to manage|
|One machine with many OS - needs several VMs| One machine with different OS or environment for each app - Needs only one VM now|
