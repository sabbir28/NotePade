# readCallLogs

The `readCallLogs` class provides functionality to read call logs from the device. It allows you to retrieve information about incoming and outgoing calls, including the phone number, contact name, call duration, call type, and call date.

## Constructor

### `readCallLogs(Context context, Activity activity)`

- Initializes a new instance of the `readCallLogs` class.
- Parameters:
  - `context`: The application context.
  - `activity`: The activity context.

## Methods

### `readLogs()`

- Retrieves call logs from the device.
- Returns:
  - A string containing the retrieved call logs.

## Usage

To use the `readCallLogs` class, create an instance of it by passing the application context and activity context to the constructor.

Example:
```java
readCallLogs callLogsReader = new readCallLogs(getApplicationContext(), this);
```

To read call logs from the device, call the `readLogs()` method.

Example:
```java
String callLogs = callLogsReader.readLogs();
```

The returned call logs will be in the form of a string, containing information such as the number, name, date, duration, and type of each call log entry.
