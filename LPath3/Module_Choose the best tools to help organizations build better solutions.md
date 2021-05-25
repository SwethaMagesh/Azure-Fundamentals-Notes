# [Choose the best tools to help organizations build better solutions](https://docs.microsoft.com/en-us/learn/modules/azure-devops-devtest-labs/)
## Module 4 - has 8 units
- **Prerequisites**
	```
	Software development lifecycle
	Source-code management and version control
	The various forms of testing
	Continuous integration and continuous delivery, or CI/CD
	Continuous deployment
	Infrastructure as code
	```
### UNIT 1: Introduction
- In this module, you'll learn about the various software development process tools that Microsoft offers. You'll explore the criteria that experts use to make their choices.

- By the end of this module, you'll be able to choose the software development process tools and services that best align with your organization's goals and practices.
---
### Unit 2: Understand product options
- Microsoft offers tools to enable source-code management, continuous integration and continuous delivery (CI/CD), and automating the creation of testing environments. Sometimes, it seems as though these tools overlap in functionality
```
- DevOps is a new approach that helps to align technical teams as they work toward common goals. 
- To accomplish this alignment, organizations employ practices and processes 
- These seek to automate the ongoing development, maintenance, and deployment of software systems. 
- Their aim is to expedite the release of software changes, ensure the ongoing deployability of the system, 
- ensure that all changes meet a high quality bar.

- When done correctly, DevOps practices and processes touch nearly every aspect of the company, 
- not to mention the software development lifecycle,
		- including planning, project management, and the collaboration of software developers with each other and 
		- with operations and quality assurance teams.
- Tooling automates and enforces most of the practices and processes, making it both difficult and unnecessary to work around.

- DevOps requires a fundamental mindset change from the top down.
- Organizations can't merely install software tools or adopt services and hope to get all of the benefits promised by DevOps.
```
---
- **DevOps Services**
	1. Repos
	2. Boards
	3. Pipelines
	4. Artifacts
	5. Test Plans
	- _began as on-premises server software and evolved into a software as a service (SaaS) offering from Microsoft._

---
- **GitHub and GitHub Actions**
	- **Functions**:
		- It's a shared source-code repository, including tools that enable developers to perform code reviews by adding comments and questions in a web view of the source code before it can be merged into the main code base.
		- It facilitates project management, including Kanban boards.
		- It supports issue reporting, discussion, and tracking.
		- It features CI/CD pipeline automation tooling.
		- It includes a wiki for collaborative documentation.
		- It can be run from the cloud or on-premises

	-  GitHub Actions enables **workflow automation with triggers** for many lifecycle events. One such example would be automating a CI/CD toolchain.
	> A toolchain is a combination of software tools that aid in the delivery, development, and management of software applications throughout a system's development lifecycle. 
	The output of one tool in the toolchain is the input of the next tool in the toolchain. 
	Typical tool functions range from performing automated dependency updates to building and configuring the software, delivering the build artifacts to various locations, testing, and so on.

- NOTE:1 - Azure DevOps and GitHub allow public and private code repositories
- NOTE:2 - Your choices are not limited to Azure DevOps Services or GitHub and GitHub Actions. In practice, you can mix and match these services as needed. For example, you can use GitHub repos with Azure Boards for work item tracking.

|Github|Azure DevOps|
|---|---|
|focus on individual developers n public repos n open source|focus on enterprise development|
|light weight tool|heavier project-management and planning tools, and finer-grained access control.|

- **Azure DevTest Labs**


	- automated build, setup, tear down of VM
	- Test in variety of env n builds
	- Anything you can deploy in Azure via an ARM template can be provisioned through DevTest Labs
	- Huge time saver - precreated lab env
	- Saves money - shut down when not used - we can manage the labs, how long they run n so on

---
### Unit 3: Analyse decision criteria
1. **Do you need to automate and manage test-lab creation**? - _Use Azure DevTest Labs - (but toolchain workflow in others too possible beware)_
2. **Are you building open-source software**? - _GitHub_
3. **Regarding source-code management and DevOps tools, what level of granularity do you need for permissions**? - _Azure DevOps has a much more granular set of permissions that allow organizations to refine who is able to perform most operations across the entire toolset._
4. **Regarding source-code management and DevOps tools, how sophisticated does your project management and reporting need to be**? - _Azure DevOps - reporting and categorising by collection of metadata - (GitHub has kanban board and used tags to categorise issues)_
5. **Regarding source-code management and DevOps tools, how tightly do you need to integrate with third-party tools**? - _DevOps tools create hooks or APIs that can be used by both Azure Pipelines and GitHub Actions. Even so, it's probably worth the effort to validate that assumption._ 

---
### Unit 4: Use Azure DevOps
> situations : 
> The team needs to give project sponsors and managers executive level reporting, including burndown charts, track progress against epics, and track custom information that's specific to Tailwind Traders in each work item and bug report.

>As Tailwind Traders grows and hires contractors and outside vendors for short-term work, the upper management team wants to ensure that these individuals have access only to the information they need to do their work.
---
### Unit 5: Use GitHub
> Although the internal implementation of the API is closed source, Tailwind Traders wants to create a set of examples that call the API to perform various actions. The team needs a platform to share example code, collect feedback on the API, allow contributors to report issues, and build a community around feature requests.
---
### Unit 6: Use Azure DevTest Labs
> The management team has concerns around the costs of a more automated test environment. For instance, it wants to make sure that the QA professionals are not wasting time configuring the testing environment to match the production environment. The team wants to ensure that the VMs are destroyed when they're no longer in use. It wants to limit the number of VMs that each QA professional is allowed to spin up. Also, the team wants to ensure that each environment is configured correctly and consistent with the production environment.
---
### Unit 7: Knowledge check
![image](https://user-images.githubusercontent.com/43994542/119539140-7e3d4780-bda9-11eb-852e-baf15fb129fb.png)

---
### Unit 8: Summary
- Without software development services and tools from Microsoft, the Tailwind Traders team might have difficulty in realizing the benefits of such DevOps practices as continuous integration and continuous delivery (CI/CD), source-code management, and work-item management.
---
