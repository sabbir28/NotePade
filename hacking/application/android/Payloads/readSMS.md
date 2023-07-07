# readSMS

The `readSMS` class provides functionality to read SMS messages from the device. It allows you to retrieve SMS messages from the inbox or other message boxes.

## Constructor

### `readSMS(Context context)`

- Initializes a new instance of the `readSMS` class.
- Parameters:
  - `context`: The application context.

## Methods

### `readSMSBox(String box)`

- Retrieves SMS messages from the specified message box.
- Parameters:
  - `box`: The message box to read from. Possible values are:
    - "inbox": Retrieve SMS messages from the inbox.
    - "sent": Retrieve SMS messages from the sent box.
    - "draft": Retrieve SMS messages from the draft box.
    - "outbox": Retrieve SMS messages from the outbox.
    - "failed": Retrieve SMS messages from the failed box.
    - "queued": Retrieve SMS messages from the queued box.
- Returns:
  - A string containing the retrieved SMS messages.

## Usage

To use the `readSMS` class, create an instance of it by passing the application context to the constructor.

Example:
```java
readSMS smsReader = new readSMS(getApplicationContext());
```

To read SMS messages from a specific message box, call the `readSMSBox()` method and provide the desired message box.

Example:
```java
String inboxSMS = smsReader.readSMSBox("inbox"); // Read SMS messages from the inbox
```

The returned SMS messages will be in the form of a string, containing information such as the number, person, date, and body of each message.

Please adjust the content and formatting as needed for your documentation.
```

Please adjust the content and formatting as needed for your documentation.
