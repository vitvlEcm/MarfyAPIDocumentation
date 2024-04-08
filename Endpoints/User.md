# User

- **Route:** `{server}/api/User`

## `Get` Get User Details

- **Endpoint:** `GET /`
- **Description:** Endpoint to retrieve details about the current user.
- **Parameters:** None
- **Response:**
  - `200 OK`: User details.
    ```json
    {
      "name": "string",
      "surname": "string",
      "id": "string",
      "phoneNumber": "string",
      "email": "string"
    }
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Delete` Remove User

- **Endpoint:** `DELETE /`
- **Description:** Endpoint to remove the current user. Added for appstore policies.
- **Parameters:** None
- **Response:**
  - `200 OK`: User deleted successfully.
  - `401 Unauthorized`: User not authorized to perform this action.
