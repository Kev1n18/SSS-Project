# **Software Security - Final Project Report**

## **Introduction**
This project addresses vulnerabilities in software systems by exploring known attacks, security analysis tools, and methods for flaw mitigation. The main objective is to identify, exploit, and fix vulnerabilities in applications and systems.

---

## **Project Structure**

### **1. VulnApp**
Analysis of vulnerabilities in fictitious applications simulating real-world scenarios:
- **Attack Surfaces Analyzed:**
  - **File System:** Exploitation of files with malicious inputs.
  - **User Interface:** Command-line inputs used to manipulate programs.
  - **Buffer Manipulation:** Buffer overflows in `strcpy` and `memcpy` functions.
- **Exploitation Example:** Buffer overflow triggered by malformed files.
- **Mitigation:** Replace insecure functions with safer alternatives like `strncpy`.

---

### **2. SSS-DB**
Analysis and exploitation of vulnerabilities in a simulated database system:
- **Identified Vulnerabilities:**
  - **SQL Injection:** Malicious inputs used to access sensitive tables.
  - **Stored XSS:** Injected scripts stored and executed for subsequent users.
  - **Reflected XSS:** Exploitation of reflected input vulnerabilities.
  - **Command Injection:** Execution of server-side commands to access sensitive files.
- **Suggested Fixes:**
  - Sanitize inputs using regular expressions.
  - Implement security policies with tokenization and strict validation.

---

### **3. Tool Analysis**
#### **Flawfinder**
- Identification of vulnerabilities in unsafe functions like `memcpy` and `strcpy`.
- Usage of the `-F` option to filter false positives and focus on real risks.

#### **AFL (American Fuzzy Lop)**
- Fuzzing tests to discover vulnerabilities in simulated applications.
- Identification of issues like `segmentation faults` in processing functions.

---

### **4. Python Codes (COLE.py and LEAKS.py)**
- **Vulnerabilities:**
  - **Path Traversal in COLE.py:** Manipulation of file paths.
  - **OS Command Injection in LEAKS.py:** Unsafe use of `os.system`.
- **Mitigation:**
  - Replace `os.system` with `subprocess.run`.
  - Sanitize inputs using whitelists and strict validation.

---

## **Conclusion**
The project highlights the importance of identifying and fixing vulnerabilities in critical systems. Applying secure coding practices and leveraging specialized tools are essential to mitigating risks. The methodologies presented ensure greater resilience and protection against attacks.

---

## **Tools Used**
- **OWASP ZAP:** For exploring XSS and SQL Injection vulnerabilities.
- **Flawfinder:** Static code analysis tool.
- **AFL:** Fuzzing tests for vulnerable applications.
