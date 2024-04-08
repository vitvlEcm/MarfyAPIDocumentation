# Device

- **Route:** `{server}/api/Device`

## `Get` DeviceDashboard

- **Endpoint:** `GET /DeviceDashboard/{deviceId}`
- **Description:** Endpoint for obtaining data for a concrete device dashboard.
- **Parameters:**
  - `deviceId`: The ID of the device.
  - `orgId`: Current organization ID.
  - `Preset`: Use ID from `api/Stats/PossibleTimeseriesTimes`. To use `From` and `To` times, set this to -1.
  - `From`: Start DateTime.
  - `To`: End DateTime.
- **Response:**
  - `200 OK`: List of combined data models.
    ```json
    {
      "id": 0,
      "name": "string",
      "technologyId": 0,
      "technologyName": "string",
      "typeId": 0, //Deprecated = TechnologyId
      "typeName": "string", //Deprecated = TechnologyName
      "description": "string",
      "data": [
        {
          "id": 0,
          "name": "string",
          "unitCategory": 0,
          "unit": "string",
          "value": "string",
          "lastInsert": "2024-04-08T01:18:42.174Z",
          "significant": true, //device may have multiple significant values
          "primary": true, //unique, only one variable per device
          "timerSeconds": 0,
          "deviceName": "string",
          "modelRepositoryVariable": 0,
          "range": {
            "from": 0,
            "to": 0
          }
        }
      ],
      "timeseries": {
        "name": "string",
        "unit": "string",
        "aggregationName": "string",
        "variableId": 0,
        "data": [
          {
            "timestamp": "2024-04-08T01:18:42.174Z",
            "value": 0
          }
        ]
      }
    }
    ```
  - `400 Bad Request`: Node not present in the passed organization.
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Variables

- **Endpoint:** `GET /Variables`
- **Description:** Endpoint to obtain all variables in specific device.
- **Parameters:**
  - `deviceId`: The ID of the device.
  - `orgId`: Current organization ID.
- **Response:**
  - `200 OK`: List of device data models.
    ```json
    [
      {
        "id": 0,
        "name": "string",
        "sourceUnit": "string",
        "unitCategory": 0,
        "unit": "string",
        "manualUnit": "string",
        "value": "string",
        "lastInsert": "2024-04-07T17:27:25.447Z",
        "significant": true, //device may have multiple significant values
        "primary": true, //unique, only one variable per device
        "timerSeconds": 0,
        "deviceName": "string",
        "modelRepositoryVariable": 0,
        "range": {
          "from": 0,
          "to": 0
        }
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Devices for Node

- **Endpoint:** `GET /DevicesForNode`
- **Description:** Endpoint to retrieve devices associated with a specific node.
- **Parameters:**
  - `orgId`: The ID of the organization.
  - `nodeId`: The ID of the node.
  - `technologyId` (Optional): The ID of the technology.
- **Response:**
  - `200 OK`: Devices for node retrieved successfully.
    ```json
    [
      {
        "description": "string",
        "id": 0,
        "name": "string",
        "technologyId": 0,
        "technologyName": "string"
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.
