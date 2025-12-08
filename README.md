# EC200U Cellular Monitor Dashboard

A modern web dashboard for real-time monitoring of Quectel EC200U cellular modules.

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow)
![License](https://img.shields.io/badge/License-MIT-yellow)

## ✨ Features

- **Real-time Monitoring**: Live signal quality (RSSI/BER) visualization
- **Dual Interface**: Simple mode for quick checks, Advanced mode for full control
- **Automatic Detection**: Auto-find EC200U module on USB ports
- **Responsive Design**: Works on desktop and mobile
- **REST API**: Clean FastAPI backend with comprehensive endpoints

## 🚀 Quick Start

### 1. Clone & Setup
```bash
git clone https://github.com/Faridi1419/ARMEDIA.git
cd ARMEDIA/back-end
pip install -r requirements.txt
python main.py
2. Open Dashboard
bash
cd ../front-end
python -m http.server 3000
Open http://localhost:3000 in your browser.

📁 Project Structure
text
ARMEDIA/
├── back-end/          # FastAPI server + serial communication
│   ├── main.py                 # Main server with REST API
│   ├── ec200u_module.py       # Core AT command handling
│   └── requirements.txt        # Python dependencies
├── front-end/         # Web dashboard (HTML/CSS/JS)
│   ├── index.html             # Dual-mode HTML interface
│   ├── style.css              # Modern CSS with animations
│   └── script.js              # Enhanced JavaScript logic
└── README.md

🔌 API Reference
Endpoint	Method	Description
/api/health	GET	System health check
/api/signal	GET	Get signal quality
/api/info	GET	Get module & SIM info
/api/command/{cmd}	GET	Send custom AT command

🎮 Dashboard Modes
Simple Mode
One-click connection to backend

Auto-refresh every 2 seconds

Real-time signal visualization

Basic module information

Advanced Mode
Port scanning and selection

Manual refresh control

Custom AT command console

Detailed logging system

📊 Signal Quality Guide
RSSI	Quality	Description
0-4	Very Poor	Marginal or no signal
5-9	Poor	Weak signal
10-14	Fair	Moderate signal
15-19	Good	Good signal
20-24	Very Good	Strong signal
25-31	Excellent	Excellent signal

👥 Team
Amir Radnia (@amirradnia99) - Backend & serial communication

Reza Faridi (@Faridi1419) - Frontend & dashboard design

🐛 Troubleshooting
Common Issues:
Backend not reachable - Ensure python main.py is running

No module detected - Check USB connection and power

No signal data - Verify SIM card and antenna

API errors - Check if port 8000 is available

Quick Fixes:
Restart backend server

Reconnect EC200U module

Check browser console (F12) for errors

Verify Python dependencies are installed

📄 License
MIT License - see LICENSE file for details.