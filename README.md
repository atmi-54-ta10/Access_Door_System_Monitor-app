# Access Door System Monitor APP (Raspberry Pi)

## Overview
This repository contains the Monitor Application for the Access Door System using Flutter, designed to run on a Raspberry Pi, and communicates with the server for real-time operations.

## Features
- Real-time control of door locks and indicators via GPIO pins
- Secure access control with real-time updates

## Setup and Installation

### Prerequisites
- Raspberry Pi with Raspbian OS installed
- Flutter SDK installed
- Python 3.x installed on the Raspberry Pi
- `pip` package manager

### Installation Steps

1. **Clone the repository:**
    ```sh
    git clone https://github.com/atmi-54-ta10/Access_Door_System_Monitor-app.git
    cd Access_Door_System_Monitor-app
    ```

2. **Install Flutter on Raspberry Pi:**
    Follow the official Flutter installation guide for Linux [here](https://flutter.dev/docs/get-started/install/linux).

3. **Build the App:**
    ```sh
    flutter build linux
    ```

4. **Make the executable file runnable:**
    ```sh
    chmod +x build/linux/release/bundle/monitor_app
    ```

5. **Create a shortcut on the desktop (app_monitor.desktop):**
    Create a file named `app_monitor.desktop` on the desktop with the following content:
    ```ini
    [Desktop Entry]
    Version=1.0
    Name=Monitor APP
    Comment=This is the Monitor APP for Access Door System
    Exec=/home/yourusername/Access_Door_System_Monitor-app/build/linux/release/bundle/monitor_app
    Icon=/home/yourusername/Access_Door_System_Monitor-app/assets/icon.png
    Terminal=false
    Type=Application
    ```
    Replace `/home/yourusername` with the actual path to your home directory.

6. **Move the desktop entry to Desktop:**
    ```sh
    mv app_monitor.desktop ~/Desktop/
    chmod +x ~/Desktop/app_monitor.desktop
    ```

### Running the Application
Double-click the `app_monitor.desktop` icon on the desktop to launch the application without opening a terminal.

### Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

### License
This project is licensed under the MIT License.

---

With these steps, you should be able to set up and run the Access Door System Monitor APP on your Raspberry Pi seamlessly. If you encounter any issues, feel free to reach out for support.
