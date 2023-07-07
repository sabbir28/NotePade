# Reverse Shell Payloads

This repository contains a collection of payloads for a reverse shell application. These payloads provide various functionalities such as vibration, reading SMS messages, accessing call logs, capturing images, recording audio, and more.

## Payloads

- [CameraPreview](CameraPreview.md): Capture images using the device's camera and send them as Base64-encoded strings.
- [audioManager](audioManager.md): Record audio using the device's microphone and send the recorded audio data as Base64-encoded strings.
- [ipAddr](ipAddr.md): Retrieve the IP address and MAC address of the device.
- [locationManager](locationManager.md): Get the current location of the device using GPS or network providers.
- [newShell](newShell.md): Execute shell commands on the device and communicate with a remote server.
- [readCallLogs](readCallLogs.md): Read call logs from the device.
- [readSMS](readSMS.md): Read SMS messages from the device.
- [vibrate](vibrate.md): Vibrate the device for a specified number of times.
- [videoRecorder](videoRecorder.md): Record video using the device's camera and send the recorded video data as Base64-encoded strings.

## Usage

Each payload is provided as a separate class file. You can include the required payload class in your reverse shell application to add the desired functionality. Refer to the individual payload files for detailed usage instructions.
