# Farming API

The Farming API is a Flask-based web application that provides various endpoints for managing farming-related operations. It allows users to perform actions such as registration, login, fetching farmer and user data, inserting and removing food productions, and more.

## Endpoints

### 1. `/api/map` [GET, POST]

- **GET**: Retrieves a list of image positions from a text file.
  - Response: List of image positions in JSON format.

- **POST**: Saves the image position received in the request to a text file.
  - Request Body: JSON object containing `x` and `y` coordinates of the image position.
  - Response: Success message.

### 2. `/api/login` [POST]

- Logs in a user with the provided credentials.
  - Request Body: JSON object containing the `username` and `password`.
  - Response:
    - Success: Message indicating successful login.
    - Invalid credentials: Error message indicating invalid credentials.
    - User doesn't exist: Error message indicating the user doesn't exist.

### 3. `/api/registration` [POST]

- Registers a new user with the provided details.
  - Request Body: JSON object containing the `email`, `user_name`, and `password`.
  - Response:
    - Success: Message indicating successful registration.
    - Error: Error message indicating the registration failed.

### 4. `/api/get_farmer` [POST]

- Retrieves farmer data based on the provided farmer name.
  - Request Body: Form data containing the `farmer_name`.
  - Response:
    - Success: JSON object containing the farmer's data.
    - Error: Error message indicating the farmer doesn't exist.

### 5. `/api/get_user` [POST]

- Retrieves user data based on the provided username.
  - Request Body: Form data containing the `user_name`.
  - Response:
    - Success: JSON object containing the user's data.
    - Error: Error message indicating the user doesn't exist.

### 6. `/api/update_farmer_label` [POST]

- Updates the farmer label for the provided farmer name.
  - Request Body: Form data containing the `farmer_name`.
  - Response:
    - Success: JSON object containing the success message and updated crop permissions.
    - Error: Error message indicating the farmer doesn't exist.

### 7. `/api/food_production` [POST]

- Inserts a new food production record into the database.
  - Request Body: JSON object containing the `farmer_label`, `farmer_name`, `food_name`, `food_amount`, and `time_period`.
  - Response:
    - Success: Message indicating successful food production insertion.
    - Error: Error message indicating the insertion failed.

### 8. `/api/remove_food_production` [POST]

- Removes food production records for the provided farmer name and food name.
  - Request Body: JSON object containing the `farmer_name` and `food_name`.
  - Response:
    - Success: Message indicating successful removal of food production records.
    - Error: Error message indicating the removal failed.

### 9. `/api/get_available_food_productions` [POST]

- Retrieves available food production records for the provided farmer name.
  - Request Body: JSON object containing the `farmer_name`.
  - Response:
    - Success: JSON object containing the available food productions.
    - Error: Error message indicating no food productions found for the farmer.

## Usage

1. Start the Flask application by running the script.
2. Send HTTP requests to the respective endpoints using a tool like cURL, Postman, or a custom client.

**Note:** Make sure to customize the base URL in the provided C# code to match the actual base URL of your API.

That's a high-level overview of the Farming API and its endpoints. Feel free to modify and enhance the code as per your specific requirements.
