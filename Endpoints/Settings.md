# Organizations

- **Route:** `{server}/api/Settings`

## `Get` Disable Notification

- **Endpoint:** `POST /DisableNotification/{notificationId}`
- **Description:** Disable notification by its ID.
- **Parameters:**
  - `notificationId`: The ID of the notification to disable.
- **Response:**
  - `200 OK`: Boolean indicating if the notification was successfully disabled.
    ```json
    true
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Enable Notification

- **Endpoint:** `POST /EnableNotification/{notificationId}`
- **Description:** Enable notification by its ID.
- **Parameters:**
  - `notificationId`: The ID of the notification to enable.
- **Response:**
  - `200 OK`: Boolean indicating if the notification was successfully enabled.
    ```json
    true
    ```
  - `401 Unauthorized`: User not authorized to perform this action.
