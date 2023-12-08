# Unity HTTP Request Script



The Unity HTTP Request script provides methods for making HTTP requests to a farming API using Unity's UnityWebRequest class. It supports various API endpoints such as login, registration, retrieving farmer data, updating farmer labels, inserting and removing food productions, and more.

## Dependencies

- Unity 3D Engine

## Usage

1. Attach the `HttpRequest` script to a GameObject in your Unity scene.
2. Replace the `baseUrl` constant in the script with your API's base URL.
3. Call the desired methods from other scripts to interact with the API.

## Methods

### 1. `Login(string username, string password, System.Action<string> callback)`

- Sends a login request to the API with the provided username and password.
- Parameters:
  - `username` (string): The username of the user.
  - `password` (string): The password of the user.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

### 2. `Registration(string email, string username, string password, System.Action<string> callback)`

- Sends a registration request to the API with the provided email, username, and password.
- Parameters:
  - `email` (string): The email of the user.
  - `username` (string): The username of the user.
  - `password` (string): The password of the user.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

### 3. `GetFarmer(string farmerName, System.Action<string> callback)`

- Retrieves farmer data from the API based on the provided farmer name.
- Parameters:
  - `farmerName` (string): The name of the farmer.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

### 4. `UpdateFarmerLabel(string farmerName, string newLabel, System.Action<string> callback)`

- Updates the farmer label for the provided farmer name.
- Parameters:
  - `farmerName` (string): The name of the farmer.
  - `newLabel` (string): The new label for the farmer.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

### 5. `GetAvailableFoodProductions(string farmerName, System.Action<string> callback)`

- Retrieves available food production records for the provided farmer name.
- Parameters:
  - `farmerName` (string): The name of the farmer.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

### 6. `InsertFoodProduction(string farmerLabel, string farmerName, string foodName, int foodAmount, string timePeriod, System.Action<InsertFoodProductionResponse> callback)`

- Inserts a new food production record into the API.
- Parameters:
  - `farmerLabel` (string): The label of the farmer.
  - `farmerName` (string): The name of the farmer.
  - `foodName` (string): The name of the food production.
  - `foodAmount` (int): The amount of food produced.
  - `timePeriod` (string): The time period of the food production.
  - `callback` (System.Action<InsertFoodProductionResponse>): A callback function that receives the API response as an `InsertFoodProductionResponse` object.

### 7. `RemoveFoodProduction(string farmerName, string foodName, System.Action<RemoveFoodProductionResponse> callback)`

-

 Removes a food production record from the API.
- Parameters:
  - `farmerName` (string): The name of the farmer.
  - `foodName` (string): The name of the food production to be removed.
  - `callback` (System.Action<RemoveFoodProductionResponse>): A callback function that receives the API response as a `RemoveFoodProductionResponse` object.

### 8. `GetUser(string username, System.Action<string> callback)`

- Retrieves user data from the API based on the provided username.
- Parameters:
  - `username` (string): The username of the user.
  - `callback` (System.Action<string>): A callback function that receives the API response as a string.

## Example Usage

```csharp
// Instantiate the HttpRequest object
HttpRequest httpRequest = new HttpRequest();

// Example usage of the GetFarmer method
string farmerName = "JohnDoe";
StartCoroutine(httpRequest.GetFarmer(farmerName, (response) => {
    if (response != null) {
        // Process the farmer data
        Debug.Log("Farmer data: " + response);
    } else {
        Debug.LogError("Failed to retrieve farmer data.");
    }
}));
```

## Notes

- Make sure to replace the `baseUrl` constant in the script with the actual base URL of your API.
- The provided script uses the `MiniJSON` class for JSON serialization. Ensure that you have the `MiniJSON` class available in your project.
- The script uses Unity's `UnityWebRequest` class to make HTTP requests, so make sure to include the necessary UnityWebRequest-related dependencies.

```

Please note that the documentation assumes familiarity with Unity and UnityWebRequest class. Make sure to provide any additional information or context specific to your API and Unity project.
