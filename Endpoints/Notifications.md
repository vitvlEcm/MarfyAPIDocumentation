# Notifications

- **Route:** `{server}/api/Notifications`

## `Get` Notifications

- **Endpoint:** `GET /Notifications`
- **Description:** Endpoint to retrieve all custom notifications for the user.
- **Parameters:**
  - `nodeId`: Node from tree.
  - `orgId`: Current organization ID.
- **Response:**
  - `200 OK`: Collection of custom notifications for the user.
    ```json
    [
      {
        "name": "string",
        "id": 0,
        "text": "string",
        "status": true,
        "priority": "string",
        "type": "string",
        "typeId": 0
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Notifications History

- **Endpoint:** `GET /NotificationsHistory`
- **Description:** Endpoint to retrieve all custom notifications history for a specific user device.
- **Parameters:**
  - `OrganizationId`: ID of the selected organization. (Required)
  - `LocationId`: Optional filter to get only one alarm.
  - `Take`: Count of results in the response. Default is 500, max is 500. Request with a larger input returns 500.
  - `Skip`: Skips the first n entries, implemented for paging.
- **Response:**
  - `200 OK`: Custom notifications history retrieved successfully.
    ```json
    [
      {
        "times": [
          {
            "activationTime": "2024-04-07T18:05:37.592Z",
            "ackTime": "2024-04-07T18:05:37.592Z"
          }
        ],
        "notification": {
          "name": "string",
          "id": 0,
          "text": "string",
          "status": true,
          "priority": "string",
          "type": "string",
          "typeId": 0
        }
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Notification Types

- **Endpoint:** `GET /NotificationTypes`
- **Description:** Endpoint to retrieve all possible notification types.
- **Parameters:** None
- **Response:**
  - `200 OK`: Notification types retrieved successfully.
    ```json
    [
      {
        "Id": "integer",
        "Name": "string",
        "Priority": "string",
        "ShortName": "string",
        "Icon": "string",
        "Color": "string",
        "TextColor": "string"
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.
