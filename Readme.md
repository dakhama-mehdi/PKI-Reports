<div align="left">
  <h1 style="display: flex; align-items: center; justify-content: space-between;">
    <img src="https://raw.githubusercontent.com/dakhama-mehdi/PKI-Reports/main/Logo/Logo_PKI.png" alt="PKIReports" width="250" height="150" style="margin-left: 20px;" />
    PKIReports : One command for all you want``
  </h1>
</div>


🚧 **Work in Progress** 🚧  
PKI-Stats is a lightweight PowerShell module designed to provide **monitoring and reporting** for Microsoft Certification Authorities (CAs).  
It focuses purely on **statistics and dashboards** (delivered, expired, soon-to-expire certificates, top templates, etc.) — **no security audit** is included.

---
Examples : https://dakhama-mehdi.github.io/PKI-Reports/Examples/Pkireports.html
## ✨ Features

- Global statistics:
  - Total issued, active, expired, revoked
  - Certificates expiring soon (7 / 30 / 90 days)
- Top 5 statistics:
  - Most frequently used certificate templates
  - Recently issued certificates
- Export options:
  - HTML dashboard (via [PSWriteHTML](https://github.com/EvotecIT/PSWriteHTML))
  - JSON / CSV raw data
- Multiple CA servers support (enumerated from AD)

---

## 📦 Installation (WIP)

Clone the repository and import the module locally:

```powershell
git clone 
cd PKI-Stats/src
Import-Module ./PKI.Stats.psd1 -Force
