# Auth

- **Route:** `{server}/api/Auth`

## `Post` Login

- **Endpoint:** `POST /Login`
- **Description:** Initial JWT login endpoint.
- **Parameters:**
  - `Input`: Object with username and password.
    ```json
    {
      "UserName": "string",
      "Password": "string",
      "ApplicationId": "string"
    }
    ```
- **Response:**
  - `200 OK`: User info and JWT.
    ```json
    {
      "userName": "string",
      "name": "string",
      "surname": "string",
      "accessToken": "string",
      "accessExpiration": "2024-04-07T17:41:49.042Z",
      "refreshToken": "string",
      "refreshExpiration": "2024-04-07T17:41:49.042Z"
    }
    ```
  - `401 Unauthorized`: Unauthorized.
- **Exceptions:**
  - `HttpRequestException`: If login was successful but user info could not be obtained.

## `Post` Refresh Token

- **Endpoint:** `POST /RefreshToken`
- **Description:** Endpoint to refresh the access token using a refresh token.
- **Parameters:**
  - `refreshToken`: The refresh token.
- **Response:**
  - `200 OK`: Renewed access token.
    ```json
    {
      "accessToken": "string",
      "accessExpiration": "2024-04-07T17:41:49.047Z"
    }
    ```
  - `400 Bad Request`: Provided token is not readable.
  - `401 Unauthorized`: Token user not found.

## `Post` Reset Password

- **Endpoint:** `POST /ResetPassword`
- **Description:** Endpoint to reset the password for a user.
- **Parameters:**
  - `email`: The email of the user whose password is to be reset.
- **Response:**
  - `200 OK`: Email sent successfully.
  - `401 Unauthorized`: User with the provided email not found.
