<table style="width:100%;">
<tr>
<td style="vertical-align: middle;">
<img src="https://raw.githubusercontent.com/dakhama-mehdi/PKI-Reports/main/Logo/Logo_PKI.png" alt="PKIReports" width="250" height="150">
</td>
<td align="right" style="vertical-align: middle;">
<h1>One command for all you want</h1>
</td>
</tr>
</table>

> PKIReports is a modern PowerShell module designed to build a complete and visual inventory of your AD CS servers, simplifying the management and understanding of your PKI infrastructure.  
>  
> With just **ONE COMMAND**, it generates a **comprehensive report in minutes** analyzing issued and revoked certificates, identifying trends, and providing a clear view of PKI activities  ideal for **monitoring, project tracking, administration, and capacity planning**.


---
Examples : https://dakhama-mehdi.github.io/PKI-Reports/Examples/Pkireports.html

## ✨ Features

| | |
|-----------|----------|
| **Global statistics** | Total issued, active, expired, revoked · Certificates expiring soon (7 / 30 / 90 days) · Certificate templates overview · Signature and key algorithms used |
| **Certificate & CRL health** | Validity and next update date of each CA's CRL · CRL publication point reachability · Detection of expired or missing CRL files · CA availability and service status |
| **Top statistics** | Most frequently used certificate templates · Most active requesters (users, computers, services) · Top revoked certificates (by reason or template) · Top failed requests (by error or status code) |
| **Issued & Revoked insights** | Daily issued / revoked trends · Issuance and revocation reasons · Temporal view (last 15 days) · Process name and requester correlation |
| **Multiple CA servers support** | Automatic enumeration from Active Directory · Parallel data collection · Consolidated metrics |

## 🚀 Installation

```powershell
Install-Module PKIReports -Scope CurrentUser -Force
````
## How tu use 

```powershell
Invoke-Pkireports
````

## 🧱 Prerequisites

- A machine joined to the domain (Windows Server or Windows 10/11)
- An account with at least **read permissions** on the Certification Authority server(s)

## 🛠️ Parameters

| Parameter      | Description |
|----------------|-------------|
| `SavePath`    | Directory where all reports will be exported (HTML, CSV, JSON). Useful for monitoring or serving via web server. **Example**: `-SavePath C:\Temp\PKIReports` |
| `ComputerName`| One or more specific CA servers to target. If not specified, all CAs in AD will be queried.<br>**Example**: `-ComputerName CA-1.info.lab,CA-2.info.lab` |
| `MaxSearch`   | Limit the number of certificates processed per CA (useful for testing or performance).<br>**Example**: `-MaxSearch 1000` |
| `ExportCSV`   | Export only the soon-to-expire certificates to a standalone CSV file (used with `-MaxDaysLeft`).<br>**Example**: `-ExportCSV C:\Temp\export.csv -MaxDaysLeft 7` |
| `Silent`      | Do not open the generated HTML report in the browser. Useful for Task Scheduler or automated environments. |
| `NoHtml`      | Skip HTML dashboard generation (combine with `-ExportCSV` for headless use). |

## 🤝 Contact & Contribution

Feel free to contact us for any **PKI-related project support**, including deployment of the solution on a web server with daily reporting.

Your **donations, suggestions, or contributions** help us improve PKIReports and bring new features to the community.

📧 Contact: [pkireports@outlook.fr](mailto:pkireports@outlook.fr)

---

## 📦 Dependencies

This module relies on the following PowerShell libraries:

- [`PSPKI`](https://github.com/PKISolutions/PSPKI) – for interacting with Microsoft Certification Authorities
- [`PSWriteHTML`](https://github.com/EvotecIT/PSWriteHTML) – for generating dynamic HTML dashboards and tables

---

## ⚖️ License

> ❗ **Strictly non-commercial license**

- Free to use for **end-users only**  
- **Commercial usage, resale, or deployment by third-party providers** is strictly prohibited without permission  
- For professional use or integration in a commercial environment, please contact us

---

## 🙏 Acknowledgements

Special thanks to contributor: **Hassene Saadi**


