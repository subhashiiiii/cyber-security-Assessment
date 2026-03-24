# Cyber Security Internship - Practical Exam

## Objective

The objective of this project is to identify, analyze, and mitigate common web application vulnerabilities using a vulnerable application.



## Application Used

* Damn Vulnerable Web Application (DVWA)



##  Environment Setup

### 1. Install Docker

Docker Desktop was installed from:
https://www.docker.com/products/docker-desktop/



### 2. Run DVWA Using Docker

Command used:
docker run -d -p 8080:80 vulnerables/web-dvwa



### 3. Access Application

Open browser and navigate to:
http://localhost:8080



### 4. Setup Database

* Go to: http://localhost:8080/setup.php
* Click **Create / Reset Database**



### 5. Login Credentials

Username: admin
Password: password



### 6. Security Configuration

* Navigate to DVWA Security
* Set security level to **LOW**



## Tools Used

* Burp Suite (Community Edition)
* Web Browser (Burp Browser)



## Vulnerabilities Identified

### 1. SQL Injection

* Input: `' OR '1'='1`
* Result: Retrieved all user records



### 2. Cross-Site Scripting (XSS - Stored)

* Input: `<script>alert('XSS')</script>`
* Result: Script executed in browser



### 3. Authentication Issue (Brute Force)

* Multiple login attempts allowed without restriction



### 4. Command Injection

* Input: `127.0.0.1; ls`
* Result: Executed system command



### 5. Security Misconfiguration

* Security level set to LOW
* No HTTPS
* Weak configuration





## Repository Structure

* report.pdf - Full security assessment report
* screenshots/ - Evidence of vulnerabilities
* README.md - Project documentation
