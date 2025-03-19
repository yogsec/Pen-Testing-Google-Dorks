# Pen Testing Google Dorks

![Pen Testing Google Dorks](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExYnA4MWR3dTByMDBxaWh1d2Y3cW4zZ29ycndybDJucHlhNW14ZHRxYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/hwbWdAuTjDIIg/giphy.gif)

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

### 🔍 **Finding Exposed Files & Directories**  
```bash
intitle:"index of /private" site:example.com
```
```bash
site:example.com inurl:"/uploads" -intext:"no such"
```
```bash
site:example.com inurl:"backup.zip" | inurl:"database.sql"
```
```bash
site:example.com inurl:".ssh" | inurl:"id_rsa"
```
```bash
site:example.com "Index of" "parent directory" "config"
```

### 🔑 **Finding Sensitive Credentials**  
```bash
site:example.com filetype:json "aws_secret_access_key"
```
```bash
site:example.com filetype:log "admin password"
```
```bash
site:example.com filetype:ini "smtp_password"
```
```bash
site:example.com filetype:conf "vpn_password"
```
```bash
site:example.com "Authorization: Bearer"
```

### 🔒 **Finding Login Pages & Admin Panels**  
```bash
site:example.com inurl:"/admin/login.jsp"
```
```bash
site:example.com inurl:"/login.php?redirect="
```
```bash
site:example.com inurl:"/controlpanel"
```
```bash
site:example.com intitle:"webmail login"
```
```bash
site:example.com "Please enter your username and password"
```

### 🔍 **Detecting Web Vulnerabilities**  
```bash
site:example.com inurl:".git/config"
```
```bash
site:example.com inurl:".svn/entries"
```
```bash
site:example.com inurl:"?debug=true"
```
```bash
site:example.com inurl:"/phpinfo.php"
```
```bash
site:example.com inurl:"/server-status"
```

### 📂 **Exposing Sensitive Information**  
```bash
site:example.com inurl:"/logs/error.log"
```
```bash
site:example.com filetype:db "sqlite"
```
```bash
site:example.com filetype:cfg "site.cfg"
```
```bash
site:example.com "Usernames and passwords"
```
```bash
site:example.com intext:"confidential - do not distribute"
```

### 🛠 **Detecting Outdated Software & Exposed Services**  
```bash
site:example.com "Apache/2.2.22" -apache.org
```
```bash
site:example.com inurl:"/cgi-bin/test.cgi"
```
```bash
site:example.com "X-Powered-By: ASP.NET 2.0"
```
```bash
site:example.com inurl:"/phpmyadmin/setup.php"
```
```bash
site:example.com "Server: Microsoft-IIS/6.0"
```

### 🔍 **Finding Exposed Files & Directories**  
```bash
site:example.com inurl:/uploads intitle:index.of
```
Lists exposed upload directories.  
```bash
site:example.com inurl:/private | inurl:/confidential
```
Finds directories labeled as private or confidential.  
```bash
site:example.com ext:swp | ext:bak | ext:old
```
Searches for temporary or backup files.  
```bash
site:example.com inurl:temp | inurl:cache | inurl:old
```
Finds temporary, cache, and old directories.  
```bash
site:example.com "Index of /" "userdata"
```
Locates user data directories.  

### 🔑 **Finding Sensitive Credentials**  
```bash
site:example.com ext:ini "mysql_password"
```
Finds `.ini` files containing MySQL credentials.  
```bash
site:example.com "BEGIN RSA PRIVATE KEY"
```
Searches for leaked private SSH keys.  
```bash
site:example.com "Authorization: Basic"
```
Detects HTTP Basic Authentication headers.  
```bash
site:example.com filetype:cfg "admin_password"
```
Finds configuration files with admin credentials.  
```bash
site:example.com "ftp://" intext:"@"
```
Locates plaintext FTP credentials.  

### 🔒 **Finding Login Pages & Admin Panels**  
```bash
site:example.com intitle:"Sign In" | intitle:"Login"
```
Lists general login portals.  
```bash
site:example.com inurl:/auth | inurl:/secure
```
Finds authentication pages.  
```bash
site:example.com inurl:/portal/login
```
Searches for employee or customer portals.  
```bash
site:example.com inurl:"/admin/" filetype:php
```
Locates PHP-based admin panels.  
```bash
site:example.com intitle:"Customer Login"
```
Detects exposed customer login pages.  

### 🔍 **Detecting Web Vulnerabilities**  
```bash
site:example.com "Fatal error" "on line"
```
Finds error messages revealing source code details.  
```bash
site:example.com inurl:/debug mode
```
Searches for debug pages left enabled.  
```bash
site:example.com inurl:/staging | inurl:/test
```
Finds test and staging environments.  
```bash
site:example.com inurl:/api/docs
```
Checks for exposed API documentation.  
```bash
site:example.com inurl:"/forgot-password" | "reset your password"
```
Finds password reset forms that might be abused.  

### 📂 **Exposing Sensitive Information**  
```bash
site:example.com filetype:log "error.log"
```
Finds log files with possible sensitive data.  
```bash
site:example.com ext:conf "smtp.gmail.com"
```
Finds SMTP configuration files.  
```bash
site:example.com filetype:csv "email,password"
```
Detects exposed CSV files with login credentials.  
```bash
site:example.com filetype:xlsx "username password"
```
Finds Excel spreadsheets with user credentials.  
```bash
site:example.com intext:"confidential" | intext:"classified"
```
Searches for confidential documents.  

### 🛠 **Detecting Outdated Software & Exposed Services**  
```bash
site:example.com inurl:/wp-content/plugins/ intitle:"index of"
```
Finds outdated WordPress plugins.  
```bash
site:example.com "X-Powered-By: PHP/5.3"
```
Detects sites running old PHP versions.  
```bash
site:example.com inurl:/cgi-bin/ intitle:index.of
```
Finds CGI scripts that may be vulnerable.  
```bash
site:example.com "Server: nginx/1.12"
```
Searches for outdated Nginx versions.  
```bash
site:example.com intitle:"OpenVPN Admin"
```
Detects exposed OpenVPN administration panels.  

