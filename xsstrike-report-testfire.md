
# Bug Bounty Report: Reflected XSS on demo.testfire.net

**Target URL:** http://demo.testfire.net/search.jsp?query=

**Vulnerability Type:** Reflected Cross-Site Scripting (XSS)

**Tool Used:** XSStrike v3.1.5  
**Environment:** Termux on Android

---

## 🔍 Description:

While testing the search parameter on `search.jsp`, I found a reflected XSS vulnerability that executed JavaScript code in the browser.

---

## ✅ Payload Used:

<a/+/oNmouSeoVER%0a=%0a[8].find(confirm)>v3dm0s

- **Efficiency:** 91  
- **Confidence:** 10  
- Payload successfully triggered JavaScript execution.

---

## 💥 Impact:

- JavaScript injection via URL parameter
- Can lead to cookie theft, phishing, and session hijacking

---

## 📸 Proof of Concept:

1. Opened the URL in browser with payload  
2. `confirm()` popup triggered  
3. Confirmed vulnerable endpoint

---

## 🧠 Notes:

- Reported via OpenBugBounty  
- Awaiting triage / approval (submitted on [insert date])

---

**Reported by:** Cyber Jatti 👑  
**GitHub:** https://github.com/alishba-hacks/bug-bounty-reports
