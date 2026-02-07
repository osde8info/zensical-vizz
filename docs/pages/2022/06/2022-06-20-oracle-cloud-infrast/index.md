---
title: "Oracle Cloud Infrastructure #OCI Identity - Rotate Credentials Required"
date: 2022-06-20
categories: 
  - "vizz"
---

Oracle _has identified security vulnerability CVE-2022-21503 that affected the Oracle Cloud Infrastructure (OCI) Identity service. This vulnerability has received a CVSS base score of 4.9. Oracle has completed patching activities in response to this issue. However, you must take additional actions before July 18, 2022. Failure to complete these steps can cause outages to your cloud services._

_You must rotate all affected credentials of the following types:  
• Console UI passwords  
• SMTP credentials  
• OAuth 2.0 client credentials  
• Auth tokens  
• Customer secret keys  
• MFA TOTP device seeds  
• IdP client credentials where the identity provider is other than Oracle IDCS_
