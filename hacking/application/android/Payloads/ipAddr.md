# ipAddr

The `ipAddr` class provides methods for retrieving IP addresses and MAC addresses of the device's network interfaces.

## Methods

### `getMACAddress(String interfaceName)`

- Retrieves the MAC address of the specified network interface.
- Parameters:
  - `interfaceName`: The name of the network interface. Pass `null` to retrieve the MAC address of the default interface.
- Returns the MAC address as a string.

### `getIPAddress(boolean useIPv4)`

- Retrieves the IP address of the device.
- Parameters:
  - `useIPv4`: Specify `true` to retrieve the IPv4 address, or `false` to retrieve the IPv6 address.
- Returns the IP address as a string.

## Usage

To use the `ipAddr` class, simply call the static methods to retrieve the desired information.

Example:
```java
String macAddress = ipAddr.getMACAddress(null);
String ipAddress = ipAddr.getIPAddress(true);
```
