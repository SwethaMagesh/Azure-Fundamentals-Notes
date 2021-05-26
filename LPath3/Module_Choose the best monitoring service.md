# [Choose the best monitoring service for visibility, insight, and outage mitigation](https://docs.microsoft.com/en-us/learn/modules/monitoring-fundamentals/)
## Module has 8 units

### Unit : 1 Introduction
  - React quickly to outages,
  - research intermittent issues, 
  - optimize your usage, and
  - be proactive in handling future planned downtime.
  - Tailwind needs: _optimize its cloud spend and security posture to tracking intermittent issues and planning ahead for upcoming outages._
  
---
### Unit : 2 Identify product options
- Common functions:
  - Gain answers, insights, and alerts to help ensure that you've optimized your cloud usage.
  - Ascertain the root cause of unplanned issues.
  - Prepare ahead of time for planned outages.
- **Product options**
  - **_Azure Advisor_**
    - Suggested actions you can take right away, postpone, or dismiss
    - Recommend based on evaluations
    - Via the **Azure portal and the API**, and you can **set up notifications** to alert you to new recommendations.
     ```
    - Reliability: Used to ensure and improve the continuity of your business-critical applications.
    - Security: Used to detect threats and vulnerabilities that might lead to security breaches.
    - Performance: Used to improve the speed of your applications.
    - Cost: Used to optimize and reduce your overall Azure spending.
    - Operational Excellence: Used to help you achieve process and workflow efficiency, resource manageability, and deployment best practices.
    ```
  - _**Azure Monitor**_
    - For collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire Azure and on-premises environment.
    - You can view high-level reports on the **Azure Monitor Dashboard or create custom views by using Power BI and Kusto queries**.
    - React to critical events in real time, through alerts delivered to teams via SMS, email,
    - Thresholds to trigger autoscaling functionality to scale up or down to meet the demand
    - _**Azure Application Insights**_ : used Monitor under hood; wide variety of insights from app code; finds and diagnoses error before user reports

  ![image](https://user-images.githubusercontent.com/43994542/119626085-7a9cd580-be28-11eb-881a-e5e231319d9c.png)

  - **_Azure Service Health_**
    - provides a personalized view of the health of the Azure services, regions, and resources
    - >Azure Service Health notifies you about Azure service incidents and planned maintenance so you can take action to mitigate downtime. Configure customisable cloud alerts and use your personalised dashboard to analyse health issues, monitor the impact to your cloud resources, get guidance and support, and share details and updates.
    - >Personalised dashboard shows the service issues that affect you ;
    - >Configurable cloud alerts notify you about active and upcoming service issues;
    - >Shareable details and updates, including incident root cause analyses;
    - >Guidance and support during service incidents
    - `status.azure.com website` doesn't provide all details
    - After an outage, Service Health provides official incident reports, called root cause analyses (RCAs), which you can share with stakeholders.
    - Event types: 1. Service issues 2. Planned maintenance 3. Health advisories

 
---
### Unit : 3 Analyse decision criteria
- **Do you need to analyze how you're using Azure to reduce costs? Improve resilience? Harden your security?**
  - `Azure Advisor` when you're looking for an analysis of your deployed resources.
- **Do you want to monitor Azure services or your usage of Azure?**
  - AZURE services => `Service Health`; UR VMs and other => `Monitor`
- **Do you want to measure custom events alongside other usage metrics?**
  - `Azure Monitor` when you want to measure custom events alongside other collected telemetry data
- **Do you need to set up alerts for outages or when autoscaling is about to deploy new instances?**
  - `Azure Monitor` for alert to ur specific resources
---
### Unit : 4 Azure Advisor - PRIMARILY OPTIMISATION SUGGESTIONS
> Tailwind Traders understands that it might be spending too much, is concerned about its security practices, and wants to have its cloud usage analyzed against industry best practices
---
### Unit : 5 Azure Monitor
> The Tailwind Traders e-commerce website is experiencing intermittent errors, and the team is unsure of the cause. Because of the nature of the errors, the team suspects that it's either a database or caching issue. What are the circumstances surrounding the errors? Does it happen only during peak usage times? What is the state of the team's Azure SQL instance? What is the state of its Redis caching server? How can it trace the issues to a root cause?
---
### Unit : 6 Azure service Health
>Team wants to let stakeholders know about upcoming planned downtime in advance. The team also wants its solution architects to be forewarned about any Microsoft plans to sunset services so it can rearchitect its software products accordingly.
>When outages do happen, the team wants to quickly ascertain whether the issue is specific to their services or a service interruption that affects many Azure customers. The team also wants to provide key stakeholders with reports that explain how and why the incident occurred, and so on.
---
### Unit : 7 Knowledge check
![image](https://user-images.githubusercontent.com/43994542/119629481-ac636b80-be2b-11eb-9b6c-e4af73476d84.png)

---
### Unit : 8 Summary
- Without monitoring services, Tailwind Traders would spend more money on its cloud environment, be unsure about its cloud security posture, have difficulty pinpointing issues in its application logic, and be unable to plan ahead for outages or supply formal outage reports to stakeholders.
---
