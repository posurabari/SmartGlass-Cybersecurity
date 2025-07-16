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

<img width="1908" height="1075" alt="Screenshot 2025-07-13 110747" src="https://github.com/user-attachments/assets/28eb267b-3b9c-4ab1-8d61-660c2c51e626" />
<img width="1895" height="993" alt="Screenshot 2025-07-13 113537" src="https://github.com/user-attachments/assets/10a72a90-a736-4a6c-9e26-6ee9c7b3349c" />
<img width="1893" height="1079" alt="Screenshot 2025-07-15 195553" src="https://github.com/user-attachments/assets/9c97306e-8e95-4a31-bef1-51ddb8cac29e" />


<img width="1273" height="805" alt="Screenshot 2025-07-16 193707" src="https://github.com/user-attachments/assets/28b29c4c-95a2-47f3-b369-9d30bc359c11" />


