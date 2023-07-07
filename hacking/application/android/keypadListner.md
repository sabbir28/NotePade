# Keypad Listener BroadcastReceiver for Reverse Shell Android Application

This Markdown file describes the `keypadListener` class, which is a BroadcastReceiver used in the Reverse Shell Android application. It listens for keypad events and launches the control panel activity when a keypad event is received.

## BroadcastReceiver Overview

The `keypadListener` class extends the `BroadcastReceiver` class provided by the Android framework. It listens for keypad events and performs the necessary action when a keypad event is received.

## Code Explanation

```java
package com.example.reverseshell2;

import android.content.BroadcastReceiver;
import android.content.Context;
import android.content.Intent;
import android.util.Log;

public class keypadListener extends BroadcastReceiver {
    @Override
    public void onReceive(Context context, Intent intent) {
        Log.d("adadadd", "in");
        Intent i = new Intent(context, controlPanel.class);
        i.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
        context.startActivity(i);
    }
}
```

- The `keypadListener` class extends the `BroadcastReceiver` class to create a BroadcastReceiver component.
- The `onReceive` method is overridden and called when a keypad event is received.
  - The method receives the `context` and `intent` parameters.
  - A log message is printed indicating that a keypad event has been received.
  - An instance of the `controlPanel` class is created.
  - The `setFlags(Intent.FLAG_ACTIVITY_NEW_TASK)` method is used to set the intent flags for launching the activity.
  - The `startActivity` method is called to start the `controlPanel` activity.

## Usage

The `keypadListener` BroadcastReceiver is responsible for launching the control panel activity when a keypad event is received. The control panel activity provides additional functionality and options for the Reverse Shell Android application.

## Disclaimer

Please note that the use of this application may be subject to legal restrictions. The repository owner and contributors are not responsible for any misuse or illegal activities conducted with this application. Use it responsibly and ethically.

## License

The source code in this repository is licensed under the [MIT License](LICENSE).
