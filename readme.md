# 🔍 Comprehensive Google Dorks for Security Research

[![GitHub stars](https://img.shields.io/github/stars/yourusername/google-dorks?style=social)](https://github.com/kishwordulal1234/DorkBox)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A comprehensive collection of Google search queries (dorks) for cybersecurity research, penetration testing, and bug bounty hunting. This repository serves as a resource for security professionals, researchers, and ethical hackers.

## ⚠️ IMPORTANT LEGAL DISCLAIMER

**🚨 FOR EDUCATIONAL AND AUTHORIZED TESTING ONLY 🚨**

This repository is intended for:
- ✅ Educational purposes and security research
- ✅ Authorized penetration testing with written permission
- ✅ Bug bounty programs with proper scope
- ✅ Testing your own systems and applications
- ✅ Academic research in controlled environments

**NEVER USE THESE DORKS FOR:**
- ❌ Unauthorized access to systems
- ❌ Malicious activities or cyber attacks
- ❌ Violating terms of service
- ❌ Any illegal activities

By using this repository, you agree to use it responsibly and in accordance with all applicable laws and regulations.

---

## 📚 Table of Contents

- [SQL Injection Dorks](#-sql-injection-dorks)
- [XSS (Cross-Site Scripting) Dorks](#-xss-cross-site-scripting-dorks)
- [LFI/RFI (File Inclusion) Dorks](#-lfirfi-file-inclusion-dorks)
- [Command Injection Dorks](#-command-injection-dorks)
- [Directory Traversal Dorks](#-directory-traversal-dorks)
- [Configuration Files & Sensitive Data](#-configuration-files--sensitive-data)
- [Database Exposure Dorks](#-database-exposure-dorks)
- [Login Pages & Admin Panels](#-login-pages--admin-panels)
- [File Upload Vulnerabilities](#-file-upload-vulnerabilities)
- [IoT & Network Devices](#-iot--network-devices)
- [Web Cameras & Surveillance](#-web-cameras--surveillance)
- [API Endpoints](#-api-endpoints)
- [Version Disclosure](#-version-disclosure)
- [Backup Files](#-backup-files)
- [Log Files](#-log-files)
- [Development & Testing](#-development--testing)
- [E-commerce Vulnerabilities](#-e-commerce-vulnerabilities)
- [Educational Resources](#-educational-resources)

---

## 💉 SQL Injection Dorks

### 🟢 Easy Level SQL Injection Dorks
```
# Basic Error-Based SQL Injection
inurl:"id=" & intext:"mysql_fetch_array"
inurl:"id=" & intext:"mysql_num_rows"
inurl:"id=" & intext:"mysql_connect"
inurl:"id=" & intext:"You have an error in your SQL syntax"
inurl:"page=" & intext:"mysql_fetch_array"
inurl:"category=" & intext:"mysql_num_rows"
inurl:"login=" & intext:"Warning: mysql_"
"SQL syntax" "mysql_fetch_array"
```

### 🟡 Medium Level SQL Injection Dorks
```
# Multiple Database Types
"mysql_fetch_assoc" "expects parameter"
"mysql_fetch_row" "expects parameter"
"ORA-00933" "SQL command not properly ended"
"Microsoft OLE DB Provider" "error"
"ODBC Microsoft Access Driver"
"Invalid Querystring" "sql"
"Warning: pg_connect"
"PostgreSQL query failed"
"sqlite_query" "error"
"mssql_query" "error"
```

### 🔴 Advanced Level SQL Injection Dorks
```
# Complex Parameter Combinations
(inurl:"id=" OR inurl:"pid=" OR inurl:"uid=") & intext:"mysql"
(inurl:"category=" OR inurl:"cat=" OR inurl:"cid=") & intext:"sql"
site:*.edu (inurl:"id=" OR inurl:"page=") & intext:"database"
site:*.gov (inurl:"article=" OR inurl:"news=") & intext:"mysql"
filetype:php (inurl:"id=" OR inurl:"page=") & intext:"error"
```

### 🚀 Multi-Thread Level SQL Injection Dorks
```
# Bulk Discovery Patterns
((inurl:"id=" OR inurl:"pid=" OR inurl:"uid=" OR inurl:"cid=") AND (intext:"mysql" OR intext:"sql" OR intext:"database")) site:*.com
((inurl:"page=" OR inurl:"article=" OR inurl:"news=" OR inurl:"item=") AND (intext:"error" OR intext:"warning" OR intext:"fatal")) filetype:php
(site:*.edu OR site:*.org OR site:*.gov) AND ((inurl:"id=" OR inurl:"page=") AND (intext:"mysql" OR intext:"sql"))
```

### 🔥 Crazy Level SQL Injection Dorks
```
# Extreme Discovery Combinations
(((inurl:"id=" OR inurl:"pid=" OR inurl:"uid=" OR inurl:"cid=" OR inurl:"page=" OR inurl:"cat=") AND (intext:"mysql" OR intext:"sql" OR intext:"database" OR intext:"oracle" OR intext:"postgresql")) AND (site:*.com OR site:*.org OR site:*.net OR site:*.edu OR site:*.gov)) -site:github.com -site:stackoverflow.com
((filetype:php OR filetype:asp OR filetype:aspx OR filetype:jsp) AND ((inurl:"id=" OR inurl:"page=" OR inurl:"article=" OR inurl:"news=") AND (intext:"error" OR intext:"warning" OR intext:"exception" OR intext:"fatal")))
```

### 🗄️ All Database Types SQL Injection

#### MySQL Database Dorks
```
"mysql_fetch_array" "warning"
"mysql_num_rows" "warning"
"mysql_query" "error"
"mysql_connect" "failed"
"Table 'mysql" "doesn't exist"
"MySQL server version" "error"
```

#### PostgreSQL Database Dorks
```
"pg_query" "error"
"pg_connect" "failed"
"PostgreSQL" "ERROR"
"psql" "error"
"relation" "does not exist"
"pg_num_rows" "warning"
```

#### Oracle Database Dorks
```
"ORA-00933" "SQL command"
"ORA-01756" "quoted string"
"ORA-00936" "missing expression"
"Oracle" "OCI" "error"
"TNS" "could not resolve"
"PLS-" "error"
```

#### SQL Server (MSSQL) Database Dorks
```
"Microsoft OLE DB Provider" "error"
"ODBC SQL Server Driver"
"SQL Server" "error"
"mssql_query" "error"
"Unclosed quotation mark"
"Microsoft JET Database"
```

#### SQLite Database Dorks
```
"sqlite_query" "error"
"SQLite" "database is locked"
"sqlite3" "error"
"database disk image is malformed"
"SQLite format 3"
```

### ⏱️ Time-Based SQL Injection Dorks
```
# Time-Based Detection
"sleep" inurl:"id=" filetype:php
"benchmark" inurl:"id=" filetype:php
"waitfor delay" inurl:"id=" filetype:asp
"pg_sleep" inurl:"id=" filetype:php
"dbms_pipe.receive_message" inurl:"id="
site:*.edu inurl:"id=" "sleep"
site:*.com inurl:"page=" "waitfor"
```

### 🔍 Boolean-Based Blind SQL Injection
```
inurl:"id=" "true" "false" filetype:php
inurl:"page=" "1=1" "1=2" filetype:asp
"boolean" "blind" "sql" site:*.edu
inurl:"search=" "and" "or" filetype:php
```

### 📊 UNION-Based SQL Injection
```
"union select" inurl:"id=" filetype:php
"union all select" inurl:"page=" filetype:asp
"order by" inurl:"id=" filetype:php
"group by" inurl:"category=" filetype:php
```

### 💾 Stored SQL Injection
```
"insert into" "values" filetype:php
"update" "set" "where" filetype:asp
"delete from" "where" filetype:php
"stored procedure" "execute" filetype:asp
```

---

## 🔥 XSS (Cross-Site Scripting) Dorks

### 🟢 Easy Level XSS Dorks
```
# Basic Reflected XSS
inurl:"q=" site:*.edu
inurl:"search=" site:*.com
inurl:"query=" filetype:php
inurl:"keyword=" filetype:asp
inurl:"s=" site:*.org
"<script>" site:*.edu
"javascript:" site:*.gov
```

### 🟡 Medium Level XSS Dorks
```
# Multiple XSS Vectors
"<img src=" "onerror=" filetype:php
"<iframe" "onload=" filetype:asp
"<body" "onload=" filetype:php
"<svg" "onload=" filetype:html
"<input" "onfocus=" filetype:php
"alert(" site:*.com
"confirm(" site:*.org
"prompt(" site:*.edu
```

### 🔴 Advanced Level XSS Dorks
```
# Complex XSS Detection
(inurl:"search=" OR inurl:"q=" OR inurl:"query=") AND ("<script>" OR "javascript:" OR "onerror=")
(inurl:"name=" OR inurl:"title=" OR inurl:"message=") AND ("alert(" OR "confirm(" OR "prompt(")
site:*.edu (inurl:"comment=" OR inurl:"feedback=") AND ("<" OR ">" OR "javascript:")
```

### 🚀 Multi-Thread Level XSS Dorks
```
# Bulk XSS Discovery
((inurl:"search=" OR inurl:"q=" OR inurl:"query=" OR inurl:"keyword=") AND (filetype:php OR filetype:asp OR filetype:jsp)) -site:github.com
((inurl:"name=" OR inurl:"title=" OR inurl:"comment=" OR inurl:"message=") AND ("<script>" OR "javascript:" OR "onerror=" OR "onload="))
```

### 🔥 Crazy Level XSS Dorks
```
# Extreme XSS Discovery
(((inurl:"search=" OR inurl:"q=" OR inurl:"query=" OR inurl:"s=" OR inurl:"keyword=" OR inurl:"term=") AND (filetype:php OR filetype:asp OR filetype:jsp OR filetype:html)) AND (site:*.com OR site:*.org OR site:*.net OR site:*.edu)) -site:github.com -site:stackoverflow.com
```

### 🔍 Reflected XSS Dorks
```
# URL Parameter Reflection
inurl:"q=" "reflected" filetype:php
inurl:"search=" "parameter" filetype:asp
inurl:"query=" "echo" filetype:php
inurl:"input=" "print" filetype:php
"$_GET" "echo" filetype:php
"$_POST" "print" filetype:php
"Request.QueryString" filetype:asp
```

### 💾 Stored XSS Dorks
```
# Persistent XSS in Comments/Forms
"comment" "post" "stored" filetype:php
"guestbook" "persistent" filetype:php
"feedback" "form" "database" filetype:asp
"message board" "insert" filetype:php
"forum" "post" "save" filetype:php
intitle:"add comment" "database" filetype:php
"testimonial" "submit" filetype:php
```

### 🌐 DOM-Based XSS Dorks
```
# Client-Side XSS
"document.write" filetype:js
"innerHTML" filetype:js site:*.edu
"document.location" filetype:js
"window.location" filetype:js
"eval(" filetype:js site:*.com
"location.hash" filetype:js
"document.URL" filetype:js
"window.name" filetype:js
```

### ⏱️ Time-Based XSS Dorks
```
# Delayed XSS Execution
"setTimeout" "alert(" filetype:js
"setInterval" "javascript:" filetype:js
"delay" "xss" filetype:php
"async" "script" "load" filetype:html
```

### 🔄 Blind XSS Dorks
```
# Out-of-Band XSS
"email" "notification" "html" filetype:php
"report" "admin" "html" filetype:asp
"contact" "form" "email" filetype:php
"feedback" "admin" "notification" filetype:php
"log" "admin" "panel" filetype:php
```

## 🌐 HTML Injection Dorks

### 🟢 Easy Level HTML Injection Dorks
```
# Basic HTML Injection
inurl:"name=" "<h1>" filetype:php
inurl:"title=" "<b>" filetype:asp
inurl:"comment=" "<i>" filetype:php
inurl:"message=" "<u>" filetype:html
"<html>" inurl:"input=" filetype:php
"<body>" inurl:"text=" filetype:asp
```

### 🟡 Medium Level HTML Injection Dorks
```
# Advanced HTML Tags
inurl:"content=" "<div>" filetype:php
inurl:"description=" "<span>" filetype:asp
inurl:"text=" "<p>" filetype:php
"<table>" inurl:"data=" filetype:php
"<form>" inurl:"input=" filetype:html
"<iframe>" inurl:"url=" filetype:php
"<meta>" inurl:"content=" filetype:html
```

### 🔴 Advanced Level HTML Injection Dorks
```
# Complex HTML Injection
(inurl:"name=" OR inurl:"title=" OR inurl:"content=") AND ("<div>" OR "<span>" OR "<p>")
(inurl:"comment=" OR inurl:"message=" OR inurl:"text=") AND ("<html>" OR "<body>" OR "<head>")
```

### 🚀 Multi-Thread Level HTML Injection Dorks
```
# Bulk HTML Injection Discovery
((inurl:"name=" OR inurl:"title=" OR inurl:"content=" OR inurl:"text=") AND (filetype:php OR filetype:asp OR filetype:html)) "<"
```

### 🔥 Crazy Level HTML Injection Dorks
```
# Extreme HTML Injection Discovery
(((inurl:"name=" OR inurl:"title=" OR inurl:"content=" OR inurl:"text=" OR inurl:"comment=" OR inurl:"message=") AND ("<html>" OR "<body>" OR "<div>" OR "<span>" OR "<p>" OR "<h1>")) AND (site:*.com OR site:*.org OR site:*.net))
```

---

## 🚀 Remote Code Execution (RCE) Dorks

### 🟢 Easy Level RCE Dorks
```
# Basic RCE Patterns
inurl:"cmd=" filetype:php
inurl:"exec=" filetype:php
inurl:"system=" filetype:php
inurl:"shell=" filetype:php
inurl:"command=" filetype:php
"shell_exec" filetype:php
"passthru" filetype:php
```

### 🟡 Medium Level RCE Dorks
```
# Advanced RCE Functions
"exec(" filetype:php site:*.edu
"system(" filetype:php site:*.com
"shell_exec(" filetype:php
"passthru(" filetype:php
"popen(" filetype:php
"proc_open(" filetype:php
"eval(" "base64_decode" filetype:php
```

### 🔴 Advanced Level RCE Dorks
```
# Complex RCE Detection
(inurl:"cmd=" OR inurl:"exec=" OR inurl:"system=") AND (filetype:php OR filetype:asp OR filetype:jsp)
("shell_exec" OR "passthru" OR "system") AND ("$_GET" OR "$_POST") filetype:php
```

### 🚀 Multi-Thread Level RCE Dorks
```
# Bulk RCE Discovery
((inurl:"cmd=" OR inurl:"exec=" OR inurl:"system=" OR inurl:"shell=") AND (filetype:php OR filetype:asp OR filetype:jsp OR filetype:py)) -site:github.com
```

### 🔥 Crazy Level RCE Dorks
```
# Extreme RCE Discovery
(((inurl:"cmd=" OR inurl:"exec=" OR inurl:"system=" OR inurl:"shell=" OR inurl:"command=") AND ("shell_exec" OR "passthru" OR "system" OR "exec")) AND (filetype:php OR filetype:asp OR filetype:jsp)) -site:github.com -site:stackoverflow.com
```

### 💻 Command Execution Functions
```
# PHP RCE Functions
"shell_exec($_GET" filetype:php
"system($_POST" filetype:php
"exec($_REQUEST" filetype:php
"passthru($_COOKIE" filetype:php
"popen($_SESSION" filetype:php
"proc_open($_FILES" filetype:php
```

### 🌐 Web Shell Detection
```
# Web Shell Patterns
"web shell" filetype:php
"php shell" filetype:php
"cmd shell" filetype:asp
"shell script" filetype:jsp
"backdoor" filetype:php
"c99 shell" filetype:php
"r57 shell" filetype:php
```

---

## 🔍 Best Browsers for Google Dorking

### 🥇 1. Firefox (Recommended)
```
✅ Best Privacy Controls
✅ Advanced Search Extensions
✅ User-Agent Switching
✅ Cookie Management
✅ VPN Integration
✅ Developer Tools

Recommended Extensions:
- User-Agent Switcher
- Cookie Quick Manager
- Privacy Badger
- uBlock Origin
- FoxyProxy
```

### 🥈 2. Brave Browser
```
✅ Built-in Tor Integration
✅ Ad/Tracker Blocking
✅ Fingerprint Protection
✅ Privacy-First Design
✅ Chromium-Based Compatibility

Features:
- Built-in VPN (Premium)
- Private Windows with Tor
- Shield Settings
- Advanced Privacy Controls
```

### 🥉 3. Chrome (With Extensions)
```
⚠️ Requires Privacy Extensions
✅ Developer Tools
✅ Extension Ecosystem
✅ Sync Capabilities

Required Extensions:
- Privacy Badger
- uBlock Origin
- User-Agent Switcher
- VPN Extension
- Cookie Manager
```

### 4. Microsoft Edge
```
⚠️ Privacy Concerns
✅ InPrivate Mode
✅ Tracking Prevention
✅ Collections Feature

Limited Recommendations:
- Use InPrivate Mode
- Enable Strict Tracking Prevention
- Install Privacy Extensions
```

### 5. Bing Search Engine
```
🔍 Alternative Search Results
✅ Different Indexing
✅ Unique Dork Patterns
✅ Less Filtered Results

Bing-Specific Operators:
- ip: for IP-based searches
- contains: for file content
- filetype: works differently
- site: has variations
```

---

### Local File Inclusion
```
inurl:"page=" filetype:php
inurl:"file=" filetype:php
inurl:"path=" filetype:php
inurl:"include=" filetype:php
inurl:"inc=" filetype:php
inurl:"dir=" filetype:php
inurl:"template=" filetype:php
```

### Remote File Inclusion
```
"allow_url_include" filetype:php
"allow_url_fopen" filetype:php
inurl:"http://" inurl:"include"
inurl:"https://" inurl:"include"
filetype:php "include($_GET"
filetype:php "require($_GET"
```

### Common LFI/RFI Parameters
```
inurl:"index.php?page="
inurl:"main.php?page="
inurl:"home.php?page="
inurl:"view.php?page="
inurl:"content.php?page="
inurl:"display.php?page="
```

---

## ⚡ Command Injection Dorks

### OS Command Injection
```
inurl:"cmd=" filetype:php
inurl:"exec=" filetype:php
inurl:"system=" filetype:php
inurl:"shell=" filetype:php
inurl:"command=" filetype:php
"shell_exec" filetype:php
"passthru" filetype:php
```

### Network Commands
```
"ping" "traceroute" filetype:php
intitle:"network tools"
"network diagnostic" filetype:php
inurl:"ping.php"
inurl:"traceroute.php"
"whois" filetype:php
```

### System Information
```
"phpinfo()" filetype:php
"system info" filetype:php
"server status" filetype:php
inurl:"sysinfo" filetype:php
intitle:"system information"
```

---

## 🗂️ Directory Traversal Dorks

### Path Traversal Patterns
```
inurl:"../" filetype:php
inurl:"..\\" filetype:asp
"directory traversal" filetype:php
inurl:"path=" ".."
inurl:"dir=" ".."
filetype:php inurl:"include" ".."
```

### File Download Vulnerabilities
```
inurl:"download.php?file="
inurl:"get.php?file="
inurl:"read.php?file="
inurl:"fetch.php?file="
filetype:php "readfile"
```

---

## 🔐 Configuration Files & Sensitive Data

### Configuration Files
```
filetype:env "DB_PASSWORD"
filetype:config "password"
filetype:ini "password"
filetype:xml "password"
filetype:conf "password"
"config.php" filetype:txt
"database.yml" filetype:txt
"wp-config.php" filetype:txt
```

### Environment Files
```
".env" filetype:env
".env.local" filetype:txt
".env.production" filetype:txt
"environment.rb" filetype:txt
filetype:properties "password"
```

### API Keys and Secrets
```
"api_key" filetype:json
"secret_key" filetype:txt
"private_key" filetype:txt
"access_token" filetype:json
"auth_token" filetype:txt
"aws_access_key_id" filetype:txt
"sk-" "openai" filetype:txt
```

---

## 🗄️ Database Exposure Dorks

### Database Files
```
filetype:sql "INSERT INTO"
filetype:sql "CREATE TABLE"
filetype:sql "password"
filetype:mdb "password"
filetype:db "password"
"dump.sql" filetype:sql
"backup.sql" filetype:sql
```

### Database Admin Tools
```
intitle:"phpMyAdmin" "Welcome to phpMyAdmin"
intitle:"Adminer" "Login"
intitle:"phpPgAdmin"
"Database Administration" inurl:admin
"MySQL Admin" filetype:php
intitle:"SQL Web Data Administrator"
```

### Database Connection Strings
```
"connectionstring" filetype:txt
"Data Source=" filetype:txt
"Server=" "Database=" filetype:txt
"mysql_connect" filetype:php
"pg_connect" filetype:php
```

---

## 🔑 Login Pages & Admin Panels

### Admin Panels
```
intitle:"admin" "login"
intitle:"administrator" "login"
inurl:"admin" "login" filetype:php
inurl:"administrator" filetype:php
intitle:"control panel" "login"
"admin panel" "password"
intitle:"dashboard" "login"
```

### CMS Admin Areas
```
inurl:"wp-admin" "login"
inurl:"administrator" "joomla"
inurl:"admin" "drupal"
"typo3" "login"
"magento" "admin"
"prestashop" "admin"
```

### Default Credentials
```
"admin" "admin" "login"
"root" "root" "login"
"guest" "guest" "login"
intitle:"login" "default password"
"username" "password" "default"
```

---

## 📤 File Upload Vulnerabilities

### 🟢 Easy Level File Upload Dorks
```
# Basic Upload Endpoints
inurl:"upload.php"
inurl:"fileupload" filetype:php
inurl:"file_upload.php"
inurl:"upload_file.php"
"choose file" "upload"
intitle:"file upload"
"multipart/form-data" "upload"
```

### 🟡 Medium Level File Upload Dorks
```
# Advanced Upload Patterns
"file upload" "allowed types"
"upload" "extension" "filter"
"file upload" "validation"
"upload" "mime type" "check"
"image upload" "resize"
"document upload" "virus scan"
```

### 🔴 Advanced Level File Upload Dorks
```
# Complex Upload Discovery
(inurl:"upload" OR inurl:"file") AND ("php" OR "asp" OR "jsp") AND ("form" OR "post")
("file upload" OR "upload file") AND ("allowed" OR "permitted" OR "accepted") filetype:php
```

### 🚀 Multi-Thread Level File Upload Dorks
```
# Bulk Upload Discovery
((inurl:"upload" OR inurl:"file_upload" OR inurl:"fileupload") AND (filetype:php OR filetype:asp OR filetype:jsp)) -site:github.com
```

### 🔥 Crazy Level File Upload Dorks
```
# Extreme Upload Discovery
(((inurl:"upload" OR inurl:"file_upload" OR inurl:"fileupload" OR inurl:"file-upload") AND ("form" OR "post" OR "multipart")) AND (filetype:php OR filetype:asp OR filetype:jsp OR filetype:html)) -site:github.com -site:w3schools.com
```

### 📷 Image Upload Vulnerabilities
```
# Image-Specific Upload
"image upload" filetype:php
"photo upload" filetype:php
"avatar upload" filetype:php
inurl:"img_upload" filetype:php
"profile picture" "upload"
"gallery" "upload" "image"
"jpeg" "png" "gif" "upload" filetype:php
```

### 📄 Document Upload Vulnerabilities
```
# Document Upload Endpoints
"document upload" filetype:php
"file manager" "upload"
"resume upload" filetype:php
"CV upload" filetype:php
"attachment" "upload"
"pdf" "doc" "docx" "upload" filetype:php
"excel" "csv" "upload" filetype:php
```

### 🎵 Media Upload Vulnerabilities
```
# Audio/Video Upload
"media upload" filetype:php
"video upload" filetype:php
"audio upload" filetype:php
"mp3" "mp4" "upload" filetype:php
"streaming" "upload" filetype:php
```

### 🗜️ Archive Upload Vulnerabilities
```
# Compressed File Upload
"zip upload" filetype:php
"rar upload" filetype:php
"archive upload" filetype:php
"compressed" "file" "upload" filetype:php
"tar" "gz" "upload" filetype:php
```

### ⚠️ Unrestricted File Upload
```
# Dangerous Upload Patterns
"upload" "any file type" filetype:php
"upload" "no restriction" filetype:php
"file upload" "all formats" filetype:php
"upload" "exe" "allowed" filetype:php
"unrestricted" "file upload" filetype:php
```

### 🔍 File Upload with Path Disclosure
```
# Upload Path Information
"upload" "directory" "path" filetype:php
"file uploaded to" filetype:php
"upload successful" "location" filetype:php
"uploaded files" "folder" filetype:php
"upload path" "configuration" filetype:php
```

### 💾 File Upload with Database Storage
```
# Database-Integrated Upload
"upload" "database" "store" filetype:php
"file upload" "mysql" "insert" filetype:php
"upload" "blob" "database" filetype:php
"file" "upload" "sql" "table" filetype:php
```

### 🔐 File Upload Bypass Techniques Discovery
```
# Upload Filter Bypass Information
"upload" "bypass" "filter" filetype:php
"file upload" "double extension" filetype:php
"upload" "null byte" filetype:php
"mime type" "bypass" "upload" filetype:php
"upload" "content-type" "spoof" filetype:php
```

### 🖼️ File Upload with Preview/Display
```
# Upload with File Display
"upload" "preview" "display" filetype:php
"file upload" "thumbnail" filetype:php
"upload" "gallery" "view" filetype:php
"uploaded files" "list" "view" filetype:php
"file browser" "upload" filetype:php
```

### 📊 File Upload Statistics/Logs
```
# Upload Monitoring/Logging
"upload log" filetype:log
"file upload" "statistics" filetype:php
"upload" "monitor" "track" filetype:php
"uploaded files" "log" filetype:txt
"upload activity" "report" filetype:php
```

### 🔄 Bulk File Upload
```
# Multiple File Upload
"bulk upload" filetype:php
"multiple file upload" filetype:php
"batch upload" filetype:php
"mass upload" filetype:php
"drag and drop" "upload" filetype:php
```

### ☁️ Cloud File Upload Integration
```
# Cloud Storage Upload
"upload" "aws" "s3" filetype:php
"file upload" "google drive" filetype:php
"upload" "dropbox" "api" filetype:php
"cloud upload" "storage" filetype:php
"upload" "azure" "blob" filetype:php
```

### 🔧 File Upload Configuration Files
```
# Upload Configuration Exposure
"upload.conf" filetype:conf
"upload_config.php" filetype:txt
"file_upload.ini" filetype:ini
"upload_settings.xml" filetype:xml
"upload" "configuration" "file" filetype:json
```

---

## 🏠 IoT & Network Devices

### Router Interfaces
```
intitle:"router" "login"
"Router Configuration" "password"
intitle:"wireless" "setup"
"ADSL" "configuration"
intitle:"modem" "status"
"DD-WRT" "login"
"OpenWrt" "login"
```

### Network Printers
```
intitle:"printer" "configuration"
"Printer Status" inurl:printer
"HP LaserJet" "configuration"
"Canon" "printer" "status"
"Epson" "network" "printer"
```

### IoT Devices
```
"IoT" "device" "login"
intitle:"smart home" "control"
"thermostat" "login"
"security camera" "login"
"home automation" "admin"
```

---

## 📹 Web Cameras & Surveillance

### IP Cameras
```
intitle:"webcam" "live"
intitle:"camera" "view"
"mjpg" "video" "stream"
"axis camera" "view"
inurl:"ViewerFrame?Mode="
inurl:"MultiCameraFrame?Mode="
intitle:"Live View" "AXIS"
```

### Surveillance Systems
```
"surveillance" "camera" "login"
intitle:"security camera"
"CCTV" "viewer"
"IP Camera" "login"
"video surveillance" "web"
"DVR" "login"
```

### Streaming Servers
```
"streaming server" "admin"
"media server" "login"
"rtmp" "streaming"
"live stream" "control"
```

---

## 🔌 API Endpoints

### REST APIs
```
inurl:"api/v1"
inurl:"api/v2"
inurl:"/rest/"
inurl:"/graphql"
"api documentation" filetype:json
"swagger" "api"
"openapi" filetype:json
```

### API Keys in URLs
```
inurl:"api_key="
inurl:"apikey="
inurl:"access_token="
inurl:"auth_token="
"bearer" inurl:"api"
```

### API Endpoints
```
"/api/users"
"/api/admin"
"/api/auth"
"/api/login"
"/api/register"
"/api/config"
"/api/debug"
```

---

## 📊 Version Disclosure

### Server Information
```
"Server: Apache" filetype:txt
"Server: nginx" filetype:txt
"X-Powered-By: PHP" filetype:txt
"Server: Microsoft-IIS" filetype:txt
intitle:"Apache" "server status"
```

### Application Versions
```
"WordPress" "version" filetype:txt
"Joomla" "version" filetype:txt
"Drupal" "version" filetype:txt
"Laravel" "version" filetype:txt
"CodeIgniter" filetype:txt
```

### Framework Detection
```
"Powered by" "framework"
"Built with" "version"
"generator" "meta" "version"
"/assets/" "version" filetype:js
```

---

## 💾 Backup Files

### Backup File Extensions
```
filetype:bak "password"
filetype:backup "database"
filetype:old "config"
filetype:orig "password"
filetype:tmp "password"
site:*.edu filetype:bak
```

### Database Backups
```
"backup.sql" filetype:sql
"dump.sql" filetype:sql
"database.sql" filetype:sql
"db_backup" filetype:sql
filetype:sql "mysqldump"
```

### Archive Files
```
filetype:zip "backup"
filetype:rar "backup"
filetype:tar "backup"
filetype:7z "backup"
"backup" filetype:gz
```

---

## 📝 Log Files

### Server Logs
```
filetype:log "error"
filetype:log "access"
"error.log" filetype:log
"access.log" filetype:log
"server.log" filetype:log
filetype:log "exception"
```

### Application Logs
```
"debug.log" filetype:log
"app.log" filetype:log
"application.log" filetype:log
"laravel.log" filetype:log
"rails.log" filetype:log
```

### Security Logs
```
"security.log" filetype:log
"auth.log" filetype:log
"firewall.log" filetype:log
"intrusion" filetype:log
```

---

## 🧪 Development & Testing

### Development Environments
```
"development" "environment"
"staging" "server"
"test" "server"
inurl:"dev" filetype:php
inurl:"beta" filetype:php
"localhost" filetype:php
```

### Debug Information
```
"debug" "true" filetype:php
"debug mode" "on"
"error_reporting" "E_ALL"
"display_errors" "On"
"var_dump" filetype:php
```

### Git Repositories
```
".git" "directory"
".git/config" filetype:txt
"git" "repository" "clone"
inurl:"/.git/"
filetype:git
```

---

## 🛒 E-commerce Vulnerabilities

### Shopping Carts
```
"shopping cart" "admin"
"e-commerce" "admin"
"online store" "admin"
"magento" "admin"
"woocommerce" "admin"
"shopify" "admin"
```

### Payment Processing
```
"payment" "gateway" "test"
"credit card" "processing"
"paypal" "integration"
"stripe" "api"
"payment" "debug"
```

### Order Systems
```
"order" "management" "admin"
"inventory" "system" "admin"
"product" "catalog" "admin"
```

---

## 🎓 Educational Resources

### Deliberately Vulnerable Applications
```
site:testphp.vulnweb.com
site:demo.testfire.net
"damn vulnerable web application"
"webgoat" "deliberately vulnerable"
"mutillidae" "vulnerable"
"bwapp" "buggy web application"
```

### Security Training Sites
```
site:*.edu "penetration testing"
site:*.edu "ethical hacking"
"cybersecurity" "lab" site:*.edu
"vulnerability" "assessment" site:*.edu
```

---

## 🛠️ Advanced Search Techniques

### Combining Operators
```
# Multiple conditions
(inurl:"admin" OR inurl:"login") AND filetype:php

# Excluding results
"sql injection" -site:github.com -site:stackoverflow.com

# Wildcard searches
"password" filetype:* site:*.edu

# Date ranges
after:2020 "data breach"
before:2022 "vulnerability disclosure"
```

### Site-Specific Searches
```
# Educational institutions
site:*.edu "vulnerable"

# Government sites
site:*.gov "security"

# Specific domains
site:example.com "admin"

# IP ranges (use Shodan for this)
net:"192.168.1.0/24"
```

### File Type Combinations
```
(filetype:php OR filetype:asp OR filetype:jsp) "admin"
(filetype:txt OR filetype:log OR filetype:conf) "password"
(filetype:sql OR filetype:db OR filetype:mdb) "users"
```

---

## 📖 Usage Guidelines

### Best Practices
1. **Always get permission** before testing any system
2. **Use VPN** for anonymity during research
3. **Document findings** properly for reports
4. **Rate limit** your searches to avoid detection
5. **Verify results** manually before reporting

### Search Tips
1. Use quotes for exact phrase matching
2. Combine multiple operators for precise results
3. Use exclusion (-) to filter out noise
4. Try variations of keywords
5. Use different search engines (Google, Bing, DuckDuckGo)

### Tools Integration
- **Burp Suite**: Import found URLs for testing
- **OWASP ZAP**: Automated scanning of discovered endpoints
- **Nmap**: Port scanning of discovered systems
- **SQLmap**: Automated SQL injection testing
- **XSStrike**: XSS vulnerability testing

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### How to Contribute
1. Fork the repository
2. Create a feature branch
3. Add new dorks with proper categorization
4. Test the dorks for accuracy
5. Submit a pull request

### Contribution Categories
- New vulnerability types
- Better search patterns
- Regional/language-specific dorks
- Tool integration examples
- Educational resources

---

## 📚 References & Resources

### Learning Resources
- [OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [HackerOne Hacktivity](https://hackerone.com/hacktivity)
- [SANS Penetration Testing](https://www.sans.org/cyber-security-courses/penetration-testing-ethical-hacking/)

### Tools
- [Google Hacking Database](https://www.exploit-db.com/google-hacking-database)
- [Shodan](https://www.shodan.io/)
- [Censys](https://censys.io/)
- [PublicWWW](https://publicwww.com/)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚖️ Legal Notice

This repository is for educational purposes only. The authors and contributors are not responsible for any misuse of the information provided. Always ensure you have proper authorization before testing any systems.

**Remember: With great power comes great responsibility. Use these tools ethically and legally.**

---

⭐ **If this repository helped you in your security research, please consider giving it a star!**

**Happy Ethical Hacking! 🔒**
