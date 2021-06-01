# [Build a cloud governance strategy on Azure](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/)
## Module has 12 units
### Unit : 1 Intro
  - GOVERNANCE: rules n policies, ensure they are enforced
  - This is for compliance with 
    - Industry standards like `PCI DSS`
      - >PCI DSS means Payment Card Industry (PCI) Data Security Standard (DSS)
    - Corporate or organisational stds: EG: `Network data is encrypted`
  - NEEDED and beneficial when
    - `stds or regulatory requirements to be followed`
    - `Multiple teams, Multiple subscriptions`
  - **The company knows that these restrictions reduce team agility and the ability to innovate.**
  - How to still maintain control while allowing innovation
---
### Unit : 2 CLOUD ADOPTION FRAMEWORK for Azure
- Accelerate your cloud adoption journey by using the Cloud Adoption Framework for Azure
- **Cloud Adoption Framework for Azure**
  - consists of tools, documentation, and proven practices
  - **STAGES**
    - **Define your strategy.**
      - Motivations, outcomes, business case (ROI), right first pro
    - **Make a plan.**
      - > Digital estate: Create an inventory of the existing digital assets and workloads that you plan to migrate to the cloud.
      - Dig estate, organisational alignment, skill readiness, cloud adoption plan
    - **Ready your organization.**
      - Landing zone creation to host workload
      - Azure Setup guide, landing zone, expand, best practices
    - **Adopt the cloud.**
      - Migrate , Innovate
      - Guide, scenarios, feedback nd best practices
      - >minimum viable product **(MVP)** - INNOVATE
    - **Govern and manage your cloud environments.**
      - Govern: Methodology, benchmark, init foundation, improve
      - Manage: Baseline, business commitments, expand, operation n design
      - >**A management baseline** is the minimum set of tools and processes that should be applied to every asset in an environment.
      - 

![image](https://user-images.githubusercontent.com/43994542/120170199-5bce8280-c21e-11eb-809b-05e90043d3bd.png)


---
### Unit : 3 Subscription governance strategy
  - **Recap: Management groups, subscriptions, resource groups, resources**
  - Involves forming a **cloud center of excellence team** (also called a **cloud enablement team or a cloud custodian team**)
  - **Remember**:
    - Billing
      - > An **IT chargeback** is the practice of charging business units for their IT usage. An **IT showback** is the practice of calculating the value of IT services consumed by business units without actually charging it.  
      - These cases - new subscriptions for each dept
    - Access Control
      - Prod n dev
    - Subscription limit
      - Eg: expressroute 10 for subscription
    

---
### Unit : 4 AZURE RBAC
- **Control access to cloud resources by using Azure role-based access control**
  - 4 Scopes: MG, Subscription, Res group, Res
  - **When you grant access at a parent scope, those permissions are inherited by all child scopes**. 
  - Custom + builtin
  - Eg of types of users: **Observers, Users managing resources, Admins, and Automated processes**

![image](https://user-images.githubusercontent.com/43994542/120312272-2301dc80-c2f6-11eb-97c0-ab7e0e5cd21f.png)

  -  **How is Azure RBAC enforced?**
    -  Allow model initially - overlap allowed
    -  REST API thru ARM - 
    -  APP/ data level security not enforced  - vulnerable
  -  **Who it applies to?** - User, group, managed identity, service principal
  -  **HOW?** - IAM pane 
---
### Unit : 5 Prevent accidental changes thru resource locks
  - Even after RBAC, ppl at right level can delete inadvertently
    - _Resource locks apply regardless of **RBAC permissions**. Even if you're an owner of the resource, you must still remove the lock before you can perform the blocked activity._

![image](https://user-images.githubusercontent.com/43994542/120319268-76782880-c2fe-11eb-8f03-71721916c501.png)

  - You can manage resource locks from the **Azure portal, PowerShell, the Azure CLI, or from an Azure Resource Manager template**.
  - **Levels :** 
    - CanNotDelete or
    - ReadOnly.
  - **Azure Blue prints**
    - EG: blueprint that specifies that a **certain resource lock must exist**.
    - _Azure Blueprints can automatically replace the resource lock if that lock is removed_.
---
### Unit : 6 EX: Protect a storage accnt using resource lock
- Create resource group lock
- Try deleting
- Add storage acnt to that resource grp
- Try deleting it
- Then remove lock , delete the resource grp

- **SANDBOX WONT WORK - need ur own subscription**

---
### Unit : 7 Organise through TAGS
- **You can add, modify, or delete resource tags through PowerShell, the Azure CLI, Azure Resource Manager templates, the REST API, or the Azure portal.**
- **_POLICY:_** Very important
- Reapply tags, tags as resource is created, inherit tags etc, customised
- Usually for: 
  1. Resource management - `locate workload, env, BU or owner`
  2. Cost manage, optimise - `Budget, forecast, estimate`
  3. Operation management - `SLA - criticality of availability`
  4. Security -  `public or confidential`
  5. Governance and regulatory compliance - `industry stds`
  6. Workload optimise, automate - `devops`
---
### Unit : 8 Control n audit through policy
  - **Policy and Initiatives (groups of related policies)**
  - prevents non-compliant resources from getting created
  - **EG**: 
    1. SKU Of VM in ur subscription
    2. Tag to be reapplied
    3. DevOps for CI/CD pipelines
  - **3 steps: 1. create defn 2. Assign defn to resource 3. Evaluation results**
  - >A **policy assignment** is a policy definition that takes place within a specific scope. This scope could be a **management group (a collection of multiple subscriptions), a single subscription, or a resource group**. 
  - Normally inherited
  - But you can exclude subscope from a policy assignment
  - **Policy evaluation happens about once per hour**

---
  - **Initiatives**:
    - Azure Policy also includes initiatives that support _regulatory compliance standards such as **HIPAA and ISO 27001**._
    - EG: **Enable Monitoring in Azure Security Center**
      - 3 policies n over 100 separate policy definitions
---
### Unit : 9 EX: Restrict deployments to specific location by azure policy
  - you create a policy in Azure Policy that restricts the deployment of Azure resources to a specific location. You verify the policy by attempting to create a storage account in a location that violates the policy.
  - **SANDBOX won't work - read only policy - write access denied**

---
### Unit : 10 Govern Multiple subscriptions  AZURE BLUEPRINTS
  - Define a template of repeatable set of governance tools and standard Azure resources
  ```
  Azure Blueprints orchestrates the deployment of various resource templates and other artifacts, such as:

  Role assignments
  Policy assignments
  Azure Resource Manager templates
  Resource groups
  ```
  - **STEPS: 1. CREATE BLUEPRINT 2. ASSIGN 3. TRACK BLUEPRINT ASSIGNMENTS**
  - **Versioned** blueprints
  - Azure creates a record that associates a resource with the blueprint that defines it - preserves relationship b/w defn n assignment
  - Each component in the blueprint definition is known as an **artifact**.
  - Parameters - may or may not have
  

---
### Unit : 11 Knowledge check
![image](https://user-images.githubusercontent.com/43994542/120330951-ef7d7d00-c30a-11eb-9daa-6b866b9e7a0e.png)

---
### Unit : 12 Summary
- Azure role-based access control (Azure RBAC) enables you to create roles that define access permissions.
- Resource locks prevent resources from being accidentally deleted or changed.
- Resource tags provide extra information, or metadata, about your resources.
- Azure Policy is a service in Azure that enables you to create, assign, and manage policies that control or audit your resources.
- Azure Blueprints enables you to define a repeatable set of governance tools and standard Azure resources that your organization requires.


---
