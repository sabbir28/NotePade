# Reverse Shell Android Application

This repository contains the source code for a Reverse Shell Android application. The application allows for remote control and monitoring of Android devices.

## Class Documentation

- [MainActivity](MainActivity.md): Provides the main entry point for the application and initiates the TCP connection.
- [broadcastReceiver](broadcastReceiver.md): Listens for a specific broadcast event and ensures that the main service is running.
- [controlPanel](controlPanel.md): Implements a control panel activity for the application with options to uninstall and restart the service.
- [functions](functions.md): Contains various utility methods used throughout the application.
- [jobScheduler](jobScheduler.md): Implements a job scheduler for scheduling background tasks in Android.
- [jumper](jumper.md): Initializes the application by checking network connectivity and starting the main service if necessary.
- [keypadListner](keypadListner.md): Listens for keypad events and starts the control panel activity when triggered.
- [mainService](mainService.md): Implements the main service for background execution of the reverse shell.
- [config](config.md): Contains configuration settings for the application.
- [tcpConnection](tcpConnection.md): Establishes and maintains the TCP connection with the remote server.

## Getting Started

To build and run the Reverse Shell Android application, follow these steps:

1. Clone the repository: `git clone <repository-url>`
2. Open the project in Android Studio.
3. Build and run the application on an Android device or emulator.

## License

This project is licensed under the [MIT License](LICENSE).

