# Nova-Security
Nova Security is a Python-based modular vulnerability scanner and monitoring agent. It scans local systems for software, ports, and CVEs, performs remote intelligence aggregation, logs data to a server or database, and optionally visualizes results in a web dashboard. Ideal for pentesters, sysadmins, and students.

# 🛡️ Nova Security Project

**📄 Short Description (350 chars):**  
Nova Security is a Python-based modular vulnerability scanner and monitoring agent. It scans local systems for software, ports, and CVEs, aggregates intelligence remotely, logs data to a server or database, and optionally visualizes results in a web dashboard. Ideal for pentesters, sysadmins, and learners.

---

## 🔹 Project Overview

Nova Security is designed to help security professionals, red teams, and system administrators automate system and network vulnerability discovery. The project is modular, lightweight, and can run both offline and online.

**Core Goal:**  
Autonomously gather system/network information, detect vulnerabilities, and optionally send reports to a central dashboard or database.

---

## 🧩 Modules & Features

| Module                     | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| 🧠 Local Scanner            | Detects running software, open ports, service banners, and system details. |
| 📦 Version Checker          | Compares installed software with latest known versions.                     |
| 💣 Vulnerability Scanner    | Queries CVEs using Vulners API or local database.                           |
| 🌐 Remote Uploader          | Sends gathered data to a central server or database for aggregation.       |
| 📡 Banner Grabber           | Uses sockets to extract service banners from open ports.                    |
| 🔐 Offline & Online Modes   | Works offline with local CVE dumps or online with live API queries.        |
| 🧩 Shell Command Deployable | One-liner to quickly run on any machine silently.                           |
| 📊 Logging / Web UI (Opt.)  | Optionally save logs to a file or visualize them in a web dashboard.       |

---

## ⚙️ Tech Stack

| Component          | Tools / Libraries                                      |
|-------------------|--------------------------------------------------------|
| Local Scan         | `psutil`, `nmap`, `socket`, `platform`                |
| Vulnerability Lookup | Vulners API, `requests`, `packaging.version`       |
| Remote Sync        | `Flask` / `FastAPI` server, HTTP POST                 |
| Storage            | JSON logs, MongoDB, SQLite                              |
| Optional UI        | `Tkinter` (local), Flask web dashboard                 |
| Automation         | Cron jobs, Python scheduling, `.env` for config       |

---

## 💻 Requirements

- **OS:** Linux / macOS / Windows (Python 3.9+)
- **Python Packages:** `psutil`, `nmap`, `requests`, `packaging`, `flask`, `fastapi`, `python-dotenv`
- **Optional Accounts/Keys:**
  - Vulners API (for CVE lookups)
  - GitHub token (optional, for pushing reports)
  - Remote server/database credentials (MongoDB, SQLite, etc.)

---

## 🛠️ Installation & Setup

1. **Clone Repository:**
```bash
git clone https://github.com/index-oss/nova-security-project.git
cd nova-security-project

2. Install Dependencies:



pip install -r requirements.txt

3. Configure Environment: Create a .env file in the root directory:



VULNERS_API_KEY=your_api_key
REMOTE_DB_URL=mongodb://user:pass@host:port/dbname

4. Initial Test Run:



python nova_agent.py -d 127.0.0.1

This will run a local scan on your machine and generate logs.

5. Optional Web Dashboard:



cd dashboard
python app.py

Open your browser at http://localhost:5000 to view results.


---

🚀 Usage

Run Local Scan:


python nova_agent.py --scan

Check Vulnerabilities:


python nova_agent.py --cve

Send Results to Server:


python nova_agent.py --upload

Full Workflow:


python nova_agent.py --full


---

🎯 Use Cases

Audience	Purpose

🔐 Pentesters	Fast recon & reporting during engagements
🧰 SysAdmins	Lightweight DevSecOps monitoring tool
🧪 Red Teams	Post-exploitation system inventory
🎓 Students	Learn system & network-level scripting



---

💡 Next Steps / Enhancements

[ ] Add authentication & encryption (API keys / JWT)

[ ] Build GUI or browser-based dashboard

[ ] Export results as PDF reports

[ ] Integrate Slack / Telegram alerts

[ ] Remote command execution (C2-lite)

[ ] Pack into a single binary with PyInstaller



---

📄 License

MIT License — feel free to use, modify, or contribute to this project.


---
