# 🔍 DorkBox - The Ultimate Google Dorks Toolkit

[![GitHub stars](https://img.shields.io/github/stars/kishwordulal1234/dorkbox?style=social)](https://github.com/kishwordulal1234/DorkBox?tab=readme-ov-file)
[![License](https://img.shields.io/badge/license-CC%20BY--NC--ND%204.0-blue.svg)](LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A comprehensive collection of **working** Google search queries (dorks) for cybersecurity research, penetration testing, and bug bounty hunting. All dorks are tested and proven effective for finding real vulnerabilities.

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

- [🔍 Best Browsers for Dorking](#-best-browsers-for-dorking)
- [💉 SQL Injection Dorks](#-sql-injection-dorks)
- [🔥 XSS (Cross-Site Scripting) Dorks](#-xss-cross-site-scripting-dorks)
- [🌐 HTML Injection Dorks](#-html-injection-dorks)
- [🚀 Remote Code Execution (RCE) Dorks](#-remote-code-execution-rce-dorks)
- [📁 LFI/RFI (File Inclusion) Dorks](#-lfirfi-file-inclusion-dorks)
- [📤 File Upload Vulnerabilities](#-file-upload-vulnerabilities)
- [🔐 Configuration Files & Sensitive Data](#-configuration-files--sensitive-data)
- [🗄️ Database Exposure Dorks](#-database-exposure-dorks)
- [🔑 Login Pages & Admin Panels](#-login-pages--admin-panels)
- [🏠 IoT & Network Devices](#-iot--network-devices)
- [📹 Web Cameras & Surveillance](#-web-cameras--surveillance)
- [🔌 API Endpoints](#-api-endpoints)
- [💾 Backup Files](#-backup-files)
- [📝 Log Files](#-log-files)
- [🧪 Development & Testing](#-development--testing)
- [🛒 E-commerce Vulnerabilities](#-e-commerce-vulnerabilities)
- [🎓 Educational Resources](#-educational-resources)

---

## 🔍 Best Browsers for Google Dorking

### 🥇 1. Firefox (Most Recommended)
```
✅ Superior Privacy Controls
✅ Advanced Search Extensions Support
✅ User-Agent Switching Capabilities
✅ Excellent Cookie Management
✅ VPN Integration Support
✅ Comprehensive Developer Tools
✅ No Search Result Filtering

Recommended Extensions:
- User-Agent Switcher and Manager
- Cookie Quick Manager
- Privacy Badger
- uBlock Origin
- FoxyProxy Standard
- ClearURLs
```

### 🥈 2. Brave Browser
```
✅ Built-in Tor Integration
✅ Native Ad/Tracker Blocking
✅ Fingerprint Protection
✅ Privacy-First Design Philosophy
✅ Chromium-Based Compatibility
✅ No Search Censorship

Key Features:
- Built-in VPN (Premium)
- Private Windows with Tor
- Aggressive Shield Settings
- Advanced Privacy Controls
- Search Result Transparency
```

### 🥉 3. Chrome (With Privacy Extensions)
```
⚠️ Requires Heavy Privacy Configuration
✅ Excellent Developer Tools
✅ Large Extension Ecosystem
✅ Sync Capabilities
❌ Google Tracking Concerns

Essential Extensions:
- Privacy Badger
- uBlock Origin
- User-Agent Switcher
- Decentraleyes
- ClearURLs
- VPN Extension
```

### 4. Microsoft Edge
```
⚠️ Privacy Concerns Present
✅ InPrivate Mode Available
✅ Basic Tracking Prevention
✅ Collections Feature
❌ Limited Dorking Effectiveness

Configuration Tips:
- Always Use InPrivate Mode
- Enable Strict Tracking Prevention
- Install Privacy Extensions
- Disable Bing Integration
```
### developer recomendation 
use firefox an use this with every dork 
```
-site:bugs.mysql.com -site:bug.php -site:bugs -site:sphinxsearch.com -site:webassist.com -site:ghithu.com -site:stackoverflow.com -site:routicket.com -site:mydbr.com -site:mysqlforum.com -site:forums.mysql.com
i use the most


site:*.com inurl:php?id= (intext:"You have an error in your SQL syntax" | intext:"mysql_fetch" | intext:"Warning: mysql") -site:bugs.mysql.com -site:bug.php -site:bugs -site:sphinxsearch.com -site:webassist.com -site:ghithu.com -site:stackoverflow.com -site:routicket.com -site:mydbr.com -site:mysqlforum.com -site:forums.mysql.com


site:*.com inurl:"php?id=" (intext:"SQL syntax" | intext:"mysql_fetch" | intext:"Warning MYSQL:")
-site:bugs.mysql.com -site:bug.php -site:bugs ...


site:*.com inurl:"php?id=" (intext:"SQL syntax" | intext:"mysql_fetch" | intext:"Warning MYSQL:") -site:bugs.mysql.com -site:bug.php -site:bugs -site:sphinxsearch.com -site:webassist.com -site:ghithu.com -site:stackoverflow.com -site:routicket.com -site:mydbr.com


inurl:".php?id=" "You have an error in your SQL syntax"

```

### 5. Alternative Search Engines
```
🔍 Bing - Different Indexing, Less Filtering
🔍 DuckDuckGo - Privacy-Focused, Limited Results
🔍 Yandex - Different Regional Focus
🔍 Baidu - Chinese Content Focus
🔍 Searx - Open Source, Aggregated Results

Bing-Specific Operators:
- ip:192.168.1.1 (IP-based searches)
- contains:password (file content search)
- filetype: (works differently than Google)
- site: (has regional variations)
```

---

## 💉 SQL Injection Dorks

### 🟢 Easy Level SQL Injection Dorks (Beginner)
```
# Basic PHP MySQL Errors
intext:"Warning: mysql_fetch_assoc()" inurl:".php?id="
intext:"Warning: mysql_num_rows()" inurl:".php?id="
intext:"SQL syntax error" inurl:"php?id="
intext:"mysql_fetch_array()" inurl:"id="
inurl:".php?id=" "You have an error in your SQL syntax"

# Simple Parameter Testing
inurl:"news.php?id="
inurl:"article.php?id="
inurl:"product.php?id="
inurl:"page.php?id="
inurl:"item.php?id="
```

### 🟡 Medium Level SQL Injection Dorks (Intermediate)
```
# Multiple Database Error Types
intext:"SQLSTATE[42000]" inurl:"php?id="
intext:"Warning: pg_query()" inurl:".php?id="
intext:"Microsoft OLE DB Provider" inurl:"asp?id="
intext:"ORA-00933: SQL command not properly ended"
intext:"sqlite3.OperationalError:" inurl:"py?"

# Regional Targeting with Errors
site:*.edu intext:"SQL syntax error" | intext:"mysql_fetch_assoc"
site:*.gov intext:"Warning: mysql" inurl:"php?id="
site:*.org intext:"SQLSTATE" | intext:"PDOException"
```

### 🔴 Advanced Level SQL Injection Dorks (Expert)
```
# Complex Parameter Combinations
inurl:(details.php | view.php | item.php | search.php) inurl:id= intext:"mysql"
site:*.com inurl:"php?id=" (intext:"SQL syntax" | intext:"mysql_fetch" | intext:"Warning:")
(inurl:"category=" | inurl:"cat=" | inurl:"cid=") intext:"database error"

# Advanced Database-Specific Errors
site:*.edu intext:"Microsoft OLE DB Provider for SQL Server" intext:"80040e14"
site:*.gov intext:"PostgreSQL query failed" inurl:"php?"
site:*.org intext:"Oracle error" | intext:"ORA-" inurl:"jsp?"
```

### 🚀 Multi-Thread Level SQL Injection Dorks (Mass Discovery)
```
# Bulk Discovery Patterns
((inurl:"id=" | inurl:"pid=" | inurl:"uid=" | inurl:"cid=") & (intext:"mysql" | intext:"sql" | intext:"database")) site:*.com
((inurl:"page=" | inurl:"article=" | inurl:"news=" | inurl:"item=") & (intext:"error" | intext:"warning" | intext:"fatal")) filetype:php
(site:*.edu | site:*.org | site:*.gov) & ((inurl:"id=" | inurl:"page=") & (intext:"mysql" | intext:"sql"))
```

### 🔥 Crazy Level SQL Injection Dorks (Extreme Discovery)
```
# Maximum Coverage Combinations
(((inurl:"id=" | inurl:"pid=" | inurl:"uid=" | inurl:"cid=" | inurl:"page=" | inurl:"cat=") & (intext:"mysql" | intext:"sql" | intext:"database" | intext:"oracle" | intext:"postgresql")) & (site:*.com | site:*.org | site:*.net | site:*.edu | site:*.gov)) -site:github.com -site:stackoverflow.com

# Country-Specific Mass Discovery
((site:*.np | site:*.in | site:*.pk | site:*.bd | site:*.lk) & (inurl:"php?id=" | inurl:"asp?id=") & (intext:"SQL" | intext:"mysql" | intext:"database"))
```

### 🗄️ Database-Specific SQL Injection Dorks

#### MySQL Database Errors
```
intext:"Warning: mysql_fetch_assoc()" inurl:"php?id="
intext:"mysql_num_rows(): supplied argument" inurl:".php?id="
intext:"Table 'mysql.user' doesn't exist" inurl:"php?"
intext:"MySQL server version for the right syntax" inurl:"id="
site:*.np intext:"Warning: mysql" | intext:"mysql_fetch"
```

#### PostgreSQL Database Errors  
```
intext:"Warning: pg_query()" inurl:"php?"
intext:"PostgreSQL query failed: ERROR:" 
intext:"pg_connect(): Unable to connect" inurl:"php?"
intext:"relation does not exist" inurl:"php?id="
site:*.in intext:"pg_query" | intext:"PostgreSQL"
```

#### Oracle Database Errors
```
intext:"ORA-00933: SQL command not properly ended"
intext:"ORA-01756: quoted string not properly terminated"
intext:"ORA-00936: missing expression" inurl:"jsp?"
intext:"TNS: could not resolve service name"
site:*.gov intext:"ORA-" | intext:"Oracle error"
```

#### SQL Server (MSSQL) Errors
```
intext:"Microsoft OLE DB Provider for SQL Server" intext:"80040e14"
intext:"ODBC SQL Server Driver" inurl:"asp?"
intext:"Unclosed quotation mark before the character string"
intext:"Microsoft JET Database Engine error" inurl:"asp?id="
site:*.com intext:"Microsoft OLE DB" | intext:"SQL Server"
```

#### SQLite Database Errors
```
intext:"sqlite3.OperationalError:" inurl:"py?"
intext:"SQLite error: database is locked"
intext:"database disk image is malformed"
intext:"SQLite format 3" filetype:db
site:*.org intext:"sqlite" | intext:"SQLite error"
```

### ⏱️ Time-Based SQL Injection Discovery
```
# Time Delay Function Detection
inurl:"php?id=" intext:"sleep(" 
inurl:"asp?id=" intext:"waitfor delay"
inurl:"php?" intext:"benchmark("
inurl:"jsp?" intext:"dbms_pipe.receive_message"
site:*.edu inurl:"id=" intext:"sleep" | intext:"delay"
```

### 🔍 Boolean-Based Blind SQL Injection
```
inurl:"php?id=" intext:"true" intext:"false"
inurl:"id=" (intext:"1=1" | intext:"1=2") filetype:php
inurl:"search.php?" intext:"and" intext:"or"
site:*.com inurl:"category=" (intext:"true" | intext:"false")
```

### 📊 UNION-Based SQL Injection Discovery
```
inurl:"php?id=" intext:"union select"
inurl:"id=" intext:"union all select" filetype:php
inurl:"page=" intext:"order by" filetype:asp
inurl:"item=" intext:"group by" intext:"having"
```

### 💾 Stored/Insert SQL Injection
```
inurl:"register.php" intext:"insert into"
inurl:"contact.php" intext:"insert" intext:"values"
inurl:"feedback.php" intext:"update" intext:"set"
inurl:"comment.php" intext:"insert" | intext:"update"
```

---

## 🔥 XSS (Cross-Site Scripting) Dorks

### 🟢 Easy Level XSS Dorks (Beginner)
```
# Basic Reflected XSS Parameters
inurl:"search=" site:*.edu
inurl:"q=" site:*.com  
inurl:"query=" filetype:php
inurl:"keyword=" filetype:asp
inurl:"s=" filetype:php
inurl:"term=" site:*.org
```

### 🟡 Medium Level XSS Dorks (Intermediate)
```
# XSS with HTML Tags Present
inurl:"search=" intext:"<script>" filetype:php
inurl:"q=" intext:"javascript:" site:*.com
inurl:"name=" intext:"<img" filetype:php
inurl:"title=" intext:"onerror=" filetype:asp
inurl:"comment=" intext:"onload=" filetype:php
```

### 🔴 Advanced Level XSS Dorks (Expert)
```
# Complex XSS Detection Patterns
(inurl:"search=" | inurl:"q=" | inurl:"query=") & (intext:"<script>" | intext:"javascript:" | intext:"onerror=")
(inurl:"name=" | inurl:"title=" | inurl:"message=") & (intext:"alert(" | intext:"confirm(" | intext:"prompt(")
site:*.edu (inurl:"comment=" | inurl:"feedback=") & (intext:"<" | intext:">" | intext:"javascript:")
```

### 🚀 Multi-Thread Level XSS Dorks (Mass Discovery)
```
# Bulk XSS Parameter Discovery
((inurl:"search=" | inurl:"q=" | inurl:"query=" | inurl:"keyword=") & (filetype:php | filetype:asp | filetype:jsp)) -site:github.com -site:w3schools.com
((inurl:"name=" | inurl:"title=" | inurl:"comment=" | inurl:"message=") & (site:*.edu | site:*.org | site:*.gov))
```

### 🔥 Crazy Level XSS Dorks (Extreme Discovery)
```
# Maximum XSS Coverage
(((inurl:"search=" | inurl:"q=" | inurl:"query=" | inurl:"s=" | inurl:"keyword=" | inurl:"term=") & (filetype:php | filetype:asp | filetype:jsp | filetype:html)) & (site:*.com | site:*.org | site:*.net | site:*.edu)) -site:github.com -site:stackoverflow.com -site:w3schools.com
```

### 🔍 Reflected XSS Dorks
```
# Parameter Reflection Testing
inurl:"search.php?q=" 
inurl:"index.php?search="
inurl:"results.php?query="
inurl:"find.php?keyword="
site:*.np inurl:"search=" | inurl:"q="
site:*.in inurl:"query=" | inurl:"find="
```

### 💾 Stored XSS Dorks  
```
# Persistent XSS in Forms
inurl:"comment.php" "post comment"
inurl:"guestbook.php" "add entry" 
inurl:"feedback.php" "submit feedback"
inurl:"contact.php" "send message"
inurl:"forum.php" "new post"
site:*.edu inurl:"comment" | inurl:"feedback"
```

### 🌐 DOM-Based XSS Dorks
```
# Client-Side XSS Detection
filetype:js intext:"document.write("
filetype:js intext:"innerHTML =" 
filetype:js intext:"document.location"
filetype:js intext:"window.location"
filetype:js intext:"eval(" 
site:*.com filetype:js intext:"location.hash"
```

### ⏱️ Time-Based XSS Dorks
```
# Delayed XSS Execution
filetype:js intext:"setTimeout" intext:"alert("
filetype:js intext:"setInterval" intext:"javascript:"
inurl:"js?" intext:"delay" intext:"script"
filetype:html intext:"async" intext:"script"
```

### 🔄 Blind XSS Dorks
```
# Out-of-Band XSS Discovery
inurl:"contact.php" intext:"email" intext:"admin"
inurl:"report.php" intext:"admin" intext:"notification"  
inurl:"feedback.php" intext:"email" intext:"send"
inurl:"support.php" intext:"ticket" intext:"admin"
```

---

## 🌐 HTML Injection Dorks

### 🟢 Easy Level HTML Injection Dorks (Beginner)
```
# Basic HTML Tag Injection
inurl:"name=" filetype:php
inurl:"title=" filetype:asp
inurl:"comment=" filetype:php  
inurl:"message=" filetype:html
inurl:"description=" filetype:php
```

### 🟡 Medium Level HTML Injection Dorks (Intermediate)
```
# HTML Tags in Parameters
inurl:"content=" intext:"<div>" filetype:php
inurl:"text=" intext:"<span>" filetype:asp
inurl:"data=" intext:"<p>" filetype:php
inurl:"html=" intext:"<table>" filetype:php
```

### 🔴 Advanced Level HTML Injection Dorks (Expert)
```
# Complex HTML Injection Detection
(inurl:"name=" | inurl:"title=" | inurl:"content=") & (intext:"<div>" | intext:"<span>" | intext:"<p>")
(inurl:"comment=" | inurl:"message=" | inurl:"text=") & (intext:"<html>" | intext:"<body>" | intext:"<head>")
```

### 🚀 Multi-Thread Level HTML Injection Dorks (Mass Discovery)
```
# Bulk HTML Injection Discovery
((inurl:"name=" | inurl:"title=" | inurl:"content=" | inurl:"text=") & (filetype:php | filetype:asp | filetype:html)) -site:github.com
```

### 🔥 Crazy Level HTML Injection Dorks (Extreme Discovery)
```
# Maximum HTML Injection Coverage
(((inurl:"name=" | inurl:"title=" | inurl:"content=" | inurl:"text=" | inurl:"comment=" | inurl:"message=") & (intext:"<html>" | intext:"<body>" | intext:"<div>" | intext:"<span>" | intext:"<p>" | intext:"<h1>")) & (site:*.com | site:*.org | site:*.net))
```

---

## 🚀 Remote Code Execution (RCE) Dorks

### 🟢 Easy Level RCE Dorks (Beginner)
```
# Basic Command Execution
inurl:"cmd=" filetype:php
inurl:"exec=" filetype:php
inurl:"system=" filetype:php
inurl:"shell=" filetype:php  
inurl:"command=" filetype:php
```

### 🟡 Medium Level RCE Dorks (Intermediate)
```
# PHP Execution Functions
intext:"shell_exec(" filetype:php
intext:"system(" filetype:php site:*.edu
intext:"exec(" filetype:php
intext:"passthru(" filetype:php
intext:"popen(" filetype:php
```

### 🔴 Advanced Level RCE Dorks (Expert)
```
# Complex RCE Detection
(inurl:"cmd=" | inurl:"exec=" | inurl:"system=") & (filetype:php | filetype:asp | filetype:jsp)
(intext:"shell_exec" | intext:"passthru" | intext:"system") & (intext:"$_GET" | intext:"$_POST") filetype:php
```

### 🚀 Multi-Thread Level RCE Dorks (Mass Discovery)
```
# Bulk RCE Discovery
((inurl:"cmd=" | inurl:"exec=" | inurl:"system=" | inurl:"shell=") & (filetype:php | filetype:asp | filetype:jsp | filetype:py)) -site:github.com -site:stackoverflow.com
```

### 🔥 Crazy Level RCE Dorks (Extreme Discovery)
```
# Maximum RCE Coverage
(((inurl:"cmd=" | inurl:"exec=" | inurl:"system=" | inurl:"shell=" | inurl:"command=") & (intext:"shell_exec" | intext:"passthru" | intext:"system" | intext:"exec")) & (filetype:php | filetype:asp | filetype:jsp)) -site:github.com -site:stackoverflow.com
```

### 💻 Command Execution Function Detection
```
# Dangerous PHP Functions
intext:"shell_exec($_GET" filetype:php
intext:"system($_POST" filetype:php  
intext:"exec($_REQUEST" filetype:php
intext:"passthru($_COOKIE" filetype:php
intext:"eval(" intext:"base64_decode" filetype:php
```

### 🌐 Web Shell Detection
```
# Web Shell Patterns
intext:"web shell" filetype:php
intext:"php shell" filetype:php
intext:"cmd shell" filetype:asp
intext:"c99 shell" filetype:php
intext:"r57 shell" filetype:php  
intext:"wso shell" filetype:php
```

### 🔧 Network Command Tools
```
# Network Diagnostic RCE
inurl:"ping.php" 
inurl:"traceroute.php"
inurl:"whois.php"
intext:"ping" intext:"exec" filetype:php
intext:"nslookup" filetype:php
```

---

## 📁 LFI/RFI (File Inclusion) Dorks

### 🟢 Easy Level LFI/RFI Dorks (Beginner)
```
# Basic File Inclusion Parameters
inurl:"page=" filetype:php
inurl:"file=" filetype:php
inurl:"path=" filetype:php
inurl:"include=" filetype:php
inurl:"inc=" filetype:php
```

### 🟡 Medium Level LFI/RFI Dorks (Intermediate)
```
# Advanced Inclusion Patterns
inurl:"index.php?page="
inurl:"main.php?file="
inurl:"home.php?path="
inurl:"content.php?include="
inurl:"template.php?page="
```

### 🔴 Advanced Level LFI/RFI Dorks (Expert)
```
# Complex File Inclusion Detection
(inurl:"page=" | inurl:"file=" | inurl:"path=") & (filetype:php | filetype:asp)
(inurl:"include=" | inurl:"inc=" | inurl:"template=") & intext:"include"
```

### 🚀 Multi-Thread Level LFI/RFI Dorks (Mass Discovery)
```
# Bulk File Inclusion Discovery
((inurl:"page=" | inurl:"file=" | inurl:"path=" | inurl:"include=") & (filetype:php | filetype:asp | filetype:jsp)) -site:github.com
```

### 🔥 Crazy Level LFI/RFI Dorks (Extreme Discovery)
```
# Maximum File Inclusion Coverage
(((inurl:"page=" | inurl:"file=" | inurl:"path=" | inurl:"include=" | inurl:"inc=" | inurl:"template=") & (filetype:php | filetype:asp | filetype:jsp)) & (site:*.com | site:*.org | site:*.edu))
```

### 📂 Local File Inclusion (LFI)
```
# LFI-Specific Patterns
inurl:"page=" intext:"../../"
inurl:"file=" intext:"etc/passwd"
inurl:"path=" intext:"../../../"
inurl:"include=" intext:"/etc/"
```

### 🌐 Remote File Inclusion (RFI)
```
# RFI Configuration Detection
intext:"allow_url_include = On" filetype:php
intext:"allow_url_fopen = On" filetype:php
inurl:"include=" intext:"http://"
inurl:"page=" intext:"https://"
```

### 📄 Directory Traversal
```
# Path Traversal Patterns
inurl:"../" filetype:php
inurl:"..\\" filetype:asp
inurl:"path=" intext:".."
inurl:"dir=" intext:"../"
```

---

## 📤 File Upload Vulnerabilities

### 🟢 Easy Level File Upload Dorks (Beginner)
```
# Basic Upload Endpoints
inurl:"upload.php"
inurl:"fileupload.php" 
inurl:"file_upload.php"
inurl:"upload_file.php"
intitle:"file upload"
```

### 🟡 Medium Level File Upload Dorks (Intermediate)
```
# Upload with File Types
inurl:"upload.php" intext:"allowed"
inurl:"upload" intext:"file type"
inurl:"upload" intext:"extension"
inurl:"fileupload" intext:"format"
```

### 🔴 Advanced Level File Upload Dorks (Expert)
```
# Complex Upload Detection
(inurl:"upload" | inurl:"file_upload") & (intext:"php" | intext:"asp" | intext:"jsp")
(inurl:"upload.php" | inurl:"fileupload.php") & (intext:"allowed" | intext:"permitted")
```

### 🚀 Multi-Thread Level File Upload Dorks (Mass Discovery)
```
# Bulk Upload Discovery
((inurl:"upload" | inurl:"file_upload" | inurl:"fileupload") & (filetype:php | filetype:asp | filetype:jsp)) -site:github.com -site:w3schools.com
```

### 🔥 Crazy Level File Upload Dorks (Extreme Discovery)
```
# Maximum Upload Coverage
(((inurl:"upload" | inurl:"file_upload" | inurl:"fileupload" | inurl:"file-upload") & (intext:"form" | intext:"post" | intext:"multipart")) & (filetype:php | filetype:asp | filetype:jsp | filetype:html)) -site:github.com -site:w3schools.com
```

### 📷 Image Upload Vulnerabilities
```
# Image-Specific Upload Endpoints
inurl:"image_upload.php"
inurl:"photo_upload.php"  
inurl:"avatar_upload.php"
inurl:"picture_upload.php"
intext:"image upload" filetype:php
```

### 📄 Document Upload Vulnerabilities
```
# Document Upload Endpoints
inurl:"document_upload.php"
inurl:"file_manager.php" intext:"upload"
inurl:"resume_upload.php"
inurl:"cv_upload.php"
intext:"document upload" filetype:php
```

### 🎵 Media Upload Vulnerabilities
```
# Media File Upload
inurl:"media_upload.php"
inurl:"video_upload.php"
inurl:"audio_upload.php"
intext:"media upload" filetype:php
intext:"mp3 upload" | intext:"mp4 upload"
```

### ⚠️ Unrestricted File Upload
```
# Dangerous Upload Patterns
intext:"upload any file" filetype:php
intext:"no file restrictions" filetype:php
intext:"all file types allowed" filetype:php  
inurl:"upload" intext:"exe allowed"
```

### 🔍 Upload Path Disclosure
```
# Upload Directory Information
intext:"file uploaded to" filetype:php
intext:"upload successful" intext:"path"
intext:"uploaded to directory" filetype:php
inurl:"upload" intext:"folder created"
```

---

## 🔐 Configuration Files & Sensitive Data

### 🟢 Easy Level Configuration Dorks (Beginner)
```
# Basic Configuration Files
filetype:env
filetype:config
filetype:ini
filetype:conf
filetype:xml intext:"password"
```

### 🟡 Medium Level Configuration Dorks (Intermediate)
```
# Environment Files with Passwords
filetype:env intext:"DB_PASSWORD"
filetype:env intext:"API_KEY"
filetype:config intext:"password"
filetype:ini intext:"mysql"
filetype:xml intext:"database"
```

### 🔴 Advanced Level Configuration Dorks (Expert)
```
# Complex Configuration Discovery
(filetype:env | filetype:config | filetype:ini) & (intext:"password" | intext:"secret" | intext:"key")
(filetype:xml | filetype:json | filetype:yml) & (intext:"database" | intext:"mysql" | intext:"api")
```

### 🚀 Multi-Thread Level Configuration Dorks (Mass Discovery)
```
# Bulk Configuration Discovery
((filetype:env | filetype:config | filetype:ini | filetype:xml) & (intext:"password" | intext:"secret")) -site:github.com
```

### 🔥 Crazy Level Configuration Dorks (Extreme Discovery)
```
# Maximum Configuration Coverage
(((filetype:env | filetype:config | filetype:ini | filetype:xml | filetype:json | filetype:yml) & (intext:"password" | intext:"secret" | intext:"key" | intext:"token")) & (site:*.com | site:*.org | site:*.net))
```

### 💾 Database Configuration Files
```
# Database Config Exposure
"wp-config.php" filetype:txt
"database.yml" intext:"password"
"config.php" intext:"mysql_connect"
"db_config.php" filetype:txt
"connection.php" intext:"password"
```

### 🔑 API Keys and Secrets
```
# API Key Exposure
intext:"api_key" filetype:json
intext:"secret_key" filetype:txt
intext:"private_key" filetype:pem
intext:"access_token" filetype:json
intext:"auth_token" filetype:txt
```

### ☁️ Cloud Configuration
```
# AWS/Cloud Configuration
intext:"aws_access_key_id" filetype:txt
intext:"aws_secret_access_key" filetype:txt  
intext:"GOOGLE_APPLICATION_CREDENTIALS" filetype:json
intext:"azure_client_secret" filetype:txt
```

---

## 🗄️ Database Exposure Dorks

### 🟢 Easy Level Database Dorks (Beginner)
```
# Basic Database Files
filetype:sql
filetype:db
filetype:mdb
filetype:sqlite
filetype:dump
```

### 🟡 Medium Level Database Dorks (Intermediate)
```
# Database Files with Content
filetype:sql intext:"INSERT INTO"
filetype:sql intext:"CREATE TABLE"
filetype:sql intext:"password"
filetype:db intext:"users"
filetype:dump intext:"mysql"
```

### 🔴 Advanced Level Database Dorks (Expert)
```
# Complex Database Discovery
(filetype:sql | filetype:db | filetype:sqlite) & (intext:"password" | intext:"users" | intext:"admin")
(filetype:dump | filetype:backup) & (intext:"mysql" | intext:"database")
```

### 🚀 Multi-Thread Level Database Dorks (Mass Discovery)
```
# Bulk Database Discovery
((filetype:sql | filetype:db | filetype:sqlite | filetype:dump) & (intext:"password" | intext:"users")) -site:github.com
```

### 🔥 Crazy Level Database Dorks (Extreme Discovery)
```
# Maximum Database Coverage
(((filetype:sql | filetype:db | filetype:sqlite | filetype:dump | filetype:backup) & (intext:"INSERT INTO" | intext:"CREATE TABLE" | intext:"password" | intext:"users" | intext:"admin")) & (site:*.com | site:*.org | site:*.edu))
```

### 🗄️ Database Admin Tools
```
# Database Management Interfaces
intitle:"phpMyAdmin" "Welcome to phpMyAdmin"
intitle:"Adminer" "Login"  
intitle:"phpPgAdmin"
intitle:"SQL Web Data Administrator"
intitle:"MySQL Admin" filetype:php
```

### 💾 Database Backup Files
```
# Database Backup Discovery
"backup.sql" filetype:sql
"dump.sql" filetype:sql
"database.sql" filetype:sql
"db_backup" filetype:sql
"mysqldump" filetype:sql
site:*.edu filetype:sql intext:"CREATE TABLE"
```

### 🔗 Database Connection Strings
```
# Connection String Exposure
intext:"connectionstring" filetype:txt
intext:"Data Source=" filetype:config
intext:"Server=" intext:"Database=" filetype:txt
intext:"mysql_connect(" filetype:php
intext:"pg_connect(" filetype:php
```

---

## 🔑 Login Pages & Admin Panels

### 🟢 Easy Level Login Dorks (Beginner)
```
# Basic Login Pages
intitle:"login"
intitle:"admin login"
intitle:"administrator login"
inurl:"login.php"
inurl:"admin.php"
```

### 🟡 Medium Level Login Dorks (Intermediate)
```
# Advanced Login Discovery
intitle:"admin panel" "login"
intitle:"control panel" "login"
intitle:"dashboard" "login"
inurl:"admin" filetype:php
inurl:"administrator" filetype:asp
```

### 🔴 Advanced Level Login Dorks (Expert)
```
# Complex Login Detection
(intitle:"admin" | intitle:"administrator") & (intext:"login" | intext:"password")
(inurl:"admin" | inurl:"login") & (filetype:php | filetype:asp | filetype:jsp)
```

### 🚀 Multi-Thread Level Login Dorks (Mass Discovery)
```
# Bulk Login Discovery
((intitle:"admin" | intitle:"login" | intitle:"administrator") & (filetype:php | filetype:asp)) -site:github.com
```

### 🔥 Crazy Level Login Dorks (Extreme Discovery)
```
# Maximum Login Coverage
(((intitle:"admin" | intitle:"login" | intitle:"administrator" | intitle:"control panel") & (intext:"username" | intext:"password" | intext:"login")) & (filetype:php | filetype:asp | filetype:jsp))
```

### 🖥️ CMS Admin Areas
```
# Content Management System Logins
inurl:"wp-admin" "WordPress"
inurl:"administrator" "Joomla"
inurl:"admin" "Drupal"  
inurl:"typo3" "login"
inurl:"admin" "Magento"
```

### 🔐 Default Credential Hints
```
# Default Login Information
intitle:"login" intext:"admin" intext:"admin"
intitle:"login" intext:"root" intext:"root"
intitle:"login" intext:"guest" intext:"guest"
intitle:"default password" intext:"admin"
```

### 🏢 Corporate Login Panels
```
# Enterprise Login Systems
intitle:"employee login"
intitle:"staff login"
intitle:"corporate login"
intitle:"intranet login"
intitle:"portal login"
```

---

## 🏠 IoT & Network Devices

### 🟢 Easy Level IoT Dorks (Beginner)
```
# Basic IoT Device Discovery
intitle:"router login"
intitle:"camera view"
intitle:"printer status"
intitle:"modem configuration"
intitle:"device management"
```

### 🟡 Medium Level IoT Dorks (Intermediate)
```
# Advanced IoT Discovery
intitle:"wireless router" "configuration"
intitle:"IP camera" "login"
intitle:"network printer" "status"
intitle:"smart home" "control"
intitle:"IoT device" "management"
```

### 🔴 Advanced Level IoT Dorks (Expert)
```
# Complex IoT Detection
(intitle:"router" | intitle:"camera" | intitle:"printer") & (intext:"login" | intext:"admin")
(intitle:"IoT" | intitle:"smart") & (intext:"device" | intext:"control" | intext:"management")
```

### 🚀 Multi-Thread Level IoT Dorks (Mass Discovery)
```
# Bulk IoT Discovery
((intitle:"router" | intitle:"camera" | intitle:"printer" | intitle:"modem") & (intext:"login" | intext:"configuration")) -site:github.com
```

### 🔥 Crazy Level IoT Dorks (Extreme Discovery)
```
# Maximum IoT Coverage
(((intitle:"router" | intitle:"camera" | intitle:"printer" | intitle:"modem" | intitle:"IoT" | intitle:"smart") & (intext:"login" | intext:"admin" | intext:"configuration" | intext:"management")) & (site:*.com | site:*.net))
```

### 🌐 Router Interfaces
```
# Router Admin Panels
intitle:"DD-WRT" "router"
intitle:"OpenWrt" "configuration"
intitle:"pfSense" "login"
intitle:"MikroTik" "router"
intitle:"Cisco" "router" "login"
```

### 🖨️ Network Printers
```
# Printer Web Interfaces
intitle:"HP LaserJet" "configuration"
intitle:"Canon" "network printer"
intitle:"Epson" "printer" "status"
intitle:"Brother" "printer" "setup"
```

### 📡 Surveillance Systems
```
# Security Camera Systems
intitle:"security camera" "login"
intitle:"CCTV" "viewer"
intitle:"surveillance" "system"
intitle:"DVR" "login"
intitle:"NVR" "system"
```

---

## 📹 Web Cameras & Surveillance

### 🟢 Easy Level Camera Dorks (Beginner)
```
# Basic Camera Discovery
intitle:"webcam"
intitle:"camera view"  
intitle:"live view"
intitle:"video stream"
intitle:"IP camera"
```

### 🟡 Medium Level Camera Dorks (Intermediate)
```
# Advanced Camera Discovery
intitle:"webcam" "live view"
intitle:"IP camera" "viewer"
intitle:"security camera" "login"
intitle:"CCTV" "live"
intitle:"surveillance" "camera"
```

### 🔴 Advanced Level Camera Dorks (Expert)
```
# Complex Camera Detection
(intitle:"webcam" | intitle:"camera" | intitle:"CCTV") & (intext:"live" | intext:"view" | intext:"stream")
(intitle:"IP camera" | intitle:"security camera") & (intext:"login" | intext:"admin")
```

### 🚀 Multi-Thread Level Camera Dorks (Mass Discovery)
```
# Bulk Camera Discovery
((intitle:"webcam" | intitle:"camera" | intitle:"CCTV" | intitle:"surveillance") & (intext:"live" | intext:"view")) -site:github.com
```

### 🔥 Crazy Level Camera Dorks (Extreme Discovery)
```
# Maximum Camera Coverage
(((intitle:"webcam" | intitle:"camera" | intitle:"CCTV" | intitle:"surveillance" | intitle:"IP camera") & (intext:"live" | intext:"view" | intext:"stream" | intext:"monitor")) & (site:*.com | site:*.org))
```

### 📺 Live Streaming Cameras
```
# Public Camera Streams
inurl:"ViewerFrame?Mode="
inurl:"MultiCameraFrame?Mode="
intitle:"Live View" "AXIS"
intitle:"Network Camera" "Live"
inurl:"video.cgi"
```

### 🏢 Corporate Surveillance
```
# Business Security Systems
intitle:"office camera" "live"
intitle:"building security" "camera"
intitle:"parking camera" "view"
intitle:"entrance camera" "monitor"
```

### 🏠 Home Security Cameras
```
# Residential Camera Systems
intitle:"home camera" "view"
intitle:"baby monitor" "camera"
intitle:"pet camera" "live"
intitle:"driveway camera" "monitor"
```

---

## 🔌 API Endpoints

### 🟢 Easy Level API Dorks (Beginner)
```
# Basic API Discovery
inurl:"/api/"
inurl:"/rest/"
inurl:"/graphql"
inurl:"/v1/"
inurl:"/v2/"
```

### 🟡 Medium Level API Dorks (Intermediate)
```
# API Documentation Discovery
inurl:"/api/" "documentation"
inurl:"/api/" "swagger"
inurl:"/api/" "openapi"
inurl:"/rest/" "json"
inurl:"/graphql" "schema"
```

### 🔴 Advanced Level API Dorks (Expert)
```
# Complex API Detection
(inurl:"/api/" | inurl:"/rest/" | inurl:"/graphql") & (intext:"json" | intext:"xml" | intext:"swagger")
(inurl:"/v1/" | inurl:"/v2/" | inurl:"/v3/") & (intext:"endpoint" | intext:"documentation")
```

### 🚀 Multi-Thread Level API Dorks (Mass Discovery)
```
# Bulk API Discovery
((inurl:"/api/" | inurl:"/rest/" | inurl:"/graphql" | inurl:"/v1/") & (filetype:json | intext:"swagger")) -site:github.com
```

### 🔥 Crazy Level API Dorks (Extreme Discovery)
```
# Maximum API Coverage
(((inurl:"/api/" | inurl:"/rest/" | inurl:"/graphql" | inurl:"/v1/" | inurl:"/v2/") & (intext:"json" | intext:"xml" | intext:"swagger" | intext:"openapi")) & (site:*.com | site:*.org))
```

### 🔑 API Keys in URLs
```
# Exposed API Keys
inurl:"api_key="
inurl:"apikey="
inurl:"access_token="
inurl:"auth_token="
inurl:"bearer="
```

### 📊 API Documentation
```
# API Doc Discovery
intitle:"API Documentation"
intitle:"REST API"
intitle:"GraphQL Playground"
intitle:"Swagger UI"
intitle:"OpenAPI"
```

### 🔍 API Endpoints by Function
```
# Functional API Discovery
inurl:"/api/users"
inurl:"/api/admin"
inurl:"/api/auth"
inurl:"/api/login"
inurl:"/api/config"
inurl:"/api/debug"
```

---

## 💾 Backup Files

### 🟢 Easy Level Backup Dorks (Beginner)
```
# Basic Backup Files
filetype:bak
filetype:backup  
filetype:old
filetype:orig
filetype:tmp
```

### 🟡 Medium Level Backup Dorks (Intermediate)
```
# Backup Files with Content
filetype:bak intext:"password"
filetype:backup intext:"database"
filetype:old intext:"config"
filetype:tmp intext:"mysql"
filetype:orig intext:"admin"
```

### 🔴 Advanced Level Backup Dorks (Expert)
```
# Complex Backup Detection
(filetype:bak | filetype:backup | filetype:old) & (intext:"password" | intext:"database" | intext:"config")
(filetype:tmp | filetype:orig | filetype:save) & (intext:"admin" | intext:"mysql" | intext:"users")
```

### 🚀 Multi-Thread Level Backup Dorks (Mass Discovery)
```
# Bulk Backup Discovery
((filetype:bak | filetype:backup | filetype:old | filetype:tmp) & (intext:"password" | intext:"config")) -site:github.com
```

### 🔥 Crazy Level Backup Dorks (Extreme Discovery)
```
# Maximum Backup Coverage
(((filetype:bak | filetype:backup | filetype:old | filetype:tmp | filetype:orig) & (intext:"password" | intext:"database" | intext:"config" | intext:"admin")) & (site:*.com | site:*.edu | site:*.org))
```

### 🗜️ Archive Backup Files
```
# Compressed Backup Discovery
filetype:zip intext:"backup"
filetype:rar intext:"backup"
filetype:tar intext:"backup"
filetype:7z intext:"backup"
filetype:gz intext:"backup"
```

### 💾 Database Backup Files
```
# Database Backup Discovery
"backup.sql" filetype:sql
"dump.sql" filetype:sql
"database_backup" filetype:sql
"db_backup" filetype:sql
"mysql_backup" filetype:sql
```

### 🗂️ Configuration Backup Files
```
# Config Backup Discovery
"config.bak" filetype:bak
"wp-config.bak" filetype:bak
"database.bak" filetype:bak
"settings.backup" filetype:backup
```

---

## 📝 Log Files

### 🟢 Easy Level Log Dorks (Beginner)
```
# Basic Log Files
filetype:log
filetype:txt intext:"log"
intitle:"log" filetype:txt
inurl:"log" filetype:txt
inurl:"logs" filetype:log
```

### 🟡 Medium Level Log Dorks (Intermediate)
```
# Specific Log Types
filetype:log intext:"error"
filetype:log intext:"access"
filetype:log intext:"debug"
filetype:log intext:"exception"
filetype:log intext:"warning"
```

### 🔴 Advanced Level Log Dorks (Expert)
```
# Complex Log Detection
(filetype:log | filetype:txt) & (intext:"error" | intext:"exception" | intext:"debug")
(inurl:"log" | inurl:"logs") & (intext:"admin" | intext:"password" | intext:"login")
```

### 🚀 Multi-Thread Level Log Dorks (Mass Discovery)
```
# Bulk Log Discovery
((filetype:log | filetype:txt) & (intext:"error" | intext:"access" | intext:"debug")) -site:github.com
```

### 🔥 Crazy Level Log Dorks (Extreme Discovery)
```
# Maximum Log Coverage
(((filetype:log | filetype:txt) & (intext:"error" | intext:"access" | intext:"debug" | intext:"exception" | intext:"warning")) & (site:*.com | site:*.org | site:*.edu))
```

### 🖥️ Server Log Files
```
# Server-Specific Logs
"error.log" filetype:log
"access.log" filetype:log
"server.log" filetype:log
"apache.log" filetype:log
"nginx.log" filetype:log
```

### 💻 Application Log Files
```
# Application-Specific Logs
"debug.log" filetype:log
"app.log" filetype:log
"application.log" filetype:log
"laravel.log" filetype:log
"php.log" filetype:log
```

### 🔒 Security Log Files
```
# Security-Related Logs
"security.log" filetype:log
"auth.log" filetype:log
"firewall.log" filetype:log
"intrusion.log" filetype:log
"audit.log" filetype:log
```

---

## 🧪 Development & Testing

### 🟢 Easy Level Development Dorks (Beginner)
```
# Basic Development Environments
inurl:"dev"
inurl:"test"
inurl:"staging"
inurl:"beta"
inurl:"demo"
```

### 🟡 Medium Level Development Dorks (Intermediate)
```
# Development Environment Detection
inurl:"dev" filetype:php
inurl:"test" filetype:asp
inurl:"staging" filetype:jsp
inurl:"beta" intext:"development"
inurl:"demo" intext:"test"
```

### 🔴 Advanced Level Development Dorks (Expert)
```
# Complex Development Detection
(inurl:"dev" | inurl:"test" | inurl:"staging") & (filetype:php | filetype:asp | filetype:jsp)
(inurl:"beta" | inurl:"demo" | inurl:"localhost") & (intext:"development" | intext:"debug")
```

### 🚀 Multi-Thread Level Development Dorks (Mass Discovery)
```
# Bulk Development Discovery
((inurl:"dev" | inurl:"test" | inurl:"staging" | inurl:"beta") & (filetype:php | filetype:asp)) -site:github.com
```

### 🔥 Crazy Level Development Dorks (Extreme Discovery)
```
# Maximum Development Coverage
(((inurl:"dev" | inurl:"test" | inurl:"staging" | inurl:"beta" | inurl:"demo") & (filetype:php | filetype:asp | filetype:jsp)) & (site:*.com | site:*.org))
```

### 🐛 Debug Information
```
# Debug Mode Detection
intext:"debug" intext:"true" filetype:php
intext:"error_reporting" intext:"E_ALL"
intext:"display_errors" intext:"On"
intext:"debug mode" intext:"enabled"
```

### 📁 Git Repository Exposure
```
# Git Repository Discovery
inurl:"/.git/"
intitle:"Index of /.git"
".git/config" filetype:txt
".git/HEAD" filetype:txt
inurl:".git" intext:"repository"
```

### 🔧 Configuration Files in Development
```
# Development Config Files
".env" filetype:env
".env.local" filetype:txt
"config.dev" filetype:txt
"settings.test" filetype:txt
"debug.config" filetype:config
```

---

## 🛒 E-commerce Vulnerabilities

### 🟢 Easy Level E-commerce Dorks (Beginner)
```
# Basic E-commerce Discovery
inurl:"shop"
inurl:"store"
inurl:"cart"
inurl:"checkout"
inurl:"product"
```

### 🟡 Medium Level E-commerce Dorks (Intermediate)
```
# E-commerce Platform Detection
inurl:"shop" "admin"
inurl:"store" "login"
inurl:"magento" "admin"
inurl:"woocommerce" "admin"
inurl:"shopify" "admin"
```

### 🔴 Advanced Level E-commerce Dorks (Expert)
```
# Complex E-commerce Detection
(inurl:"shop" | inurl:"store" | inurl:"cart") & (intext:"admin" | intext:"login")
(inurl:"magento" | inurl:"woocommerce" | inurl:"prestashop") & intext:"admin"
```

### 🚀 Multi-Thread Level E-commerce Dorks (Mass Discovery)
```
# Bulk E-commerce Discovery
((inurl:"shop" | inurl:"store" | inurl:"cart" | inurl:"product") & (intext:"admin" | intext:"login")) -site:github.com
```

### 🔥 Crazy Level E-commerce Dorks (Extreme Discovery)
```
# Maximum E-commerce Coverage
(((inurl:"shop" | inurl:"store" | inurl:"cart" | inurl:"product" | inurl:"checkout") & (intext:"admin" | intext:"login" | intext:"dashboard")) & (site:*.com | site:*.net))
```

### 💳 Payment Processing
```
# Payment Gateway Discovery
inurl:"payment" "gateway"
inurl:"checkout" "payment"
intext:"stripe" "api"
intext:"paypal" "integration"
intext:"credit card" "processing"
```

### 📦 Order Management
```
# Order System Discovery
inurl:"order" "management"
inurl:"orders" "admin"
inurl:"inventory" "system"
inurl:"product" "catalog"
```

### 🏪 Shopping Cart Systems
```
# Shopping Cart Discovery
intext:"shopping cart" "admin"
intext:"add to cart" filetype:php
inurl:"cart.php"
inurl:"basket.php"
inurl:"shopping.php"
```

---

## 🎓 Educational Resources

### 🟢 Easy Level Educational Dorks (Beginner)
```
# Basic Educational Sites
site:*.edu
site:testphp.vulnweb.com
site:demo.testfire.net
intitle:"deliberately vulnerable"
intitle:"intentionally vulnerable"
```

### 🟡 Medium Level Educational Dorks (Intermediate)
```
# Educational Vulnerable Applications
site:*.edu intext:"vulnerable"
site:*.edu intext:"penetration testing"
site:*.edu intext:"ethical hacking"
"damn vulnerable web application"
"webgoat" "deliberately vulnerable"
```

### 🔴 Advanced Level Educational Dorks (Expert)
```
# Complex Educational Discovery
(site:*.edu | site:*.org) & (intext:"vulnerable" | intext:"security testing")
(intext:"deliberately vulnerable" | intext:"intentionally vulnerable") & (filetype:php | filetype:asp)
```

### 🚀 Multi-Thread Level Educational Dorks (Mass Discovery)
```
# Bulk Educational Discovery
((site:*.edu | site:*.org) & (intext:"vulnerable" | intext:"security" | intext:"testing")) -site:github.com
```

### 🔥 Crazy Level Educational Dorks (Extreme Discovery)
```
# Maximum Educational Coverage
(((site:*.edu | site:*.org | site:*.ac.*) & (intext:"vulnerable" | intext:"security" | intext:"penetration testing" | intext:"ethical hacking")) & (filetype:php | filetype:asp | filetype:jsp))
```

### 🏫 Security Training Platforms
```
# Security Learning Sites
"mutillidae" "vulnerable"
"bwapp" "buggy web application"
"dvwa" "damn vulnerable"
"vulnhub" "vulnerable"
"hackthebox" "penetration testing"
```

### 📚 Cybersecurity Labs
```
# Academic Security Labs
site:*.edu "cybersecurity" "lab"
site:*.edu "information security" "course"
site:*.edu "penetration testing" "lab"
site:*.ac.* "ethical hacking"
```

### 🔬 Research Environments
```
# Security Research Sites
site:*.edu "vulnerability research"
site:*.org "security research"
site:*.edu "exploit development"
site:*.edu "malware analysis"
```

---

## 🛠️ Advanced Search Techniques

### 🔍 Search Operator Combinations
```
# Logical OR Combinations
(inurl:"admin" | inurl:"login") & filetype:php
(intext:"mysql" | intext:"sql" | intext:"database") & inurl:"php?id="
(site:*.edu | site:*.org | site:*.gov) & intext:"vulnerable"

# Exclusion Patterns
"sql injection" -site:github.com -site:stackoverflow.com -site:w3schools.com
"xss vulnerability" -site:owasp.org -site:portswigger.net
"file upload" -site:github.com -site:documentation

# Wildcard Usage
"password" filetype:* site:*.edu
"admin" inurl:* filetype:php
"database" intext:* site:*.gov
```

### 🌍 Geographic and Domain Targeting
```
# Country-Specific TLD Targeting
site:*.np (Nepal)
site:*.in (India)
site:*.pk (Pakistan)
site:*.bd (Bangladesh)
site:*.lk (Sri Lanka)
site:*.mm (Myanmar)
site:*.bt (Bhutan)

# Organization Type Targeting
site:*.edu (Educational)
site:*.gov (Government)
site:*.mil (Military)
site:*.org (Non-profit)
site:*.ac.* (Academic - International)
```

### 📅 Time-Based Searches
```
# Date Range Searches
after:2020 "data breach"
before:2022 "vulnerability disclosure"
after:2021 before:2023 "security incident"

# Recent Content Focus
after:2023 "zero day"
after:2022 "cve" "vulnerability"
```

### 🔗 File Type Combinations
```
# Multiple File Type Searches
(filetype:php | filetype:asp | filetype:jsp) "admin"
(filetype:txt | filetype:log | filetype:conf) "password"
(filetype:sql | filetype:db | filetype:mdb) "users"
(filetype:env | filetype:config | filetype:ini) "secret"
```

---

## 📖 Usage Guidelines & Best Practices

### 🎯 Effective Dorking Strategies
```
1. Start with Easy Level dorks for broad discovery
2. Use Medium Level for targeted reconnaissance  
3. Apply Advanced Level for specific vulnerabilities
4. Deploy Multi-Thread Level for mass discovery
5. Reserve Crazy Level for comprehensive assessments
```

### 🔒 Ethical Guidelines
```
✅ Always get explicit written permission
✅ Use only for authorized penetration testing
✅ Respect rate limits and avoid server overload
✅ Document findings for responsible disclosure
✅ Follow local laws and regulations
✅ Use VPN for anonymity and protection
```

### 🛡️ Operational Security (OPSEC)
```
🔐 Use VPN or Tor for anonymity
🔐 Rotate User-Agent strings regularly
🔐 Implement search delays between queries
🔐 Use different search engines alternately
🔐 Clear browser data between sessions
🔐 Monitor for detection and blocking
```

### 📊 Result Verification Process
```
1. Manual verification of discovered endpoints
2. Test for actual vulnerabilities (authorized only)
3. Document findings with screenshots
4. Classify severity levels appropriately
5. Prepare for responsible disclosure
```

---

## 🤝 Contributing to DorkBox

### 📝 How to Contribute
```
1. Fork the repository
2. Create a feature branch (git checkout -b new-dorks)
3. Add your tested and working dorks
4. Categorize by difficulty level
5. Test thoroughly before submission
6. Submit a pull request with clear descriptions
```

### 🎯 Contribution Categories Needed
```
- New vulnerability types and patterns
- Country/region-specific dorks
- Industry-specific dorks (healthcare, finance, etc.)
- Emerging technology dorks (blockchain, AI, etc.)
- Mobile application dorks
- Cloud service specific dorks
```

### ✅ Quality Standards
```
✅ All dorks must be tested and working
✅ Include difficulty level classification
✅ Provide clear descriptions and context
✅ Follow ethical usage guidelines
✅ Include real-world examples when possible
```

---

## 📚 Learning Resources & References

### 🎓 Educational Platforms
```
- OWASP Web Security Testing Guide
- PortSwigger Web Security Academy  
- HackerOne Hacktivity Reports
- SANS Penetration Testing Courses
- Cybrary Security Training
```

### 🛠️ Essential Tools Integration
```
- Burp Suite: Import discovered URLs for testing
- OWASP ZAP: Automated scanning of endpoints
- Nmap: Port scanning of discovered systems
- SQLmap: Automated SQL injection testing
- XSStrike: Cross-site scripting testing
- Nuclei: Fast vulnerability scanner
```

### 🌐 Alternative Search Engines
```
- Shodan: Internet-connected device search
- Censys: Internet asset discovery
- PublicWWW: Source code search engine
- BinaryEdge: Cybersecurity search engine
- Fofa: Cyberspace mapping
```

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License**.

### 🎯 License Summary:
- ✅ **Use** for security research and educational purposes
- ✅ **Attribution** required when using or referencing
- ❌ **No commercial use** without explicit permission
- ❌ **No redistribution** or derivative works allowed

### 📋 Usage Requirements:
- Must credit original author and repository
- Must link back to original source
- Use only for legal and ethical purposes
- Comply with all applicable laws and regulations

---

## ⚖️ Final Legal Notice

**🚨 IMPORTANT REMINDER 🚨**

This repository contains powerful search techniques that can discover sensitive information and vulnerable systems. The tools and techniques provided are intended solely for:

- **✅ Authorized security testing**
- **✅ Educational and research purposes**  
- **✅ Bug bounty programs within scope**
- **✅ Improving your own security posture**

**❌ NEVER USE FOR:**
- Unauthorized access to systems
- Malicious activities or attacks
- Violating terms of service
- Any illegal activities

By using this repository, you acknowledge that you understand these restrictions and agree to use the information responsibly and legally.

---

## 🌟 Support DorkBox

If this repository has helped you in your security research or educational journey:

⭐ **Give us a star on GitHub**  
🐛 **Report issues and suggest improvements**  
🤝 **Contribute your own working dorks**  
📢 **Share with the security community**  
💬 **Join discussions and provide feedback**

**Together, we can make the internet more secure through responsible research and ethical hacking! 🔒**

---

**Happy Ethical Hacking!** 🔍🛡️
