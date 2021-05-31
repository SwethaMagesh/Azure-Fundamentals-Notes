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

---

- **What services does Azure AD provide?**
  - Authenticate
    - `self-service password reset, multifactor authentication, a custom list of banned passwords, and smart lockout services`
  - SSO
    - one username and one password to access multiple applications
  - App manage
    - `Application Proxy, SaaS apps, the My Apps portal (also called the access panel), SSO`
  - Dev manage
    - tools like **Microsoft Intune**
    - **Device-based conditional access policies** - even if user account is authentic, if device is not known, access denied
   
---

- **What kinds of resources can Azure AD help secure?**
  1. External : **SaaS - MS Office 365, Azure portal**
  2. Internal : **apps on corporate net, intranet, cloud apps in organisation**

- **SSO** - _only one ID and one password_
    - Use one time sign in = in **multiple resource and app from different providers**
    - The more passwords a user has to manage, the greater the risk of a credential-related security incident
    - **Helps reduce strain on help desk** - deal with account lockouts and password reset requests

---

- **How can I connect Active Directory with Azure AD?** 
  - To provide consistent identity experience to users
  - To connect : **use Azure AD Connect**
    - syncs UID b/w onprem Active dir and Azure AD
    - Features like SSO, Multifactor Auth, passwd reset allowed in both
      - `Self-service password reset prevents users from using known compromised passwords.`

![image](https://user-images.githubusercontent.com/43994542/120160426-dd6ce300-c213-11eb-8b01-1f1cf512a018.png)

- **Benefit of connecting Active dir with Azure AD**
  - simplifies its ability to sign in to different applications, manage changes to user identities and control, and monitor and block unusual access attempts.


---
### Unit 4: Multifactor Authentication and Conditional access
- **What's multifactor authentication?**
- _EG: a code on their mobile phone or a fingerprint scan._
- **1. User knows (pwd) 2. User has (otp) or 3. User is (biometry)**

- **What's Azure AD Multi-Factor Authentication?**
  - MS Service
  - Eg of extra auth: such as a phone call or mobile app notification.
  - Service providers
    - Azure AD
        -  for administrators with the global admin level of access
        -  Thru MS Authenticator app, SMS, phone call
        -  Security defaults in AAD Tenant: Set only thru app etc.
        -  Conditional Access policy -> **premium P1 or P2 license alone**
    - MF auth for Office 365

---
- **CONDITIONAL ACCESS**
  - allow (or deny) access to resources based on identity signals
  - **SIGNALS**:
    - Who he is 
    - Where he is : location 
    - What device he is requesting from
    - What application that the user is trying to access.
  - **GRANULAR Multifactor Auth**
  - Eg: 2 factor only if unusual signin or unexpected location
  - **Enforcement** is the action that carries out the decision. For example, the action is to allow access or require the user to provide a second form of authentication.

![image](https://user-images.githubusercontent.com/43994542/120163707-6a656b80-c217-11eb-819c-d4b404f033bb.png)

- **When can I use Conditional Access?**
  - Multi factor auth
    - _Config: Whether all users or only certain admins, also whether all networks or only untrusted nets_
  - Access through approved client app only
    - _Eg: Access Office 365 thru Outlook mobile app only_  
  - Only from managed dev
    - _dev which meets stds for security and compliance_
  - Block untrusted sources
    - _unknown locations_ 

- **What If tool**
  - plan n troubleshoot Access policies
  - Model recent signin attempts n check **what if enabled**
  - **To test conditional access policy before implement**

- **Conditional access availability**
  - Azure AD Premium P1 or P2 license
  - MS 365 Business Premium License
  
---
### Unit 5: Knowledge check

![image](https://user-images.githubusercontent.com/43994542/120164861-a0571f80-c218-11eb-8341-3abe7c09db98.png)

---
### Unit 6: Summary
  - AuthN
  - AuthZ
  - SSO
  - AAD
  - AAD MF authentication
  - Conditional access
---
