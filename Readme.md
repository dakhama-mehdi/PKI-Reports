<table style="width:100%;">
<tr>
<td style="vertical-align: middle;">
<img src="https://raw.githubusercontent.com/dakhama-mehdi/PKI-Reports/main/Logo/Logo_PKI.png" alt="PKIReports" width="250" height="150">
</td>
<td align="right" style="vertical-align: middle;">
<h1>PKIReports : One command for all you want</h1>
</td>
</tr>
</table>

> **PKIReports** is a modern PowerShell module designed to **generate a complete and visual inventory** of your AD CS servers, simplifying the management and understanding of your PKI infrastructure.  
>  
> Built to address the growing need for **clear visibility and automation in PKI environments**, PKIReports helps administrators, auditors, and engineers gain instant insights into their certification authorities.  
>  
> With just **ONE COMMAND**, it generates a **comprehensive report in minutes** — analyzing issued and revoked certificates, identifying trends, and providing a clear view of PKI activities — ideal for **monitoring, project tracking, administration, and capacity planning**.


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
