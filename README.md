# 💀 NullSpace-Resume-Engine
### Zero-Cost, Infinite-Design, Automated Resume Generation Pipeline (AI + Google Apps Script)

![Status](https://img.shields.io/badge/Status-Active-success)
![Cost](https://img.shields.io/badge/Cost-100%25%20Free-blue)
![Security](https://img.shields.io/badge/Category-Automation%20%7C%20DevSecOps-orange)

**NullSpace-Resume-Engine** is a completely serverless, zero-cost automation pipeline that builds pixel-perfect, ATS-friendly PDF/DOCX resumes using **Google Apps Script** and **AI (DeepSeek/ChatGPT)**. 

No more fighting with broken Word margins, ugly tab-stops, or paying monthly fees to resume builders. You control the content via AI, and the engine handles the design via code.

---

## 🧠 Why "NullSpace"?
In cybersecurity and math, "Null Space" is the set of vectors that map to zero. In this project, it represents the **void of manual formatting**. We send empty instructions to the void, and the engine generates a flawless structure.

## 💡 The "Unlimited Design" Concept
Google Docs is free. Apps Script is free. DeepSeek is free. 
Because the design is written in **code** (JavaScript), you are not limited to 5 templates. You can change the font sizes, colors, margins, and layout by changing a single number in the script. You can generate **infinite** unique designs without paying a single rupee.

---

## 🧰 The Ingredients (What You Need)
To run this engine, you only need three things, all of which are **FREE**:
1. **A Google Account** (For Google Drive, Google Docs, and Google Apps Script).
2. **A DeepSeek Account** (or ChatGPT/Claude) - To rewrite your resume content, optimize keywords, and make it sound professional.
3. **A Web Browser** (Chrome, Edge, Firefox - no software installation required).

---

## 🚀 Step-by-Step Deployment Guide

### Step 1: Generate Content with AI (DeepSeek / ChatGPT)
1. Go to [DeepSeek Chat](https://chat.deepseek.com) or ChatGPT.
2. Give it your raw resume text and prompt it:
   > *"Rewrite my resume for a VAPT Analyst role. Make it ATS-friendly, use strong action verbs, and keep it to 1 page. Do not use emojis."*
3. Copy the text output. This is your **raw data**.

### Step 2: Open Google Apps Script
1. Go to [Google Apps Script](https://script.google.com/).
2. Click **"New Project"** (top left).
3. Rename the project from "Untitled project" to **"NullSpace-Resume-Engine"**.

### Step 3: Inject the Engine (The Code)
1. Delete the default `myFunction()` code in the editor.
2. Paste the entire `Code.gs` code from this repository into the editor.
3. *(Optional but recommended)*: Replace the text in the `addName()`, `addBullet()`, etc., functions with the AI-generated text from Step 1.

### Step 4: Authenticate & Execute
1. Click the **Save** icon (💾) at the top.
2. Click the **Run** button (▶️) at the top.
3. A popup will appear: *"Authorization required."* Click **Review Permissions**.
4. Choose your Google Account.
5. Google will warn you: *"Google hasn't verified this app."* Click **Advanced** -> **Go to NullSpace-Resume-Engine (unsafe)**.
6. Click **Allow**. (This is safe; the script only has permission to create documents in your own Google Drive).

### Step 5: Retrieve Your Masterpiece
1. Look at the **Execution Log** at the bottom of the screen. It will say:
   `SUCCESS! Open your resume here: https://docs.google.com/...`
2. Click that link. Your perfectly formatted resume is now in your Google Drive.
3. Open it and go to **File > Download > Microsoft Word (.docx)** or **PDF Document (.pdf)**.

---

## ⚙️ How It Works (Under the Hood)

This engine uses the `DocumentApp` API to create the document from absolute scratch. This bypasses the bugs of standard Word templates.

- **Borderless Tables for Alignment:** Standard Google Docs "Tab Stops" often break across pages, causing ugly gaps. This engine uses invisible, zero-width tables to perfectly right-align dates and locations on the exact same line.
- **Dynamic Hyperlinking:** The script uses `editAsText().setLinkUrl()`. It intelligently finds the URL strings, makes them clickable, colors them blue (`#1155cc`), and underlines them, while keeping the label (e.g., "GitHub:") black.
- **Native Horizontal Rules:** Injects true Google Docs horizontal lines under section headers for a clean, professional separation.
- **Margin Control:** Sets exact page margins in points (`36pts = 0.5 inches`) to maximize the 1-page layout without spilling to page 2.

---

## 🛡️ Why This is a Security & DevSecOps Flex
If you are a cybersecurity professional, this project proves:
1. **Automation Mindset:** You don't do things manually. You script them.
2. **API Manipulation:** You understand how to interact with cloud APIs (Google Drive API).
3. **Logic & Structure:** You know how to parse text and structure it securely.
4. **Zero-Dependency:** No third-party libraries, no npm installs, no supply-chain risk.

---

## 📜 License
This project is licensed under the MIT License. Fork it, break it, redesign it, and make it your own.

---
*Created by [Dickman Pious](https://github.com/dickmanpiouscyber)*
