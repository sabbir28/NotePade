# Reverse Shell Android Application - Functions Class

The `functions` class in the Reverse Shell Android application provides various utility methods and functionalities. This document provides an overview of each method in the class.

## Class Overview

The `functions` class contains methods that handle different utility functionalities for the Reverse Shell Android application.

## Method Details

### `deviceInfo()`

Retrieves device information such as the manufacturer, version/release, product, model, brand, device, and host.

### `readFromClipboard()`

Retrieves the content from the clipboard if it contains plain text.

### `get_numberOfCameras()`

Retrieves the number of available cameras and their details (front or back).

### `jobScheduler(Context context)`

Schedules a job using the `JobScheduler` API to execute tasks periodically.

### `getPhoneNumber(Context context)`

Retrieves phone number details, including call state, IMEI/MEID numbers, mobile number, serial number, SIM operator name, SIM state, and country ISO.

### `getScreenUp(Activity activity)`

Enables various window flags to turn the screen on and dismiss the keyguard.

### `hideAppIcon(Context context)`

Disables the app icon by changing the component enabled setting.

### `unHideAppIcon(Context context)`

Enables the app icon by changing the component enabled setting.

### `overlayChecker(Context context)`

Checks if the app has the overlay permission and displays system-specific settings for enabling the permission if necessary.

### `createNotiChannel(Context context)`

Creates a notification channel for displaying foreground notifications.

Please note that the code provided is for reference purposes and may require additional implementation or modifications to suit your specific application needs.

