### 🛡️Microsoft-365-Security-Tenant SC-200 - Using Microsoft 365 E5 & Entra ID
- **Focus**: Security Operations | Identity & Access Management | Microsoft Defender XDR
- **Environment**: Microsoft 365 E5 Trial | Microsoft Entra ID | Default Directory
- **Date**: 2026
- **Author**: Andre Patterson

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📋 Overview

I present a hands-on Microsoft 365 security operations lab, built as part of Microsoft's SC-200 (Security Operations Analyst) curriculum, completed during an active transition into Cloud Security and SOC Engineering. 
Each lab stands up a real, working Microsoft 365 E5 tenant and applies core security operations practices: identity separation of duties, least-privilege user provisioning, and centralised security alerting.

All labs were completed live in the Microsoft 365 admin center and Microsoft Defender XDR portal on an E5 trial tenant. Every step is documented with screenshots as verifiable evidence of hands-on configuration.

**Evidence integrity**: Screenshots are taken from completed console work and have been sanitised for a public GitHub repository. Domain names, tenant identifiers, and other identifying information are redacted.

**Project objective**

Build a small Microsoft 365 security operations baseline that applies four core practices:

1. Identity foundation through a Microsoft 365 E5 tenant and Entra ID.
2. Separation of duties through distinct Global Administrator and Security Administrator roles.
3. Least privilege through standard user accounts with no administrative access.
4. Centralised alerting through Microsoft Defender XDR incident notification rules.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🗂️ Repo Structure

  
    Microsoft-365-Security-Tenant SC-200/
- │
- ├── README.md                        ← Project overview
- ├── docs/
- │   └── lab-notes.md                 ← Step-by-step notes mirroring every screenshot
- └── screenshots/
-       ├── lab1-tenant-entra-setup/           ←  10 screenshots
-       ├── lab2-e5-trial-domain/              ←   3 screenshots
-       ├── lab3-admin-accounts/               ←  12 screenshots
-       └── lab 4- standard-users/             ←   7 screenshots
-       └── lab 5- defender-xdr-alerts/        ←  11 screenshots


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧠 Why These Services Matter in Security Operations 

|               **Service**                        |                  **Security Purpose**                        |                                     Real-World Use                                                    |                                 
|--------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
|         **Entra ID Tenant Setup**                |  Establishes the identity foundation for every other control | Every Microsoft 365 security control (Defender, Purview, Intune) is built on top of Entra ID identity |                
|                                                  |                                                              |                                                                                                       |
|  **Global Admin / Security Admin Separation**    |    Restricts full tenant control to a dedicated account      |     Prevents a compromised security-operations login from becoming a full tenant takeover             |       
|                                                  |                                                              |                                                                                                       |
|     **Least-Privilege Standard Users**           |       Ensures regular accounts carry no admin rights         |       Limits blast radius if a standard user's credentials are phished or compromised                 |
|                                                  |                                                              |                                                                                                       |
|   **Defender XDR Incident Notifications**        | Auto routes medium/high severity alerts to the right people  |            Primary mechanism for ensuring security incidents are seen and actioned promptly           |




-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## ✅ Labs Completed

### Lab 1 - Microsoft 365 Tenant & Entra ID Setup

Establishing the tenant and navigating Microsoft Entra ID, the identity foundation for every later lab.

**What I configured:**
- Created a Microsoft 365 tenant and navigated to Microsoft Entra ID
- Reviewed the Entra ID admin center layout (Users, Groups, Roles)
- Created the first administrative user account with console access
- Assigned the Global Administrator directory role via Assignments → Add role
- Reviewed and confirmed the new admin account on the Review + create screen

**Key security concepts:**
- Entra ID as the identity backbone underneath every Microsoft 365 security control
- Directory roles vs. license assignment as two separate, distinct concepts
- Reviewing changes before committing (Review + create pattern)

📁 **Screenshots → screenshots/lab1-tenant-entra-setup/ 📄 Step-by-step notes → docs/lab-notes.md#lab-1**


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Lab 2 - Microsoft 365 E5 Trial & Domain Configuration

Provisioning the E5 licence that unlocks Defender, Sentinel integrations, and other security tooling used in later labs.

**What I configured:**
- Started a Microsoft 365 E5 trial via Marketplace → Microsoft 365 E5 → Start free trial
- Verified the E5 licence appeared under Billing → Licences

**Key security concepts:**
- Licence tier as the gatekeeper for which security products are available (Defender XDR, Sentinel integrations require E5)
- Domain configuration as a prerequisite for realistic identity and email security testing

📁 **Screenshots → screenshots/lab2-e5-trial-domain/ 📄 Step-by-step notes → docs/lab-notes.md#lab-2**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Lab 3 - Administrative Account Separation of Duties

Creating two distinct administrative accounts rather than one all powerful login, mirroring the admin/user key separation pattern.

**What I configured:**
- Created **Lab Admin_1**, assigned a Microsoft 365 E5 licence, and granted the **Global Administrator** role
- Created a dedicated **Security Analyst** account, assigned an E5 licence, and granted the **Security Administrator** role — providing access to Microsoft security products without full tenant-wide administrative rights
- Confirmed both accounts appeared as Active users with correct licence and role assignments

**Key security concepts:**
- Separation of duties between full tenant administration (Global Administrator) and security-specific administration (Security Administrator)
- Role-based access aligned to job function, not a single shared admin login
- Least privilege applied to administrative accounts, not just standard users

📁 **Screenshots → screenshots/lab3-admin-accounts/ 📄 Step-by-step notes → docs/lab-notes.md#lab-3**


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Lab 4 - Standard User Provisioning (Least Privilege)

Provisioning regular employee accounts with no administrative rights, to simulate a realistic organisation for later investigation and detection exercises.

**What I configured:**
- Created standard user **John Smith** with a Microsoft 365 E5 licence and **User (no admin center access)** selected
- Created four additional standard user accounts following the same least-privilege pattern
- Confirmed all standard accounts appeared as Active users with no administrative roles assigned

**Key security concepts:**
- Least privilege as a default, not an afterthought - standard users get no admin center access by design
- Standard accounts as the realistic baseline needed for future sign-in activity, device enrolment, and attack-simulation exercises

📁 **Screenshots → screenshots/lab4-standard-users/ 📄 Step-by-step notes → docs/lab-notes.md#lab-4**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Lab 5 - Microsoft Defender XDR: Incident Alert Notifications

Configuring automated email alerting so that security-relevant incidents reach the right people without manual checking.

**What I configured:**
- Navigated to Microsoft Defender XDR via Settings → Microsoft Defender XDR → Email notifications
- Created a new incident notification rule via + Add incident notification rule
- Scoped the rule to **Medium** and **High** severity incidents, balancing coverage of important incidents against alert fatigue
- Added the admin address as a notification recipient
- Reviewed and submitted the rule, confirming it was created successfully

**Key security concepts:**
- Severity-based alert routing to avoid both under-alerting (missing real incidents) and over-alerting (notification fatigue)
- Defender XDR as a unified alerting layer across Microsoft's security stack
- Notification rules as a foundational SOC practice — an undetected incident with no alert is functionally the same as no detection at all

📁 **Screenshots → screenshots/lab5-defender-xdr-alerts/ 📄 Step-by-step notes → docs/lab-notes.md#lab-5**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### 🚧 Lab 6 – Microsoft Defender for Endpoint (In Progress)

Currently extending this tenant into Microsoft Defender for Endpoint as part of ongoing SC-200 coursework. This section will be updated with screenshots and notes as the lab is completed.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 📚 Key Security Concepts Demonstrated

- **Identity as the foundation** - every Microsoft 365 security control sits on top of Entra ID
- **Separation of duties** - Global Administrator and Security Administrator are distinct accounts with distinct purposes
- **Least privilege by default** - standard users are provisioned with no administrative access from the start
- **Severity-based alerting** - Defender XDR notification rules scoped to Medium/High to balance coverage against noise
- **Change review discipline** - using Review + Create style confirmation steps before committing configuration changes

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔗 Related Projects

- 🔐 AWS Security Controls Lab (https://github.com/aap-soc/AWS-Security-Controls-Lab)
- 🖥️ Virtualisation Lab - Ubuntu on VirtualBox (https://github.com/aap-soc/Virtualisation-Lab)
- 🔐 Linux Security & Log Handling Portfolio (https://github.com/aap-soc/linux-security-portfolio)

