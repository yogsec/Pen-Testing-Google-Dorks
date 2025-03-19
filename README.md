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

### 🔍 **Finding Open Directories & Exposed Data**  
```bash
intitle:"index of /private" site:example.com
```
```bash
site:example.com intitle:"index of /" "backup"
```
```bash
site:example.com intitle:"index of /" "config"
```
```bash
site:example.com inurl:/admin/backup
```
```bash
site:example.com filetype:conf "mysql" | "nginx"
```

### 🔑 **Finding Leaked Credentials & Sensitive Files**  
```bash
site:example.com filetype:sql "INSERT INTO"
```
```bash
site:example.com filetype:xml "password"
```
```bash
site:example.com filetype:ini "username"
```
```bash
site:example.com filetype:log "error"
```
```bash
site:example.com filetype:cfg "password"
```

### 🔒 **Finding Login & Admin Panels**  
```bash
site:example.com inurl:"/cpanel"
```
```bash
site:example.com inurl:/admin/login
```
```bash
site:example.com inurl:/user/login
```
```bash
site:example.com intitle:"control panel"
```
```bash
site:example.com inurl:signin | inurl:auth
```

### 🔍 **Detecting Web Vulnerabilities**  
```bash
site:example.com inurl:.php?id=
```
```bash
site:example.com inurl:"product.php?item="
```
```bash
site:example.com inurl:"view.php?page="
```
```bash
site:example.com inurl:".env" "APP_KEY"
```
```bash
site:example.com "PHP Parse error" | "Fatal error"
```

### 📂 **Exposing Internal Data & Source Code**  
```bash
site:example.com filetype:json "password"
```
```bash
site:example.com filetype:yaml "secret"
```
```bash
site:example.com filetype:php "config"
```
```bash
site:example.com filetype:log "access.log"
```
```bash
site:example.com "Index of /git"
```

### 🛠 **Detecting Outdated Software & Misconfigurations**  
```bash
site:example.com inurl:/cgi-bin/
```
```bash
site:example.com "Apache/2.2.15"
```
```bash
site:example.com "X-Powered-By: ASP.NET"
```
```bash
site:example.com intitle:"phpMyAdmin"
```
```bash
site:example.com "Server at example.com Port 80"
```

### 🔍 **Finding Open Directories & Exposed Data**  
```bash
intitle:"index of /admin" site:example.com
```
```bash
intitle:"index of /backup" site:example.com
```
```bash
site:example.com intitle:"index of /" "database"
```
```bash
site:example.com filetype:cfg "passwd"
```
```bash
site:example.com "Index of /ftp"
```

### 🔑 **Finding Leaked Credentials & Sensitive Files**  
```bash
site:example.com filetype:json "private_key"
```
```bash
site:example.com filetype:csv "email,password"
```
```bash
site:example.com filetype:ini "db_password"
```
```bash
site:example.com "confidential" filetype:doc | filetype:pdf
```
```bash
site:example.com "restricted" filetype:xlsx | filetype:ppt
```

### 🔒 **Finding Login & Admin Panels**  
```bash
site:example.com inurl:"/dashboard/login"
```
```bash
site:example.com inurl:admin.cgi
```
```bash
site:example.com intitle:"staff login"
```
```bash
site:example.com "Welcome to phpMyAdmin"
```
```bash
site:example.com inurl:portal/login
```

### 🔍 **Detecting Web Vulnerabilities**  
```bash
site:example.com inurl:".git"
```
```bash
site:example.com inurl:"debug.log"
```
```bash
site:example.com inurl:"config.php~"
```
```bash
site:example.com inurl:"test.php"
```
```bash
site:example.com inurl:"old_site"
```

### 📂 **Exposing Internal Data & Source Code**  
```bash
site:example.com filetype:bak "config"
```
```bash
site:example.com filetype:log "credentials"
```
```bash
site:example.com filetype:php "dbconnect"
```
```bash
site:example.com "Index of /gitlab"
```
```bash
site:example.com intext:"API_SECRET"
```

### 🛠 **Detecting Outdated Software & Misconfigurations**  
```bash
site:example.com inurl:/phpinfo.php
```
```bash
site:example.com "Apache/2.2.15 (Unix)"
```
```bash
site:example.com "X-Powered-By: JSP"
```
```bash
site:example.com intitle:"cPanel Login"
```
```bash
site:example.com "Server at example.com Port 443"
```
