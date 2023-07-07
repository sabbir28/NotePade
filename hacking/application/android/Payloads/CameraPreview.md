# CameraPreview

The `CameraPreview` class provides methods for capturing photos using the device's camera and sending them as Base64-encoded strings.

## Constructor

### `CameraPreview(Context context)`

- Creates a new instance of the `CameraPreview` class.
- Parameters:
  - `context`: The context of the calling activity or application.

## Methods

### `startUp(int cameraID, OutputStream outputStream)`

- Starts the camera preview and captures a photo.
- Parameters:
  - `cameraID`: The ID of the camera to be used (0 for back camera, 1 for front camera).
  - `outputStream`: The output stream to send the captured photo data.
- This method will initiate the camera, start the preview, capture a photo, compress it as a JPEG image, encode it as a Base64 string, and send it through the provided output stream.

### `sendPhoto(byte[] data)`

- Sends the captured photo data as a Base64-encoded string.
- Parameters:
  - `data`: The byte array containing the photo data.
- This method will compress the photo as a JPEG image, encode it as a Base64 string, and send it through the output stream.

### `releaseCamera()`

- Releases the camera resources.
- This method should be called after capturing a photo to release the camera and stop the preview.

## Usage

To use the `CameraPreview` class, create an instance of the class and call the `startUp` method to capture a photo and send it through the output stream.

Example:
```java
CameraPreview cameraPreview = new CameraPreview(context);
cameraPreview.startUp(cameraID, outputStream);
```
