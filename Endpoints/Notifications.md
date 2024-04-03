# Notifications

- Get all custom notifications for user

## Response

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

# NotificationsForDevice/{deviceId}

# NotificationsHistory

## Response

```json
[
  {
    "times": [
      {
        "activationTime": "2024-04-03T09:33:34.013Z",
        "ackTime": "2024-04-03T09:33:34.013Z"
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

# NotificationTypes

## Response

```json
[
  {
    "name": "string",
    "priority": "string",
    "shortName": "string",
    "icon": "string",
    "color": "string",
    "textColor": "string"
  }
]
```
