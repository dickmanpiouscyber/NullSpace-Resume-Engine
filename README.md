# 💀 NullSpace-Resume-Engine
### Zero-Cost, Infinite-Design, Automated Resume Generation Pipeline (ChatGPT + Google Apps Script)

![Status](https://img.shields.io/badge/Status-Active-success)
![Cost](https://img.shields.io/badge/Cost-100%25%20Free-blue)
![Security](https://img.shields.io/badge/Category-Automation%20%7C%20DevSecOps-orange)
![License](https://img.shields.io/badge/License-MIT-green)

**NullSpace-Resume-Engine** is a completely serverless, zero-cost automation pipeline that builds pixel-perfect, ATS-friendly PDF/DOCX resumes using **Google Apps Script** and **ChatGPT**. 

No more fighting with broken Word margins, ugly tab-stops, or paying monthly fees to resume builders. You control the content via ChatGPT, and the engine handles the design via code.

---

## 🧠 Why "NullSpace"?
In mathematics and computer science, the "Null Space" is the set of vectors that map to zero. In this project, it represents the **void of manual formatting**. We start with an empty, blank document, send our data into the void, and the engine generates a flawless, structured piece of art. It's a nod to the hacker mindset: automating the boring stuff.

## 💡 The "Unlimited Design" Concept
Google Docs is free. Apps Script is free. ChatGPT (Free Tier) is free. 
Because the design is written in **code** (JavaScript), you are not limited to 5 templates. You can change the font sizes, colors, margins, and layout by changing a single number in the script. You can generate **infinite** unique designs without paying a single rupee.

---

## 🧰 The Ingredients (What You Need)
To run this engine, you only need three things, all of which are **100% FREE**:
1. **A Google Account** (For Google Drive, Google Docs, and Google Apps Script).
2. **A ChatGPT Account** (Free tier works perfectly for text generation).
3. **A Web Browser** (Chrome, Edge, Firefox - no software installation required).

---

## 🚀 The Deep-Dive Step-by-Step Deployment Guide

### Step 1: Generate Your Content with ChatGPT
1. Open a new tab and go to [ChatGPT](https://chatgpt.com).
2. Log in / Sign up (the free tier is more than enough).
3. Paste your raw, unformatted resume text into the chat.
4. Copy and paste this exact prompt:
   > *"Act as an expert technical recruiter. Rewrite my resume for a VAPT Analyst role. Make it ATS-friendly, use strong action verbs, and keep the bullet points concise. I need a Professional Summary, Technical Skills (grouped), Projects, Experience, Certifications, and Education. Do not use emojis. Output as plain text."*
5. Copy ChatGPT's output and save it in a Notepad file. This is your **Data Payload**.

*(For advanced prompting techniques, see the "🧠 How to Prompt ChatGPT" section below).*

### Step 2: Set Up Your Google Environment
1. Open a new tab and go to [Google Apps Script](https://script.google.com/).
2. Make sure you are logged into your Google Account (top right corner).
3. Click the **"+ New Project"** button.
4. At the top left, click on **"Untitled project"** and rename it to **"NullSpace-Resume-Engine"**.
5. You will see an empty code editor with `function myFunction() { }`.

### Step 3: Inject the Engine (The Code)
1. Go to the `Code.gs` file in this GitHub repository.
2. Click the **"Copy raw contents"** button (top right of the code box).
3. Go back to your Google Apps Script tab.
4. **Delete everything** inside the editor (`function myFunction() { }`).
5. **Paste** the copied code into the editor.
6. *Optional:* Scroll through the code and replace the placeholder text in `addBullet("...")` with the ChatGPT-generated text from Step 1.
7. Click the **Save** icon (💾) at the top.

### Step 4: Authenticate & Execute
1. Click the **Run** button (▶️) at the top of the editor.
2. A popup will appear: *"Authorization required. This project requires your permission to access your data."* Click **Review Permissions**.
3. Choose your Google Account from the list.
4. Google will show a warning screen: *"Google hasn't verified this app."* 
   * **DO NOT PANIC.** This is normal for personal scripts.
   * Click **"Advanced"** (bottom left).
   * Click **"Go to NullSpace-Resume-Engine (unsafe)"**.
5. Click **"Allow"**.
6. The script will run. Look at the **Execution Log** at the bottom of the screen. You will see:
   `SUCCESS! Open your resume here: https://docs.google.com/...`

### Step 5: Retrieve & Export Your Masterpiece
1. Click the link in the Execution Log.
2. It will open a new tab with your perfectly formatted resume in Google Docs.
3. Go to **File > Download > Microsoft Word (.docx)** (for job portals).
4. Go to **File > Download > PDF Document (.pdf)** (for emailing recruiters).

---

## 🧠 How to Prompt ChatGPT for Maximum ATS Score

To get the best possible content from ChatGPT before feeding it to the engine, use these advanced prompts:

**1. The "Action Verb" Prompt:**
> *"Take my resume bullets and rewrite them starting with strong action verbs (e.g., Engineered, Architected, Exploited, Secured). Quantify results wherever possible with numbers or percentages."*

**2. The "Keyword Injection" Prompt:**
> *"Here is the Job Description for a VAPT Analyst role I am applying for. Extract the top 15 keywords and naturally integrate them into my resume summary and skills section."*

**3. The "One-Page Constraint" Prompt:**
> *"My resume is currently 2 pages long. Condense it into a strict 1-page format without losing any critical technical skills or project impact."*

**4. The "Formatting Fixer" Prompt:**
> *"Rewrite the following text into clean, ATS-friendly plain text. Remove all weird spacing, emojis, and symbols. Format it with clear ALL CAPS headers."*

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
* **A:** Make sure you pasted the code exactly as it is. Do not mix `Code.gs` with HTML files.

**Q: The script ran, but I can't find the document.**
* **A:** Go to your [Google Drive](https://drive.google.com), click "Recent", and look for a file named `Dickman Pious - VAPT Analyst Resume` (or whatever name is in the `addName` function).

**Q: I want to change the font or colors.**
* **A:** Look for `.setFontFamily("Arial")`. Change "Arial" to "Calibri", "Times New Roman", etc. Look for `.setForegroundColor(... "#1155cc")` to change the link color.

**Q: I want to add a new project.**
* **A:** In the code, just copy the `addTitleAndDate(...)` and `addBullet(...)` blocks, paste them under the Projects section, and change the text.

**Q: ChatGPT gave me text with bold markdown like `**Bold**`. Will the engine handle it?**
* **A:** No, the engine expects plain text. Before pasting into the script, ask ChatGPT: *"Output everything as plain text without markdown formatting."*

---

## 📜 License
This project is licensed under the MIT License. Fork it, break it, redesign it, and make it your own.

---
*Created by [Dickman Pious](https://github.com/dickmanpiouscyber)*
