# 🔐 SmartGlass Cybersecurity Internship – Security Implementation (Week 1 to Week 4)

## 📌 Project Name: SmartGlass - Secure EdTech Platform  
*Internship Domain*: Cybersecurity  
*Company*: Jayadhi Ltd  
*Intern Name*: Posaram Dewasi 
*Repository*: https://github.com/posurabari/SmartGlass-Cybersecurity 



## ✅ WEEK 1: Initial Security Risk Assessment

### 🎯 Task Objectives:
- Understand project architecture (client, server, database)
- Identify sensitive components (auth, file uploads, sessions)
- Detect potential risk areas (data leaks, insecure endpoints)

### 🔍 Actions Taken:
- Reviewed backend routes (/api/auth, /api/upload, etc.)
- Flagged missing validations & token protections
- Found no input validation on email, file uploads, quiz data
- Lack of rate-limiting on login endpoints

### ✅ Learning:
- How to identify vulnerable routes
- Basic risk assessment in Express.js & MongoDB projects


## ✅ WEEK 2: Secure Coding Guidelines & Static Review

### 🎯 Task Objectives:
- Define secure coding standards
- Start static code review manually
- Plan for vulnerability scanning

### 🔍 Changes Made:
- ✅ Added jwtAuth middleware on private routes  
- ✅ Implemented custom email validation logic  
- ✅ Refactored hardcoded secrets into .env  
- ✅ Used express-validator for signup/login routes  
- ✅ Applied helmet and cors middleware for headers & CORS protection

### ✅ Learning:
- Secure coding patterns in Node.js  
- Use of environment variables  
- Secure headers and input checks


## ✅ WEEK 3: Code Audits, Monitoring & Compliance

### 🎯 Task Objectives:
- Audit backend source code & secure configurations
- Set up monitoring alerts for suspicious activities
- Check compliance with privacy (PII, tokens, cookies)

### 🔍 Tasks Performed:
- ✅ Reviewed all API endpoints (auth.routes.js, upload.routes.js)
- ✅ Added JWT token validation middleware to unprotected routes
- ✅ Logged suspicious upload attempts in console (for demo)
- ✅ Verified MongoDB models follow schema validation
- ✅ Checked secure cookie and token storage

### 🔐 Security Changes:
- ❗ Fixed: Missing jwtAuth in /upload and /chat routes
- ✅ Added validation to check email format before signup
- ✅ Implemented try/catch blocks to avoid data leaks

### ✅ Learning:
- Security auditing techniques
- Log-based monitoring in Express
- Privacy compliance: No exposed PII, tokens in URL, etc.


## ✅ WEEK 4: Vulnerability Scans & Final Report

### 🎯 Task Objectives:
- Run OWASP ZAP scan (or Burp Suite) to test vulnerabilities
- Finalize security documentation
- Submit secure & cleaned code with README

### 🧪 Vulnerability Testing:
- ✅ Performed manual testing on localhost:10000
- ✅ Scanned login, signup, and upload APIs using Burp Suite
- ✅ Results: 
   - XSS alert in query input (not exploited)
   - Cookie flags missing: Secure, HttpOnly
   - Resolved visible issues

### 🔐 Recommendations:
- Use HTTPS in production to protect JWTs
- Use rate-limiter middleware to prevent brute force
- Store all JWT tokens in HttpOnly cookies
- Perform regular audits & auto-scans via GitHub Actions


## 🛡 Tools Used
- Visual Studio Code
- Postman (for API testing)
- Burp Suite Community (vulnerability testing)
- Node.js, Express.js, MongoDB
- express-validator, helmet, dotenv


## 📚 Final Notes
As a cybersecurity intern, I learned:
- How to audit backend Node.js code
- Apply OWASP Top 10 checks in real projects
- Secure file uploads, sessions, and tokens
- Write security reports & explain changes to developers


## 🗂 How to Run the Project Securely

```bash
# In /server directory
npm install
npm run dev

# In /client directory
npm install
npm run dev

# Environment variables (.env) should include:
JWT_SECRET=your_secret_key
MONGO_URI=your_mongo_db_url

<img width="859" height="373" alt="image" src="https://github.com/user-attachments/assets/5f150468-337b-404f-8280-411efb2c0810" />
<img width="940" height="425" alt="image" src="https://github.com/user-attachments/assets/d6883177-57db-4094-b96d-e2251ee3c3c0" />
![WhatsApp Image 2025-07-16 at 19 35 09_3028fa36](https://github.com/user-attachments/assets/0f777467-5735-4326-b7ec-9c14e46c5af4)


