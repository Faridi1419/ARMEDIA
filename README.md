# EC200U Cellular Monitor Dashboard

A modern web-based dashboard for monitoring Quectel EC200U cellular modules with real-time signal quality visualization.

![Dashboard Preview](https://img.shields.io/badge/Status-Active-success)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 🚀 Features

### Backend (FastAPI Server)
- Real-time serial communication with EC200U module
- REST API endpoints for signal monitoring
- Automatic port detection
- AT command execution with error handling

### Frontend (Web Dashboard)
- Real-time signal quality visualization
- Modern, responsive UI with dark/light theme
- Signal strength bars with color coding
- Module information display
- Automatic refresh every 2 seconds
- Connection status monitoring

## 📁 Project Structure

🎨 Dashboard Features
Signal Monitoring: Real-time RSSI and BER display

Visual Indicators: Color-coded signal bars

Module Info: Display manufacturer and revision

SIM Status: Check SIM card readiness

Auto-refresh: Continuous monitoring every 2 seconds

Responsive Design: Works on mobile and desktop

👥 Contributors
Backend Development: Amir Radnia - Python serial communication and AT command implementation

Frontend & Dashboard: Reza Faridi - Web interface design and API integration

Project Integration: Both - System architecture and deployment

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
