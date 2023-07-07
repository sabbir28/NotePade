# locationManager

The `locationManager` class provides functionality for retrieving device location using GPS or network providers. It allows you to get the latitude and longitude coordinates of the device's current location.

## Constructor

### `locationManager(Context context, Activity activity)`

- Initializes a new instance of the `locationManager` class.
- Parameters:
  - `context`: The application context.
  - `activity`: The activity context.

## Methods

### `location_init()`

- Initializes the location manager and checks if GPS and network providers are enabled.

### `getNetworkLocation()`

- Retrieves the device location using the network provider.
- The location updates are requested and the last known location is obtained.

### `getGPSLocation()`

- Retrieves the device location using the GPS provider.
- The location updates are requested and the last known location is obtained.

### `getLocation()`

- Retrieves the device location using the available providers (GPS or network).
- If both GPS and network providers are enabled, the GPS location is prioritized.
- Returns a string containing the location information in the format "Provider: Latitude: Longitude".

## Usage

To use the `locationManager` class, create an instance of it by passing the application context and activity context to the constructor.

Example:
```java
locationManager manager = new locationManager(getApplicationContext(), this);
```

To retrieve the device location, call the `getLocation()` method.

Example:
```java
String location = manager.getLocation();
```

Please adjust the content and formatting as needed for your documentation.
```

Please adjust the content and formatting as needed for your documentation.
