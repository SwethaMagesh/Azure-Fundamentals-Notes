# [Choose the best tools for managing and configuring your Azure environment](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/)
## Module has 10 units
### Unit : Introduction
- create hundreds of resource
- programmatic creation
- rich reports and metrics
---
### Unit : Identify product options
  - Categories: **visual tools and code-based tools.**
  - The approach to managing hardware and cloud resources, which developers use when they write application code, is referred to as **infrastructure as code.**
    - This code is also versioned and reused along with app code 
  - Two approaches to infrastructure as code: **imperative code and declarative code**
  - Imperative - describe each step + Declarative - just give overall goal. interpreter will decide actions
  - Declarative is robust in largescale
  - Product options
     ```
      1. Portal : Web UI, first time users
      2. App : When away from computer; To quickly check alerts, fixes, reports; restart VM; use CLI or shell
      3. Powershell => Azure Management API?? execute cmdlets; avl in most OSes and thru browser via Azure cloud shell;
            -  cmd or script to repeat and automate; cmds call the Azure Rest API 
      4. CLI : cmd calls Rest API. Runs commands in BASH; CLI and powershell are identical except for Syntax
      5. ARM templates(Azure Resource Manager templates): declarative JSON format; verified first; parallel resource creation; can even run automated Powershell or CLI scripts thru ARM
    ```
   - Note: Powershell and CLI are imperative; ARM is declarative
---
### Unit : Analyse decision criteria
1. **Do you need to perform one-off management, administrative, or reporting actions?**
- for one-off scenarios, you may prefer more agile tools like PowerShell, Azure CLI scripts, or the Azure portal.
2. **Do you need a way to repeatedly set up one or more resources and ensure that all the dependencies are created in the proper order?**
- ARM templates
3. **When you're scripting, do you come from a Windows administration or Linux administration background?**
- Powershell / CLI
---
### Unit : 4 Portal
>Situations: 
>- Visualisation for cloud spend 
>- Both tech and executive people
---

### Unit : 5 Powershell for one off admin tasks
>Situations: 
>- strong backgrounds in Windows development and network administration.
>- The team quickly realized that managing Azure from the portal takes too much time and is not repeatable.
---
### Unit : 6 CLI for one off admin tasks
>Situations:
>- Linux dev env
>- Portal is time consuming
---
### Unit : 7 Mobile apps
>Situations:
>- the director wants to relax this requirement and allow employees to spend these dates with their families during national holidays, weekends, vacations
---
### Unit : 8 ARM template
>Situations
>- The company needs a repeatable, reliable way to scale its operations during peak sales periods
>- Is efficient and can potentially create many resources in parallel.
>- Creates all dependencies in the correct order.
>- Can be used without worrying that it failed in the middle of provisioning the necessary infrastructure.

- You could use Azure PowerShell or the Azure CLI, but these scripting technologies have significant limitations when it comes to deploying infrastructure. ARM templates can help overcome these limitations.
---
### Unit : 9 Knowledge Check
![image](https://user-images.githubusercontent.com/43994542/119621337-9f427e80-be23-11eb-85a0-c9ea3d840eb3.png)

---
### Unit : 10 Summary
- Without a full suite of management tools, the company would be severely limited in how it interacts with Azure. Fortunately, Azure provides a powerful mix of visual management tools, imperative scripting tools, and declarative infrastructure-as-code tools.
---

  
  
