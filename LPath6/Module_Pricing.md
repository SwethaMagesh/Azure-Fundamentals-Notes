# [Plan and Manage Azure Costs](https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/)
## Module has 8 units
### Unit 1: Intro
- The company has run a few **successful proof-of-concept projects** and
- wants to better understand how to manage its costs before it moves its workloads to Azure.
- TCO and Pricing calculator
---
### Unit 2: Compare Costs using TCOC
- **Total cost of ownership** is commonly used in finance. 
- It can be hard to see all the hidden costs related to operating a technology capability on-premises.
-  **Software licenses and hardware** are additional costs.

- Tell cost diff b/w Azure and on prem
- ONPrem: Enter Electricity, Network maintenance, IT Labor cost
- **STEPS:** 1. Define workload 2. Adjust assumption (reuse or replicate) 3. View report
- **Check out what is special abt Bseries VM** 

---
### Unit 3: Exercise: Compare sample workload costs uisng TCO Calci

- whether there are any potential cost savings in moving your European datacenter to the cloud over the next three years. You need to take into account all of the potentially hidden costs involved with operating on-premises and in the cloud.
---
### Unit 4: Purchase Azure Services
```
What types of Azure subscriptions are available?
How do we purchase Azure services?
Does location or network traffic affect cost?
What other factors affect the final cost?
How can we get a more detailed estimate of the cost to run on Azure?
```
- **Subscriptions**: 
  - Free trial
  - Pay as you go (organisations have - volume discounts and prepaid invoicing.)
  - Member offers (`Visual Studio subscribers, Microsoft Partner Network members, Microsoft for Startups members, and Microsoft Imagine members.`)
- **How do I purchase Azure services?**
  - Through an Enterprise Agreement
  - Directly from the web -  `WEB direct`
  - Through a Cloud Solution Provider
- **Factors affecting cost**
  - Resource type - Eg: type, tier, access tier(hot, cool or archive)
  - Usage meters
  - Resource usage
  - Subscription types
  - Marketplace
  - Location n network traffic
    - _Egress traffic is network traffic that begins inside of a network and proceeds through its routers to a destination somewhere outside of the network_
    - > For example, say Tailwind Traders decides to provision its Azure resources in the Azure regions that offer the lowest prices. That decision would save the company some money. But, if they need to transfer data between those regions, or if their users are located in different parts of the world, any potential savings could be offset by the additional network usage costs of transferring data between those resources.
    - Biling Zone for network traffic
- **Estimate total cost**
  - Azure pricing calculator
  -  Only an estimate - might differ
    

---
### Unit 5: Exercise: Estimate using Pricing Calci

- The IT Manager at Tailwind Traders is faced with the decision about whether to replace some aging on-premises hardware or move the application to Azure. The company needs to know how much the ongoing monthly cost of the solution in Azure would be.
---
### Unit 6: Manage n minimise total cost
1. Understand estimated costs before deploy
2. Azure advisor
3. Use spending limits 
4. Azure reservations to prepay (Enterprise Agreement, Cloud Solution Providers, and pay-as-you-go subscriptions)
5. Choose low cost location n region
6. Research available cost-saving offers
7. Use Azure Cost Management + Billing to control spending
8. Apply tags to identify owners
9. Resize underutilised vms
10. Deallocate VM during offhours
11. Delete unused resource
12. Migrate from IaaS to PaaS
13. Save licensing costs
14. Choose cost effective OS
15. Azure Hybrid Benefit
---
### Unit 7: Knowledge Check
  ![image](https://user-images.githubusercontent.com/43994542/120643280-95f48a00-c493-11eb-9a18-23c287a9fa15.png)

---
### Unit 8: Summary
  - TCO calculation
  - Prizing calculator
  - Checklist to minimise costs
---
