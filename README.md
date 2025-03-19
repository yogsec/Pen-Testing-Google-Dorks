# Pen Testing Google Dorks




Pen Testing Google Dorks contains an extensive list of **Google Dorks** that can be used for penetration testing, security research, and information gathering. Google Dorking (or Google Hacking) is a technique that leverages advanced search queries to find sensitive information, exposed directories, login pages, vulnerable files, and more.

> **Disclaimer:** This project is for educational and ethical hacking purposes only. Always obtain proper authorization before testing on any system.

## 📌 Features

- Categorized Google Dorks for different penetration testing use cases.
- Regularly updated with new dorks.
- Useful for **Bug Bounty Hunting**, **OSINT**, and **Reconnaissance**.
- Includes search queries for finding **exposed credentials**, **admin panels**, **sensitive files**, and more.

## 📖 How to Use

1. Open **Google** (or any search engine that supports advanced queries).
2. Copy a dork from the list and paste it into the search bar.
3. Modify the query as needed to target specific domains or file types.

Example:
```bash
intitle:"index of" "admin"
```
This query finds open directories with the keyword "admin" in the title.

---

# 🔍 Google Dorks for Pen Testing Vulnerabilities

This repository contains a list of **30 powerful Google Dorks** that help security researchers identify vulnerabilities in websites. These dorks can reveal **sensitive files, login portals, credentials, outdated software, and misconfigurations** that may pose security risks.

> **Disclaimer:** Use these dorks only for ethical hacking and penetration testing with proper authorization.

## 🚀 Google Dorks List

### 🔍 **Finding Exposed Files & Directories**  
```bash
intitle:"index of" site:example.com
```
Lists open directories.  
```bash
site:example.com ext:log | ext:txt | ext:conf
```
Finds log, text, and config files.  
```bash
site:example.com ext:sql | ext:db
```
Searches for exposed database files.  
```bash
site:example.com inurl:backup | inurl:old | inurl:bak
```
Finds backup files.  
```bash
site:example.com intitle:"Index of /" "password"
```
Searches for password files.  

### 🔑 **Finding Sensitive Credentials**  
```bash
site:example.com inurl:wp-config.php
```
Finds WordPress config files with database credentials.  
```bash
site:example.com filetype:env "DB_PASSWORD"
```
Searches for exposed `.env` files.  
```bash
site:example.com "password" filetype:xls | filetype:csv | filetype:txt
```
Looks for passwords in documents.  
```bash
site:example.com "API_KEY" | "secret" | "token"
```
Detects leaked API keys or tokens.  
```bash
site:example.com intext:"password="
```
Finds hardcoded passwords in source code.  

### 🔒 **Finding Login Pages & Admin Panels**  
```bash
site:example.com inurl:admin
```
Finds admin login pages.  
```bash
site:example.com inurl:login
```
Searches for login pages.  
```bash
site:example.com intitle:"admin login"
```
Finds admin authentication portals.  
```bash
site:example.com inurl:"phpmyadmin" | intitle:"phpmyadmin"
```
Searches for phpMyAdmin panels.  
```bash
site:example.com inurl:dashboard
```
Detects exposed dashboards.  

### 🔍 **Detecting Web Vulnerabilities**  
```bash
site:example.com inurl:php?id=
```
Looks for SQL injection-prone URLs.  
```bash
site:example.com inurl:"search.php?q="
```
Finds search pages vulnerable to XSS.  
```bash
site:example.com "Apache/2.4.49" inurl:"server-status"
```
Checks for vulnerable Apache servers.  
```bash
site:example.com ext:action | ext:do "username"
```
Finds Java-based endpoints (Struts exploits).  
```bash
site:example.com filetype:xml inurl:"sitemap"
```
Detects sitemaps with exposed paths.  

### 📂 **Exposing Sensitive Information**  
```bash
site:example.com ext:json "password"
```
Finds JSON files with sensitive data.  
```bash
site:example.com ext:xml "phpinfo"
```
Searches for exposed PHP info pages.  
```bash
site:example.com ext:conf "nginx.conf" | "httpd.conf"
```
Finds web server configuration files.  
```bash
site:example.com "Error: SQL syntax near"
```
Detects SQL errors exposing database details.  
```bash
site:example.com "Warning: include("
```
Searches for local file inclusion (LFI) vulnerabilities.  

### 🛠 **Detecting Outdated Software & Exposed Services**  
```bash
site:example.com inurl:wp-content/plugins/
```
Finds outdated WordPress plugins.  
```bash
site:example.com "Server: Apache/2.2.3"
```
Detects old Apache versions.  
```bash
site:example.com "X-Powered-By: PHP/5.6"
```
Finds outdated PHP versions.  
```bash
site:example.com inurl:"/cgi-bin/"
```
Looks for vulnerable CGI scripts.  
```bash
site:example.com intitle:"Webmin"
```
Finds exposed Webmin panels.  

## ⚠️ Legal & Ethical Considerations

Using Google Dorks to access unauthorized data may violate laws and terms of service. Always ensure:  
✅ You have **explicit permission** to test a system.  
✅ You **do not access private data** without authorization.  
✅ You use this knowledge **responsibly** for cybersecurity research and education.  

## 🤝 Contributing

Want to contribute? Feel free to submit **pull requests** with new Google Dorks or enhancements!

## 📜 License

This repository is open-source under the **MIT License**.

## 📧 Contact

For discussions, suggestions, or collaboration opportunities, reach out at **[your email]** or connect via **[LinkedIn](your-linkedin-profile)**.

---

🚨 **Stay ethical, stay secure!** 🚨



