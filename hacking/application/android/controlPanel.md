# Reverse Shell Android Application - Control Panel Class

The `controlPanel` class in the Reverse Shell Android application is responsible for displaying the control panel UI and handling user interactions. This Markdown document provides an overview of the class and its functionality.

## Class Overview

The `controlPanel` class extends `AppCompatActivity` and manages the control panel UI of the Reverse Shell Android application.

## Class Details

### `onCreate(Bundle savedInstanceState)`

The `onCreate` method is called when the activity is being created. It sets the layout for the activity and initializes the necessary variables and components.

- Retrieves the `activity` instance for later use.
- Schedules a job or starts the main service based on the Android version.
- Sets click listeners for the "Uninstall" and "Restart" buttons.

### "Uninstall" Button Click

When the "Uninstall" button is clicked, the following actions are performed:

- Finishes the current activity.
- Launches the uninstallation process for the application.
- Uses the `Intent.ACTION_UNINSTALL_PACKAGE` action to specify the package to uninstall.
- Sends the `Intent` with the package information and requests the uninstallation process to return the result.

### "Restart" Button Click

When the "Restart" button is clicked, the following actions are performed:

- Finishes the current activity.
- Executes the `tcpConnection` task to restart the reverse shell connection by passing the `activity` and application context, as well as the IP address and port information.
- Schedules a job using `JobScheduler` or starts the main service, based on the Android version, to maintain the reverse shell connection.

Please note that the code provided is for reference purposes and may require additional implementation or modifications to suit your specific application needs.

