# [Choose the right Azure services by examining SLAs and service lifecycle](https://docs.microsoft.com/en-us/learn/modules/choose-azure-services-sla-lifecycle/)
## Module 2 has 7 units
### Unit : 1 Intro
- SLA
- Lifecycle of new Azure services - Preview to general availability
- **How will moving to the cloud affect availability agreements?**
- planned maintenance
- availability
- But no burden of supporting IT infra
- **OBJECTIVES**
- SLA and why; factors like tier and SLA; Composite SLA; Service lifecycle and preview access;
---
### Unit : 2 What are SLA
  - formal agreement between a service company and the customer. 
  - performance commitment from MS to customer

  - Each service has its own SLA
  - Knowing it, helps set SLA with customer
  - SECTION:
    - **INTRO** 
    - **GEN TERMS** - Terms, claim, receive credit, limitations
    - **SLA details** - Specifics of guarantee, 
  - Downtime
  - **Cumulative** calculations: duration of multiple outages added

  - Eg: how percentage of 99.9 and 99.99 **differ** significantly

  |SLA percentage	|Downtime per week	|Downtime per month|	Downtime per year|
  |---|---|---|---|
  |99|	1.68 hours|	7.2 hours	|3.65 days|
  |99.9|	10.1 minutes	|43.2 minutes|	8.76 hours|
  |99.95|	5 minutes|	21.6 minutes|	4.38 hours|
  |99.99|	1.01 minutes|	4.32 minutes|	52.56 minutes|
  |99.999|	6 seconds|	25.9 seconds|	5.26 minutes|

- **SERVICE credits**
- percent of fee credited back according to claim approval

- **What's the SLA for free services?** - Free products typically don't have an SLA.
- **How do I know when there's an outage?**

 ![image](https://user-images.githubusercontent.com/43994542/120612386-c5df6580-c472-11eb-817b-32ed1091f1a1.png)

  - Azure status - RSS feed of changes to health
  - Azure Service Health - link is provided in status; provides personalised view
  
- **How can I request a service credit from Microsoft?** 
  - File a claim
  - Timeline: SLA
    - EG: _*submit your claim by the end of the calendar month following the month in which the incident occurred.*_
 
---

### Unit : 3 Define Application SLA

  - SLA requirements for a specific application. This term typically refers to an application that you build on Azure.
  - Discuss with team for availability: design decisions extend beyond SLA! (BUT how?)
  - **BUSINESS IMPACT**
    - Customers will either need to try again later or possibly go to a competitor.
    - Staff cant get existing orders
  - **Effect on other business operations**
    - Majority of the Tailwind Traders business will continue to function normally if the Special Orders application went down.
  - **Usage patterns** -- when and how users access your application.
    - **Critical and non-critical time periods**. For example, a _tax-filing application_ can't fail during a filing deadline.
    - Retail hours at diff locations; - EG: it can go down in middle of night. No problem. 
  - **Team decision**
    - 99.9 % SLA, 10.1 min per week
    - HOW TO MAP? Next unit

---

### Unit : 4 Design app for meeting SLA
- In reality, failures will happen. Hardware can fail. The network can have intermittent timeout periods. While it's rare for an entire service or region to experience a disruption, you still need to plan for such events.
- **Identify your workloads**
- Workload is a distinct capability or task that's logically separated
```
Special Orders application will require:

Two virtual machines.
One instance of Azure SQL Database.
One instance of Azure Load Balancer.
```
- **Combine SLAs to compute the composite SLA**
- Overall application SLA requirement of 99.9 percent
- Computing the composite SLA requires that **you multiply the SLA of each individual service.**
-  Because using **multiple services adds an extra level of complexity and slightly increases the risk of failure**. - individual >= 99.9 but overall only 99.78

![image](https://user-images.githubusercontent.com/43994542/120616174-a0ecf180-c476-11eb-878d-a8e287909e18.png)


- **What happens when the composite SLA doesn't meet your needs?**
- **Choose customization options that fit your required SLA**
  - DISK (HDD, SSD, Premium SSD, Ultra Disk)
  - TIER (Free or paid)
 - **Build availability requirements into your design**
   - An availability zone - Same VM - different instances in diff availability zones
   - `Deploying two or more instances of an Azure virtual machine across two or more availability zones raises the virtual machine SLA to 99.99 percent.`
   - IN this case, adding VM to diff availability => causes Special order availability to 99.96%
 - **Include redundancy to increase availability**
   - Complex n expensive
 - **Very high performance is difficult to achieve**

---
### Unit : 5 Access Preview services and preview features
  - The research and development team is looking into new, cloud-based features that will keep them ahead of the competition.
  -  better understanding of how preview services affect its SLA.
  -  **Service LIFECYCLE**
  1. Development phase
  2. Public preview phase
  3. General Availability (GA) - after validation n testing

  - **What terms and conditions can I expect?**
  - Not for business critical
  - Separate policies
  - **How can I access new features for an existing service?**
  - accessible when you deploy, configure, and manage the service.
  - **How can I access preview features for the Azure portal?**
  - [PREVIEW PORTAL](https://preview.portal.azure.com/)

  ![image](https://user-images.githubusercontent.com/43994542/120619546-b283c880-c479-11eb-8c4e-9f5020c41747.png)

  - **Azure updates** - stay updated on latest announcements
  - RSS feed available

---
### Unit : 6 Knowledge check

![image](https://user-images.githubusercontent.com/43994542/120620250-6a18da80-c47a-11eb-8bde-f9cc51fc300c.png)

---
### Unit : 7 Summary
- SLA calculations
- Sketch and plan according to ur application
---
