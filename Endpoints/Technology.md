# Technology

## `Get` Technology Details

- **Endpoint:** `GET /Detail`
- **Description:** Endpoint to retrieve technology details for a specific technology.
- **Parameters:**
  - `orgId`: The ID of the organization.
  - `nodeId`: The ID of the node.
  - `technologyId`: The ID of the technology.
  - `Preset`: Use ID from `api/Stats/PossibleTimeseriesTimes`. To use `From` and `To` times, set this to -1.
  - `From`: Start DateTime.
  - `To`: End DateTime.
- **Response:**
  - `200 OK`: Technology details retrieved successfully.
    ```json
    [
      {
        "name": "string",
        "id": 0,
        "typeId": 0,
        "typeName": "string",
        "description": "string",
        "data": [
          {
            "id": 0,
            "name": "string",
            "sourceUnit": "string",
            "unitCategory": 0,
            "unit": "string",
            "manualUnit": "string",
            "value": "string",
            "lastInsert": "2024-04-03T09:55:49.098Z",
            "significant": true,
            "primary": true,
            "timerSeconds": 0,
            "deviceName": "string",
            "modelRepositoryVariable": 0,
            "range": {
              "from": 0,
              "to": 0
            }
          }
        ]
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Technologies for Node

- **Endpoint:** `GET /TechnologiesForNode`
- **Description:** Endpoint to retrieve all technologies in children nodes.
- **Parameters:**
  - `orgId`: The ID of the organization.
  - `nodeId`: The ID of the node.
- **Response:**
  - `200 OK`: Technologies for node retrieved successfully.
    ```json
    [
      {
        "id": 0,
        "name": "string",
        "description": "string",
        "iconUrl": "string",
        "iconLastUpdate": "2024-04-03T09:56:34.517Z"
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.

## `Get` Technologies List

- **Endpoint:** `GET /List`
- **Description:** Endpoint to retrieve all possible technologies.
- **Parameters:** None
- **Response:**
  - `200 OK`: List of technologies retrieved successfully.
    ```json
    [
      {
        "Id": 0,
        "Name": "string",
        "Description": "string",
        "IconUrl": "string",
        "IconLastUpdate": "string"
      }
    ]
    ```
  - `401 Unauthorized`: User not authorized to perform this action.
