# WiFi Probe Request Monitor

A simple tool to monitor WiFi probe requests using Python and Scapy.

## Table of Contents

- [Requirements](#requirements)

- [Installation](#installation)

- [Usage](#usage)

- [Important Notes](#important-notes)

- [License](#license)


## Requirements

- Python 3.x
- Wireless adapter that supports monitor mode
- Root/sudo privileges

## Installation

1. Clone the repository:
```bash
git clone (https://github.com/richujoseph/wifi-probe-sniffer.git)
cd wifi-probe-monitor
```

2. Install requirements:
```bash
pip install scapy flask flask-socketio flask-cors
```

## Usage

1. Enable monitor mode on your wireless interface:
```bash
sudo ifconfig wlan0 down
sudo iwconfig wlan0 mode monitor
sudo ifconfig wlan0 up
```

2. Run the backend server (requires sudo):
```bash
sudo python3 probe_sniffer.py
```

3. Open `index.html` in a web browser or serve it using a simple HTTP server:
```bash
python3 -m http.server 8000
```

4. Visit `http://localhost:8000` in your browser

## Important Notes

- This tool should only be used on networks you have permission to monitor
- Some wireless adapters may not support monitor mode
- Requires root/sudo privileges to capture packets
- Keep the backend secure and not exposed to public internet

## License

MIT License

Copyright (c) [2025] [Richu Joseph]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

1. The above copyright notice and this permission notice shall be included in
   all copies or substantial portions of the Software.

2. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
   IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
   FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
   AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
   LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
   OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
   SOFTWARE.
