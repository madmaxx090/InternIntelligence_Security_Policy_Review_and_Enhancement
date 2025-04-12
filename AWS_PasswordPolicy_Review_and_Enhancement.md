# 📄 AWS Password Policy Review and Enhancement

## 🔍 Overview  
This report documents a security policy review and enhancement task performed on **Amazon Web Services (AWS)** with a focus on the **IAM Password Policy**. The objective is to evaluate the current policy, identify gaps, and improve it using security best practices and frameworks such as **NIST SP 800-63B** and **ISO/IEC 27001**.

---

## 🎯 Objective  
- Review AWS’s existing IAM password policy settings.  
- Identify gaps based on modern security standards.  
- Propose an enhanced password policy.  
- Provide practical steps to implement the improvements in AWS.  
- Increase overall access control and user account security.

---

## 📌 Existing AWS IAM Password Policy Settings (Example)

| Setting                         | Value          |
|----------------------------------|----------------|
| Minimum password length         | 8 characters   |
| Require at least one number     | ✅ Yes         |
| Require at least one symbol     | ✅ Yes         |
| Require at least one uppercase  | ✅ Yes         |
| Require at least one lowercase  | ✅ Yes         |
| Allow users to change password  | ✅ Yes         |
| Password expiration             | ❌ Disabled    |
| Password reuse prevention       | 3 passwords    |
| MFA enforcement                 | ❌ Not enforced|

---

## 🧩 Identified Gaps  

| Issue                        | Description |
|------------------------------|-------------|
| Weak minimum length          | 8 characters is acceptable but NIST recommends 12+ for stronger security. |
| No MFA enforcement            | Multi-factor authentication is essential for protecting against stolen passwords. |
| No expiration policy          | While NIST discourages frequent password changes, privileged users may benefit from periodic password expiration. |
| Low password history count    | A history count of 3 is low; NIST recommends at least 5 to prevent simple password cycling. |
| Lack of adaptive controls     | There are no adaptive controls like brute force protection or login location monitoring. |

---

## ✅ Recommended Enhancements  

| Setting                         | Recommended Value              | Justification |
|---------------------------------|--------------------------------|----------------|
| Minimum password length         | 12+ characters                 | Align with NIST SP 800-63B |
| Require uppercase/lowercase/num/symbol | ✅ Yes for all             | Encourages strong passwords and aligns with best practices. |
| Password expiration             | 90 days (for privileged users only) | Balances between security and convenience. |
| Password reuse prevention       | Last 5 passwords               | Makes it more difficult for users to cycle through old passwords. |
| MFA enforcement                 | ✅ Mandatory for all users     | Protects against password theft and unauthorized access. |
| Monitoring                      | Enable CloudTrail + GuardDuty | Detects anomalies, brute force attempts, and suspicious login patterns. |

---

## Reference Standards  

## NIST SP 800-63B (Digital Identity Guidelines):
- Minimum length of 8 characters, but **12+ characters** preferred for stronger security.  
- No strict composition rules, but can be used based on risk.  
- MFA is **strongly recommended**.  
- Avoid forced periodic password changes unless there is evidence of compromise.

## ISO/IEC 27001:
- Stresses the importance of **access control** (A.9).  
- Regular reviews of credentials and authentication mechanisms are required.  
- Password policies should be clearly documented and enforced.


## 🧠 Author  
Unaiza Fatima 
Cyber Security Intern  
LinkedIn:https://www.linkedin.com/in/unaiza-fatima-72451127b?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app 
GitHub: madmaxx090
Email: uneezakhan4@gmail.com

