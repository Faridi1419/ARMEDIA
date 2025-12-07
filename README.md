
# EC200U Cellular Monitor Dashboard

A modern web-based dashboard for monitoring **Quectel EC200U** cellular modules with real-time signal quality visualization. The dashboard connects to a FastAPI backend that provides the necessary AT command-based data to monitor signal strength, module information, SIM status, and connection state.

![Dashboard Preview](https://img.shields.io/badge/Status-Active-success)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 🚀 Features

### Backend (FastAPI Server)
- Real-time serial communication with the EC200U module.
- REST API endpoints for signal monitoring, module info, SIM status, and connection state.
- Automatic port detection and AT command execution with error handling.

### Frontend (Web Dashboard)
- **Real-time Signal Quality Visualization**: RSSI, BER, and Signal strength bars.
- **Modern, Responsive UI**: Designed to work seamlessly across mobile and desktop platforms.
- **Connection Status Monitoring**: Displays real-time connection status and auto-refresh every 2 seconds.
- **Signal Bars**: Color-coded visual indicators of signal quality.
- **Module Information**: Displays module model, revision, and SIM card status.
- **Interactive Controls**: Port scanning, manual connection, and log clearing functionalities.
  
## 📁 Project Structure

### Frontend Features:
- **Signal Monitoring**: Displays real-time RSSI and BER.
- **Visual Indicators**: Color-coded signal strength bars indicating connection quality.
- **Module Info**: Displays manufacturer and revision details.
- **SIM Status**: Shows SIM card readiness.
- **Auto-refresh**: Continuous monitoring every 2 seconds.
- **Responsive Design**: Optimized for both mobile and desktop.

### Backend Features:
- **Automatic AT Port Detection**: Identifies available USB/COM interfaces.
- **AT Command Diagnostics**: `/connect`, `/disconnect`, `/status` endpoints.
- **Error-Handled Serial Communication**: Graceful failure management with buffer resets.

## 📄 Project Setup

### Prerequisites:
- Python 3.8+.
- FastAPI and Uvicorn for backend:
  ```bash
  pip install fastapi uvicorn pyserial
  ```

### Running the Backend:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ARMEDIA.git
   cd ARMEDIA
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```
4. The backend will be available at: `http://127.0.0.1:8000`

### Running the Frontend:
1. Open `index.html` in a web browser to use the dashboard UI.
2. The frontend automatically connects to the backend API to fetch and display the signal status.

## 👥 Contributors

- **Backend Development**: Amir Radnia – Python serial communication, AT command handling, FastAPI backend.
- **Frontend Development**: Reza Faridi – Web interface design, dashboard integration, API interaction.
- **Project Integration**: Amir Radnia & Reza Faridi – System architecture and deployment.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📝 Commit History (Frontend Update)

### Title: 
**Enhance Frontend UI: Real-time signal quality visualization, updated module info display, and connection status features**

### Description:
- Updated `index.html` to improve the layout and add real-time signal quality visualization.
- Enhanced `style.css` with responsive design for mobile and desktop, and improved the signal indicator styling for better visibility.
- Refined `script.js` to support real-time fetching and display of signal quality (RSSI and BER values) from the backend API.
- Integrated auto-refresh functionality with visual feedback for connection status (Connected/Disconnected).
- Added interactive components for managing serial ports, including port scanning and manual connection handling.
- Improved the overall user experience with a more responsive and visually appealing dashboard design.

These changes improve the dashboard's usability and real-time monitoring features, making it easier to track the signal strength and connection status of the EC200U cellular module.

---

## 📄 Troubleshooting

### 1. **No AT port detected**
- Ensure that the **EC200U module** is powered and visible (`/dev/ttyUSB*` or `COMx`).
  
### 2. **CORS or Browser Errors**
- Verify that the backend is running and accessible.
- Ensure the correct URL is used in the `script.js` file to connect to the backend.

### 3. **Unexpected Timeouts**
- Try replacing the USB cable or increasing the serial timeout in `SerialManager`.

### 4. **Log Errors in Dashboard**
- Use the "Clear Log" button to reset the log container and eliminate any error-related information.
