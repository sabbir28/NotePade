# audioManager

The `audioManager` class provides methods for recording audio and sending it as a Base64-encoded string.

## Methods

### `startRecording(OutputStream outputStream)`

- Starts the audio recording.
- Parameters:
  - `outputStream`: The output stream to send the recorded audio data.
- This method will create a temporary audio file, start the audio recording using the device's microphone, and send the recorded audio data through the provided output stream.

### `stopRecording(OutputStream outputStream)`

- Stops the audio recording and sends the recorded audio data.
- Parameters:
  - `outputStream`: The output stream to send the recorded audio data.
- This method will stop the audio recording, release the media recorder resources, send the recorded audio data as a Base64-encoded string through the output stream, and delete the temporary audio file.

### `sendData(File file, OutputStream outputStream)`

- Sends the recorded audio data as a Base64-encoded string.
- Parameters:
  - `file`: The temporary audio file containing the recorded audio data.
  - `outputStream`: The output stream to send the recorded audio data.
- This method will read the recorded audio data from the file, encode it as a Base64 string, and send it through the output stream.

## Usage

To use the `audioManager` class, create an instance of the class and call the `startRecording` method to start recording audio, and call the `stopRecording` method to stop recording and send the recorded audio data.

Example:
```java
audioManager audioManager = new audioManager();
audioManager.startRecording(outputStream);
// ...
audioManager.stopRecording(outputStream);
