# tanvirinfosec-recon-framework
A modular, authorized‑testing recon automation framework with reporting, tool checks, and structured output.
This tool does **not** perform exploitation.  
It focuses on **organization, reporting, and recon automation** for authorized security assessments.

## Features
- Tool checking and update logic
- Per‑domain workspace creation
- URL, JS, parameter, and subdomain collection
- Screenshot capture
- Markdown report generation
- Severity breakdown (Low/Medium/High/Critical)
- Manual finding templates with tags (IDOR, BAC, CSRF, XSS, SQLi, LFI, RCE, etc.)

## Usage
tanvirinfosec -d example.com

## Legal Disclaimer
This tool is intended for **authorized security testing and educational purposes only**.  
Do not use this tool on systems you do not own or have explicit permission to test.  
The author is not responsible for any misuse or damage caused by this tool.
Save and exit.


##INSTALLATION ON Mac#

Prerequisites
Before installing, make sure you have:

macOS (Apple Silicon recommended)

Homebrew installed
Install if missing:

bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
Go (1.22+) installed
Install if missing:

bash
brew install go
Clone the Repository
bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
Install the Script Globally
Move the script into your PATH:

bash
sudo mv tanvirinfosec /opt/homebrew/bin/
sudo chmod +x /opt/homebrew/bin/tanvirinfosec
Verify installation:

bash
which tanvirinfosec
Expected output:

Code
/opt/homebrew/bin/tanvirinfosec
Create Your Recon Workspace
This folder will store all recon results:

bash
mkdir -p ~/reconn/TANVIRAHMEDCS
🚀 USAGE (Add this to your README)
Run the full recon pipeline:

bash
tanvirinfosec -d example.com
This will:

Check for missing tools

Auto‑install required tools

Auto‑update existing tools

Create a workspace at:

Code
~/reconn/TANVIRAHMEDCS/example.com/
Run all recon modules:

Subdomains

DNS resolution

Port scanning

URL collection

JS file discovery

Parameter extraction

XSS candidate detection

Nuclei scanning

Screenshot capture

Generate:

report-summary.txt

report.md (pretty Markdown report)

📁 Output Structure
Your results will be organized like this:

Code
~/reconn/TANVIRAHMEDCS/example.com/
│
├── subdomains/
├── urls/
├── js/
├── parameters/
├── xss/
├── nuclei/
├── screenshots/
├── logs/
├── report-summary.txt
└── report.md
📝 Markdown Report
The tool generates a clean, ready‑to‑paste Markdown report including:

Severity breakdown (Low/Medium/High/Critical)

Subdomains

URLs

JS files

Parameters

XSS candidates

Nuclei findings

Manual finding template

Custom tags:

IDOR

BAC

CSRF

XSS

SQLi

LFI

RCE

Open Redirect

Upload flaws

API

JS logic

HTML/CSS


##INSTALLATION ON LINUX (Ubuntu / Debian / Kali)


1. Install dependencies
You need Git, Go, and Homebrew (Linuxbrew) or apt packages.

Install Git:
bash
sudo apt update
sudo apt install -y git
Install Go:
bash
sudo apt install -y golang
Verify:

bash
go version
2. Clone your repository
bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
3. Move the script into your PATH
Linux uses /usr/local/bin/ for global executables.

bash
sudo mv tanvirinfosec /usr/local/bin/
sudo chmod +x /usr/local/bin/tanvirinfosec
Verify:

bash
which tanvirinfosec
Expected:

Code
/usr/local/bin/tanvirinfosec
4. Create your recon workspace
bash
mkdir -p ~/reconn/TANVIRAHMEDCS
5. Run the pipeline
bash
tanvirinfosec -d example.com
This will:

Auto‑install missing tools

Auto‑update tools

Create workspace:

Code
~/reconn/TANVIRAHMEDCS/example.com/
Generate:

report-summary.txt

report.md

subdomains/

urls/

js/

xss/

nuclei/

screenshots/

logs/

🔵 INSTALLATION ON ARCH LINUX / MANJARO
Install Git + Go:
bash
sudo pacman -S git go --noconfirm
Clone repo:

bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
Move script:

bash
sudo mv tanvirinfosec /usr/local/bin/
sudo chmod +x /usr/local/bin/tanvirinfosec
Create workspace:

bash
mkdir -p ~/reconn/TANVIRAHMEDCS
Run:

bash
tanvirinfosec -d example.com
🟣 INSTALLATION ON FEDORA / RHEL / CENTOS
Install Git + Go:

bash
sudo dnf install -y git golang
Clone repo:

bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
Move script:

bash
sudo mv tanvirinfosec /usr/local/bin/
sudo chmod +x /usr/local/bin/tanvirinfosec
Create workspace:

bash
mkdir -p ~/reconn/TANVIRAHMEDCS
Run:

bash
tanvirinfosec -d 

🟦 INSTALLATION ON WINDOWS (PowerShell)
This works on:

Windows 10

Windows 11

Windows Server

And supports:

PowerShell

Git Bash

WSL (recommended)

🟢 OPTION 1 — BEST METHOD (WSL: Windows Subsystem for Linux)
If you want the same experience as Linux/macOS, use WSL.

✔ Recommended
✔ Easiest
✔ Full tool compatibility
✔ No path issues
Step 1 — Install WSL
Run PowerShell as Administrator:

powershell
wsl --install
Restart your PC.

Step 2 — Open Ubuntu (WSL)
Search in Start Menu:

Code
Ubuntu
Step 3 — Install Git + Go inside WSL
bash
sudo apt update
sudo apt install -y git golang
Step 4 — Clone your repo
bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
Step 5 — Install the script globally
bash
sudo mv tanvirinfosec /usr/local/bin/
sudo chmod +x /usr/local/bin/tanvirinfosec
Verify:

bash
which tanvirinfosec
Step 6 — Create workspace
bash
mkdir -p ~/reconn/TANVIRAHMEDCS
Step 7 — Run your pipeline
bash
tanvirinfosec -d example.com
Everything works exactly like Linux/macOS.

🟡 OPTION 2 — Git Bash on Windows (Works, but limited)
Some tools (like nuclei, naabu, dnsx) do not run natively on Windows.

If you still want to try:

Step 1 — Install Git Bash
Download from:
https://git-scm.com/download/win

Step 2 — Install Go for Windows
https://go.dev/dl/

Step 3 — Clone your repo
Open Git Bash:

bash
git clone https://github.com/<your-username>/tanvirinfosec-recon-framework.git
cd tanvirinfosec-recon-framework
Step 4 — Add script to PATH
Move it to a folder in PATH:

bash
mv tanvirinfosec /c/Users/<your-user>/bin/
chmod +x /c/Users/<your-user>/bin/tanvirinfosec
Add this folder to PATH in Windows settings.

Step 5 — Run
bash
tanvirinfosec -d example.com
⚠️ BUT:  
Many tools will fail because they are Linux binaries.

🔴 OPTION 3 — Native Windows (NOT recommended)
Most recon tools (subfinder, dnsx, naabu, nuclei, gowitness, etc.) are Linux-only.

You would need:

Windows versions of each tool

Manual PATH setup

Manual binary downloads

This becomes messy and unstable.

