# Notifications

- Get all custom notifications for user
- **method**: _HttpGet_

## Response

### Example

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

### Example

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

- **method**: _HttpGet_

## Response

### Example

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
