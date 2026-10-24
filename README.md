# 💀 NullSpace-Resume-Engine
### Zero-Cost, Infinite-Design, Automated Resume Generation Pipeline (DeepSeek + Google Apps Script)

![Status](https://img.shields.io/badge/Status-Active-success)
![Cost](https://img.shields.io/badge/Cost-100%25%20Free-blue)
![Security](https://img.shields.io/badge/Category-Automation%20%7C%20DevSecOps-orange)
![License](https://img.shields.io/badge/License-MIT-green)

**NullSpace-Resume-Engine** is a completely serverless, zero-cost automation pipeline that builds pixel-perfect, ATS-friendly PDF/DOCX resumes using **Google Apps Script** and **AI (DeepSeek)**. 

No more fighting with broken Word margins, ugly tab-stops, or paying monthly fees to resume builders. You ask DeepSeek to write the script, paste it into Google, and the engine handles the rest.

---

## 🧠 Why "NullSpace"?
In mathematics and computer science, the "Null Space" is the set of vectors that map to zero. In this project, it represents the **void of manual formatting**. We start with an empty, blank document, send our data into the void, and the engine generates a flawless, structured piece of art. It's a nod to the hacker mindset: automating the boring stuff.

## 💡 The "Unlimited Design" Concept
Google Docs is free. Apps Script is free. DeepSeek is free. 
Because the design is written in **code** (JavaScript), you are not limited to 5 templates. You can change the font sizes, colors, margins, and layout by changing a single number in the script. You can generate **infinite** unique designs without paying a single rupee.

---

## 🧰 The Ingredients (What You Need)
To run this engine, you only need three things, all of which are **100% FREE**:
1. **A Google Account** (For Google Drive, Google Docs, and Google Apps Script).
2. **DeepSeek Access** — Use the web version at [chat.deepseek.com](https://chat.deepseek.com) OR install a browser extension for quick access:
   * **Chrome:** [DeepSeek AI on Chrome Web Store](https://chromewebstore.google.com/detail/deepseek-ai/fgbieegonkgdlkmeaapmkejdlfalonkb) [citation:1]
   * **Firefox:** [DeepSeek AI: Sidebar & Assistant on Firefox Add-ons](https://addons.mozilla.org/firefox/addon/deepseek-ai-sidebar-assistant/) [citation:4]
3. **A Web Browser** (Chrome, Edge, Firefox - no software installation required).

---

## 🚀 The Deep-Dive Step-by-Step Deployment Guide

### Step 1: Get the Code from DeepSeek
1. Open a new tab and go to [DeepSeek Chat](https://chat.deepseek.com) (or click the DeepSeek extension icon in your browser toolbar if you installed it).
2. Log in / Sign up (it's completely free).
3. Copy and paste this exact prompt into the chat:
   > *"Write a Google Apps Script (JavaScript) that uses the DocumentApp API to generate a perfectly formatted resume in Google Docs. It needs to include a header, a summary, technical skills, projects, and experience. Use borderless tables to right-align dates. Make links blue and clickable using setLinkUrl. Add horizontal lines under section headers using appendHorizontalRule. Set page margins to 36 points."*
4. DeepSeek will generate the entire `Code.gs` script.
5. **Copy the entire code block** it gives you.

### Step 2: Open Google Apps Script
1. Open a new tab and go to [Google Apps Script](https://script.google.com/).
2. Make sure you are logged into your Google Account (top right corner).
3. Click the **"+ New Project"** button.
4. At the top left, click on **"Untitled project"** and rename it to **"NullSpace-Resume-Engine"**.
5. You will see an empty code editor with `function myFunction() { }`.

### Step 3: Paste the Code
1. **Delete everything** inside the Apps Script editor (`function myFunction() { }`).
2. **Paste** the code DeepSeek gave you into the editor.
3. *(Optional)*: Scroll through the code and replace the placeholder text (like "Your Name", "Your Project") with your actual resume details.
4. Click the **Save** icon (💾) at the top.

### Step 4: Run & Authorize
1. Click the **Run** button (▶️) at the top of the editor.
2. A popup will appear: *"Authorization required."* Click **Review Permissions**.
3. Choose your Google Account from the list.
4. Google will show a warning screen: *"Google hasn't verified this app."* 
   * **DO NOT PANIC.** This is normal for personal scripts.
   * Click **"Advanced"** (bottom left).
   * Click **"Go to NullSpace-Resume-Engine (unsafe)"**.
5. Click **"Allow"**.

### Step 5: Retrieve Your Output Link
1. Wait a few seconds for the script to finish running.
2. Look at the **Execution Log** at the bottom of the screen.
3. You will see a message saying:
   `SUCCESS! Open your resume here: https://docs.google.com/document/d/...`
4. **Click that link.** 
5. It will open your perfectly formatted resume in a new Google Docs tab.
6. Go to **File > Download > Microsoft Word (.docx)** or **PDF Document (.pdf)**.

---

## ⚙️ Under the Hood (How the Code Works)

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

## 🚑 Troubleshooting

**Q: I get an error saying "DocumentApp is not defined".**
* **A:** Make sure you pasted the code exactly as DeepSeek gave it to you. Do not mix it with other scripts.

**Q: The script ran, but I can't find the document.**
* **A:** Go to your [Google Drive](https://drive.google.com), click "Recent", and look for a file named whatever you told the script to name it (e.g., "My Resume").

**Q: I want to change the font or colors.**
* **A:** Look in the code for `.setFontFamily("Arial")`. Change "Arial" to "Calibri", "Times New Roman", etc. Look for `.setForegroundColor(... "#1155cc")` to change the link color.

**Q: I want to add a new project.**
* **A:** In the code, just copy the `addTitleAndDate(...)` and `addBullet(...)` blocks, paste them under the Projects section, and change the text.

---

## 📜 License
This project is licensed under the MIT License. Fork it, break it, redesign it, and make it your own.

---
*Created by [Dickman Pious](https://github.com/dickmanpiouscyber)*


<img width="966" height="1468" alt="image" src="https://github.com/user-attachments/assets/df10b540-6f4f-4a88-89ff-8a472b2c1b74" />


<img width="1896" height="1178" alt="image" src="https://github.com/user-attachments/assets/8fe12d82-d232-462c-bda5-cd97a7aaab21" />


<img width="1324" height="418" alt="image" src="https://github.com/user-attachments/assets/b4931ad3-62e8-4296-8cae-91be7db8ad8c" />

