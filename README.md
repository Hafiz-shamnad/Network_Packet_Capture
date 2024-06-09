# Network Traffic Analyzer

## Overview

The **Network Traffic Analyzer** is a graphical user interface (GUI) application designed to capture and display network traffic information. It uses `tkinter` for the GUI, `pyshark` for packet capturing, and `psutil` to list network interfaces.

## Features

- **Interface Selection**: Allows users to select a network interface from a dropdown menu.
- **Start and Stop Capture**: Users can start and stop the packet capture process.
- **Display Packet Information**: Captured packet details such as source IP, destination IP, protocol, and length are displayed in a scrollable text area.

## Installation

### Prerequisites

- Python 3.x
- `tkinter`
- `pyshark`
- `psutil`

### Installing Required Packages

To install the necessary Python packages, you can use `pip`:

```bash
pip install pyshark psutil
```

Note: `tkinter` is included with Python on Windows and macOS. On some Linux distributions, it may need to be installed separately.

### Installing `Wireshark`

`pyshark` relies on Wireshark's packet capturing capabilities. Ensure Wireshark is installed and accessible in your system's PATH.

- **Windows**: Download and install from [Wireshark Official Site](https://www.wireshark.org/download.html).
- **macOS**: Use Homebrew:
  ```bash
  brew install wireshark
  ```
- **Linux**: Use your package manager. For example, on Ubuntu:
  ```bash
  sudo apt-get install wireshark
  ```

## Usage

### Running the Application

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/network-traffic-analyzer.git
   cd network-traffic-analyzer
   ```

2. Run the Python script:
   ```bash
   python network_traffic_analyzer.py
   ```

### User Interface

- **Interface Dropdown**: Select the network interface to monitor.
- **Refresh Interfaces Button**: Refresh the list of available network interfaces.
- **Start Capture Button**: Begin capturing network traffic on the selected interface.
- **Stop Capture Button**: Stop the packet capture process.
- **Information Area**: Displays details about the captured packets.

## Code Overview

### Class: NetworkTrafficAnalyzer

- **`__init__(self, root)`**: Initializes the GUI components and styles.
- **`update_interfaces(self)`**: Updates the list of available network interfaces.
- **`start_capture(self)`**: Starts the packet capturing process in a separate thread.
- **`capture_packets(self, interface)`**: Captures packets continuously and displays their information.
- **`stop_capture(self)`**: Stops the packet capturing process.
- **`display_packet_info(self, packet)`**: Formats and displays the information of each captured packet.

### GUI Components

- **Main Frame**: Contains the interface selection dropdown and buttons.
- **Info Frame**: Contains the scrollable text area for displaying packet information.

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The `pyshark` library for packet capturing.
- The `psutil` library for system and network interface information.
- The `tkinter` library for GUI components.
