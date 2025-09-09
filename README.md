# 🛡️ bWAPP Pentesting Report

This repository contains the results of a web application security assessment conducted on the intentionally vulnerable **bWAPP** application, hosted at [http://www.itsecgames.com](http://www.itsecgames.com). 

## 📌 Assessment Objectives

- Identify vulnerabilities, outdated software, and CVEs.
- Detect misconfigurations and missing security headers.
- Assess SSL/TLS configuration and certificate strength.
- Highlight any exposed information that could aid attackers.
- Provide a prioritized remediation roadmap.

## 📄 Final Report

The full report with detailed findings, impact analysis, and remediation steps is available here:

🔗 [`bWAPP_Pentesting_Report_Sachin_Mishra.pdf`](./Final_Report/bWAPP_Pentesting_Report_Sachin_Mishra.pdf)


## 🧪 Tool Reports

All testing was performed using publicly available tools, in line with OWASP and PTES standards.

| Tool         | Description                                 | Report File |
|--------------|---------------------------------------------|-------------|
| **Nmap**     | Network/port scan, version detection        | [`nmap_results.txt`](./Tool_Reports/nmap_results.txt) |
| **Nikto**    | Web server vulnerability scan               | [`nikto_report.txt`](./Tool_Reports/nikto_report.txt) |
| **SSLScan**  | SSL/TLS protocol and cipher analysis        | [`ssl_report.txt`](./Tool_Reports/ssl_report.txt) |
| **OWASP ZAP**| Dynamic application security testing (DAST) | [`HTML Report`](./Tool_Reports/2025-09-08-ZAP-Report-.html), [`ZAP Export`](./Tool_Reports/2025-09-08-ZAP-Report-.zip) |


## 🛠️ Methodology

The assessment followed industry standards and used the following phases:

1. **Reconnaissance & Enumeration** – Service discovery using Nmap.
2. **Vulnerability Scanning** – Web server scanning via Nikto and OWASP ZAP.
3. **SSL/TLS Analysis** – Protocol/cipher inspection using SSLScan.
4. **Manual Verification** – Reviewed findings against known CVEs and OWASP Top 10.


## 🧯 Key Findings (Summary)

| Risk Level | Issues Identified |
|------------|--------------------|
| Critical   | Outdated Drupal 7 CMS |
| High       | Outdated OpenSSH version |
| Medium     | Missing security headers (CSP, X-Frame-Options) |
| Low        | Apache default files exposed, MIME sniffing not disabled |
| Informational | TLS 1.3 disabled, inconsistent user-agent responses |

See full details in the [PDF report](./Final_Report/bWAPP_Pentesting_Report_Sachin_Mishra.pdf).


## 🛡️ Recommendations

- Restrict access to vulnerable applications (e.g., internal only or behind VPN).
- Upgrade outdated software (Drupal, OpenSSH).
- Apply missing HTTP security headers.
- Enable TLS 1.3 and enforce HSTS.
- Clean up server misconfigurations and exposed files.
- Regularly conduct vulnerability assessments.


## 📅 Date of Assessment

**September 2025**


## 👨‍💻 Author

**Sachin Mishra**  
Security Officer Trainee  
Email: _sachinrmishra3@gmail.com_  
GitHub: [github.com/sachinrmishra](https://github.com/sachinrmishra)


## 📚 References

- OWASP Top 10 (2021)
- OWASP Testing Guide v4
- SSL Labs Best Practices
- CVE Database
