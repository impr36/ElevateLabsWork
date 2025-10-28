# 🔐 Task 6 — Create a Strong Password and Evaluate Its Strength

**Author:** Pratyush Raj  
**Date:** 28-10-2025  
**Platform Used:** [PasswordMeter.com](https://passwordmeter.com), [PasswordMonster.com](https://www.passwordmonster.com)

---

## 🧩 Objective
The goal of this task is to understand what makes a password strong, create multiple passwords with varying complexity, and evaluate their strength using online password strength testing tools.  

By analyzing the results, the objective was to identify **best practices for secure password creation** and understand how **password length and complexity** affect resistance to cyberattacks such as **brute-force** and **dictionary attacks**.

---

## 🧰 Tools Used

| Tool Name | Purpose |
|------------|----------|
| [PasswordMeter.com](https://passwordmeter.com) | To analyze password strength and obtain a numerical strength score and feedback. |
| [PasswordMonster.com](https://www.passwordmonster.com) | To analyze password strength and estimate the time required to crack a password. |
| Browser Console / Notes | To document results and perform analysis. |

---

## ⚙️ Step-by-Step Procedure

### **Step 1 — Understanding Password Strength Criteria**
Before testing, the following characteristics that contribute to password strength were reviewed:
- Use of uppercase and lowercase letters  
- Inclusion of numbers and symbols  
- Minimum length of 12–16 characters  
- Avoiding dictionary words and personal information  
- Use of unpredictable sequences  

---

### **Step 2 — Creating Sample Passwords**
Five passwords of varying complexity were created for analysis.

| Password | Type | Description |
|-----------|------|-------------|
| `123456` | Very Weak | Simple numeric sequence |
| `pratyush123` | Medium | Lowercase + digits |
| `Pratyush123` | Strong | Mixed case, includes digits |
| `Pratyush@123/` | Very Strong | Includes special characters, 13 characters long |
| `Pr@tYush#987/` | Very Strong | Randomized characters with high entropy |

---

### **Step 3 — Testing Passwords Using PasswordMeter**
Each password was tested on **PasswordMeter.com**, recording its score, strength level, and key feedback.

| Password | Score (%) | Strength Level | Key Feedback |
|-----------|------------|----------------|---------------|
| `123456` | 25% | Very Weak | Too short, only digits |
| `pratyush123` | 56% | Medium | Better complexity but predictable pattern |
| `Pratyush123` | 78% | Strong | Includes mixed case, digits, symbols |
| `Pratyush@123/` | 95% | Very Strong | Random sequence, excellent entropy |
| `Pr@tYush#987/` | 100% | Very Strong | Random sequence, excellent entropy |

---

### **Step 4 — Testing Passwords Using PasswordMonster**
Each password was further evaluated using **PasswordMonster.com** to estimate crack time and strength classification.

| Password | Strength Level | Estimated Crack Time | Classification |
|-----------|----------------|----------------------|----------------|
| `123456` | Very Weak | < 1 second | Extremely Weak |
| `pratyush` | Medium | 9 hours | Weak |
| `Pratyush123` | Strong | 4 months | Strong |
| `Pratyush@123/` | Very Strong | 91 years | Very Strong |
| `Pr@tYush#987/` | Very Strong | 11,000 years | Very Strong |

---

### **Step 5 — Observations and Learning**
- Password **length** greatly improves resistance to brute-force attacks.  
- Adding **symbols and case variation** increases entropy.  
- **Dictionary-based** passwords are highly vulnerable to dictionary attacks.  
- **Randomized or passphrase-based** passwords offer a strong balance between security and memorability.  
- **Password managers** help securely generate and store complex passwords.

---

## 📊 Results and Analysis

| Password | Strength (%) | Crack Time | Overall Rating |
|-----------|---------------|-------------|----------------|
| `123456` | 25% | < 1 sec | ❌ Weak |
| `pratyush123` | 56% | Minutes | ⚠️ Fair |
| `Pratyush123` | 78% | Weeks | ✅ Strong |
| `Pratyush@123/` | 92% | Years | 💪 Very Strong |
| `Pr@tYush#987/` | 100% | Centuries | 🏆 Excellent |

---

## ✅ Conclusion
Through this exercise, I gained a practical understanding of how **password composition** impacts its **strength and security**.  

**Key Takeaways:**
- Use passwords with **12+ characters** including uppercase, lowercase, numbers, and symbols.  
- Avoid predictable patterns or personal information.  
- Use **passphrases** or **password managers** for better security.  
- Strong passwords significantly reduce vulnerability to **brute-force** and **dictionary attacks**.

---

## 📚 References

[1] PasswordMonster, *Password Strength Checker and Analyzer*, 2024. [Online]. Available: [https://www.passwordmonster.com](https://www.passwordmonster.com)  

[2] NIST, *Digital Identity Guidelines (SP 800-63B)*, 2020. [Online]. Available: [https://pages.nist.gov/800-63-3/sp800-63b.html](https://pages.nist.gov/800-63-3/sp800-63b.html)  

[3] OWASP Foundation, *Authentication Cheat Sheet*, 2023. [Online]. Available: [https://owasp.org/Top10/A07_Identification_and_Authentication_Failures](https://owasp.org/Top10/A07_Identification_and_Authentication_Failures)  

[4] CISA, *Use Strong Passwords — Secure Our World Campaign*, 2024. [Online]. Available: [https://www.cisa.gov/secure-our-world/use-strong-passwords](https://www.cisa.gov/secure-our-world/use-strong-passwords)

---

## 📁 Repository Structure  

Task-6_Password_Strength/  
├── 📄 Task-6_ReadMe.md  
│  
├── 📂 Report/  
│ ├── 📘 Task 6_Report.pdf  
│ └── 📗 Task 6 - Interview Questions.pdf  
│  
└── 📂 Screenshots/  
├── 🖼️ PasswordMonster_1.png  
├── 🖼️ PasswordMonster_2.png  
├── 🖼️ PasswordMonster_3.png  
├── 🖼️ PasswordMonster_4.png  
├── 🖼️ PasswordMonster_5.png  
├── 🖼️ Password_Meter_1.png  
├── 🖼️ Password_Meter_2.png  
└── 🖼️ Password_Meter_3.png  
  
---
**© 2025 Pratyush Raj — ElevateLabs Pvt. Ltd. Cyber Security Internship**
