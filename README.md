# 📧 Phishing Email Analysis: Coinbase Spoof Example

## 🔍 Description

This repository contains an in-depth analysis of a real-world phishing email, designed to impersonate **Coinbase** in an attempt to steal user credentials or install malware via a malicious `.docx` attachment. The email was analyzed for common phishing traits and indicators to help users and analysts recognize and report such threats.

---

## 🚨 Phishing Indicators Found

### 📬 **Sender's Email Address (Spoofed)**

- **Display Name**: `support@mail.coinbase.com`  
- **Actual Address**:  
mssggeauthencti-cbspprt-325937197367@medisept.com.au

yaml

Copy

Edit
- ❗ **Red Flag**: The domain `medisept.com.au` is completely unrelated to Coinbase, indicating spoofing.

---

### 🧾 **Email Headers Discrepancy**

- SPF: `None`  
- DKIM: `None`  
- DMARC: `None`

> ❗ These email authentication methods are missing — a strong indicator of spoofing and illegitimacy.

---

### 📎 **Suspicious Attachments**

- **File Name**: `Coinbase -15392.docx`

> ❗ Legitimate financial institutions **never** send unsolicited `.docx` attachments. These files may contain **macros** or **malicious payloads**.

---

### ⚠️ **Urgent or Threatening Language**

- **Subject Line**:  
[Alert] Confirm your info is required [Case ID 153465]

yaml

Copy

Edit

> ❗ Language designed to create urgency and prompt action from the recipient without verification.

---

### 🔗 **Mismatched or Obfuscated URLs**

- The email uses **encoded and obscure routing** for links (actual target unknown).  
- Hovering likely reveals a **mismatched** or **malicious URL**.

> ❗ Hover text and actual link differ — a common phishing tactic.

---

### 📝 **Spelling or Grammar Issues**

- **Subject with Unicode Obfuscation**:
[A﻿l﻿e﻿r﻿t] Co﻿nf﻿i﻿rm yo﻿ur i﻿nfo is r﻿eq﻿uired﻿ [C﻿a﻿se ID 153465]

yaml

Copy

Edit

> ❗ Unicode or garbled text often used to bypass spam filters.

---

## 📊 Summary of Phishing Traits

| Indicator         | Status         | Comments                                               |
|------------------|----------------|--------------------------------------------------------|
| Sender Address    | ✅ Spoofed      | Mismatch between display name and actual domain       |
| Email Headers     | ✅ Suspicious   | SPF, DKIM, and DMARC missing                          |
| Attachment        | ✅ Suspicious   | `.docx` file, often used to deliver malware           |
| Urgency           | ✅ Present      | Phrases that incite fear or rush                      |
| Link Behavior     | ✅ Mismatched   | Encoded/obscured URLs for redirection                 |
| Grammar/Spelling  | ✅ Broken Text  | Misencoded subject line characters                    |

---

## 🛡️ Conclusion

This email is a **clear phishing attempt** posing as a security notification from Coinbase. It attempts to:

- Trick recipients into **opening a dangerous attachment**
- Spoof the sender to appear legitimate
- Bypass email filters with **Unicode manipulation**

---

## 📁 File Structure

```bash
sample-1002.eml          # Raw phishing email file
Coinbase -15392.docx     # Malicious attachment from the email
README.md                # Phishing analysis report
