# RTL-SDR IMSI Catcher with Live Dashboard

This project allows you to passively capture IMSI numbers from GSM mobile devices using an RTL-SDR dongle. It includes tools to scan GSM frequencies, decode IMSI information, and display results live on a simple web dashboard with carrier and country lookup.

## Features

- Automatic scanning for GSM frequencies based on region
- Real-time IMSI extraction and decoding using gr-gsm
- MCC/MNC lookup to resolve IMSI to country and operator names
- Live web dashboard showing IMSIs with timestamps and network info
- Easy installation and setup scripts for Ubuntu/Debian systems

## Requirements

- RTL-SDR compatible device (e.g., RTL2832U dongle)
- Ubuntu/Debian-based Linux system
- Python 3.6+
- Internet connection for installation and MCC/MNC database download

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/X3RX3SSec/IMSI_Catcher.git
   cd IMSI_Catcher
   ```

2. Run the installation script to install dependencies and tools:

   ```bash
   chmod +x install_imsi_tools.sh
   ./install_imsi_tools.sh
   ```

## Usage

1. Start the IMSI sniffer to scan and log IMSI data:

   ```bash
   chmod +x run_imsi_sniffer.sh
   ./run_imsi_sniffer.sh
   ```

   Select your region when prompted.

2. In a separate terminal, start the live web dashboard:

   ```bash
   python3 dashboard_server.py
   ```

3. Open your browser and go to:

   ```
   http://localhost:5000
   ```

   The dashboard will display captured IMSI numbers with country and operator details in real time.

## Project Structure

```
imsi-catcher/
├── install_imsi_tools.sh    # Installer script
├── run_imsi_sniffer.sh      # Script to run IMSI capture
├── dashboard_server.py      # Flask web server for dashboard
├── mcc-mnc.json             # MCC/MNC database for lookup
├── data/
│   └── imsis.json           # IMSI capture log
└── templates/
    └── dashboard.html       # Dashboard frontend template
```

## Notes and Legal Disclaimer

- This project is intended **for educational and research purposes only**.
- Passive IMSI capturing may be subject to local laws and regulations. Ensure you have permission and are compliant with all applicable laws before use.
- This tool does **not** actively impersonate cell towers or interfere with network operations.

## Contributions

Contributions, suggestions, and bug reports are welcome. Feel free to open issues or pull requests.

## License

This project is licensed under the MIT License.

---

If you have any questions or want to collaborate, please get in touch!
