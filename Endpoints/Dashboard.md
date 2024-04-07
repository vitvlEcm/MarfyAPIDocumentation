# Dashboard

- **Route:** `{server}/api/Dashboard`

### `Get` Dashboard

- **Endpoint:** `GET /`
- **Description:** Endpoint to obtain dashboard data.
- **Parameters:**

  - `nodeId`: Node from tree.
  - `orgId`: Current organization ID.

- **Response:**

  - `200 OK`: Dashboard data for initial page.
  - 2 objects

  ![Dashboard](../Images/Dashboard.png)

  - **significant values**:
    - collection
    - for boxes with values
    - Grouped to types
    - "values/size": 1 for small box, 2 for wide box
  - **technologies**
    - used for graphics in the upper half

  ```json
  {
    "significantValues": [
      {
        "name": "string",
        "description": "string",
        "technology": 0,
        "values": [
          {
            "id": 0,
            "name": "string",
            "desctription": "string",
            "value": "string",
            "unit": "string",
            "size": 0,
            "dateTime": "2024-04-01T21:24:11.095Z"
          }
        ]
      }
    ],
    "technologies": [
      {
        "name": "string",
        "id": 0,
        "typeId": 0,
        "typeName": "string",
        "description": "string",
        "sourceUnit": "string",
        "unitCategory": 0,
        "unit": "string",
        "manualUnit": "string",
        "value": "string",
        "lastInsert": "2024-04-01T21:24:11.095Z",
        "timerSeconds": 0,
        "modelRepositoryVariable": 0,
        "range": {
          "from": 0,
          "to": 0
        }
      }
    ]
  }
  ```

  - `401 Unauthorized`: User not authorized to perform this action.
