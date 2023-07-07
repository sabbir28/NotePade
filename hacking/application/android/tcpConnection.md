# Reverse Shell Android Application

This GitHub repository contains the source code for a Reverse Shell Android application. The application establishes a reverse shell connection over TCP, allowing remote control and execution of commands on the Android device.

## Features

- Connect to a remote server using IP address and port.
- Execute shell commands on the Android device.
- Take pictures using the device's camera and send them to the server.
- Retrieve device information such as model, IP address, and MAC address.
- Read SMS messages from the inbox and sent items.
- Record audio and video.
- Retrieve location information.
- Access call logs and clipboard data.
- Vibrate the device.
- And more.

## Getting Started

To get started with this application, follow these steps:

1. Clone the repository using the following command:

   ```bash
   git clone https://github.com/your-username/reverse-shell-android.git
   ```

2. Open the project in Android Studio.

3. Build and run the application on your Android device or emulator.

4. Launch the application and provide the remote server's IP address and port to establish a connection.

## Project Structure

The repository has the following structure:

```
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── reverseshell2/
│   │   │   │               ├── Payloads/
│   │   │   │               │   ├── CameraPreview.java
│   │   │   │               │   ├── audioManager.java
│   │   │   │               │   ├── ipAddr.java
│   │   │   │               │   ├── locationManager.java
│   │   │   │               │   ├── newShell.java
│   │   │   │               │   ├── readCallLogs.java
│   │   │   │               │   ├── readSMS.java
│   │   │   │               │   ├── vibrate.java
│   │   │   │               │   └── videoRecorder.java
│   │   │   │               ├── config.java
│   │   │   │               ├── functions.java
│   │   │   │               ├── jumper.java
│   │   │   │               ├── mainService.java
│   │   │   │               └── tcpConnection.java
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       │   ├── activity_main.xml
│   │   │       │   └── ...
│   │   │       ├── values/
│   │   │       │   ├── strings.xml
│   │   │       │   └── ...
│   │   │       └── ...
│   │   └── ...
│   └── ...
├── .gitignore
├── LICENSE
└── README.md
```

- The `app/` directory contains the source code and resources for the Android application.
- The `src/` directory contains the main source code and resource files.
- The `java/` directory contains the Java source code files.
- The `com/example/reverseshell2/Payloads/` directory contains the payload classes for various functionalities.
- The `config.java` file contains configuration settings for the application.
- The `functions.java` file contains utility functions used throughout the application.
- The `jumper.java` file is used for initializing certain components.
- The `mainService.java` file represents the main service of the application.
- The `tcpConnection.java` file implements the background task for establishing and maintaining the reverse shell connection.
- The `res/` directory contains the resource files such as layout and string resources.

## Contribution

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

The source code in this repository is licensed under the [MIT License](LICENSE).

Please note that this application is intended for educational and testing purposes only. Use it responsibly and at your own risk.

## Disclaimer

The use of this application may be subject to legal restrictions. The repository owner and contributors are not responsible for any misuse or illegal activities conducted with this application. Use it responsibly and ethically.
