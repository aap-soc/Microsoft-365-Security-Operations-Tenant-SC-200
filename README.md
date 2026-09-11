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
-       ├── lab1-tenant-entra-setup/           ← 19 screenshots
-       ├── lab2-e5-trial-domain/              ←  6 screenshots
-       ├── lab3-admin-accounts/               ←  13 screenshots
-       └── lab 4- standard-users/             ←  7 screenshots
-       └── lab 5- defender-xdr-alerts/        ← 14 screenshots


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
