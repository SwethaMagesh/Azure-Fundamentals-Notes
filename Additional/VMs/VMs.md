## [Introduction to Azure virtual machines](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-virtual-machines/)
- MODULE - has 8 units

### [CHECKLIST](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-virtual-machines/2-compile-a-checklist-for-creating-a-vm)
- Let's walk through a checklist of things to think about.

    - Start with the network
        - *Network addresses and subnets* are not trivial to change once you have them set up, and if you plan to connect your private company network to the Azure services, you will want to make sure you consider the topology before putting any VMs into place.
        - *Azure reserves the first four addresses and the last address in each subnet for its use.*
        - set up **Network Security Groups** (NSGs) - act as S/W Firewalls
    - Name the VM
        - `For example, devusc-webvm01 might represent the first development web server hosted in the US South Central location.` 
    - Decide the location for the VM
        - the location can limit your available options. **Each region has different hardware available and some configurations are not available in all regions**. 
        - there are price differences between locations. If your workload isn't bound to a specific location, it can be very cost effective to check your required configuration in multiple regions to find the lowest price. 
    - Determine the size of the VM
        - General purpose, compute optimised, Memory optimised, Storage optimised, GPU, High performance computes
        - CHANGE size
            - *allows you to change the VM size when the existing size no longer meets your needs. You can upgrade or downgrade the VM - as long as your current hardware configuration is allowed in the new size.*
            - `Be careful about resizing production VMs - they will be rebooted automatically which can cause a temporary outage and change some configuration settings such as the IP address` 

    - Understanding the pricing model
    - Storage for the VM
    - Select an operating system

### [Manage the availability of your Azure VMs](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-virtual-machines/5-high-availability)

###### An availability set
-  is a logical feature used to ensure that a group of related VMs are deployed so that they aren't *all subject to a single point of failure and not all upgraded at the same time during a host OS upgrade* in the datacenter.
-  VMs placed in an availability set should perform an identical set of functionalities and have the same software installed.
###### What is a fault domain?
- A fault domain is a logical group of hardware in Azure that shares a common set of hardware components, and that share a single point of failure. 
- You can think of it as a *rack within an on-premises datacenter*. 
- The first two VMs in an availability set will be provisioned into two different racks so that if the network or the power failed in a rack, only one VM would be affected. 
![image](https://user-images.githubusercontent.com/43994542/118460281-2b64ef80-b71a-11eb-87d2-6bcce5c84016.png)

###### What is an update domain?
- An update domain is a logical group of hardware that can undergo maintenance, or be rebooted at the same time.
-  Azure will automatically place availability sets into update domains to minimize the impact when the Azure platform introduces host operating system changes. 
- Azure then processes each update domain one at a time.

---
###### Azure Site Recovery - Failover across locations
- replicates workloads from a primary site to a secondary location. If an outage happens at your primary site, you can fail over to a secondary location.
- ***works with***
    -  Azure resources, 
    -  Hyper-V, VMware, and
    -  Physical servers in your on-premises infrastructure
- ***Business continuity and disaster recovery (BCDR) strategy*** 



