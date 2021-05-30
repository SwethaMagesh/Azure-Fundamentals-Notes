# [Secure access to your applications by using Azure identity services](https://docs.microsoft.com/en-us/learn/modules/secure-access-azure-identity-services/)

## Module has 6 units

### UNIT 1: Intro
- BYOD strategy
- Identity - new security boundary
- Employees : Retail, Delivery drivers - long term , short term contract ==> IDENTITY
- ACTIVE DIR - Azure AD
- **Objectives**: 
  - Explain the difference between authentication and authorization.
  - Describe how Azure AD provides identity and access management.
  - Explain the role that single sign-on (SSO), multifactor authentication, and Conditional Access play in managing user identity.
---
### Unit 2: Compare Authentication, Authorisation
- Authentication (AuthN) and Authorization (AuthZ).
- **Authenticate**: _Is user who he says he is_
- **Authorise**: Level of access: ie.  _what data they're allowed to access and what they can do with it._

![image](https://user-images.githubusercontent.com/43994542/120116568-57ff1980-c1a6-11eb-90cd-8f2c2ee8bb91.png)


---
### Unit 3: Azure Active Directory
- SSO - Single Sign On
- **How does Azure AD compare to Active Directory?**

|Active Dir| Azure AD|
|---|---|
|MS introduces in Win 2000 |Microsoft's cloud-based identity and access management service|
|Microsoft doesn't monitor sign-in attempts.|protect you by detecting suspicious sign-in attempts at no extra cost. eg: **unknown locations or unexpected IPs**|
|To manage multiple onprem infra system, components using **Single identity per user**|If you've worked with Active Directory, Azure AD will be familiar to you.|
|Identity and access management service that's managed by your own organization.| you control the identity accounts, but Microsoft ensures that the service is available globally|

- **Who uses Azure AD**
  - IT admin
  - App developers
  - Users
  - Online service subscribers 
    - **Microsoft 365, Microsoft Office 365, Azure, and Microsoft Dynamics CRM Online subscribers are already using Azure AD.**
    - **_A tenant is a representation of an organization. A tenant is typically separated from other tenants and has its own identity._**
    - Service tenent is now an Azure AD tenant

- **What services does Azure AD provide?**
  - Authenticate
  - SSO
  - App manage
  - Dev manage




---
### Unit 4: Multifactor Authentication and Conditional access
---
### Unit 5: Knowledge check
---
### Unit 6: Summary
---
