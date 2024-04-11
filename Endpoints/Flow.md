# Settings

- **Route:** `{server}/api/Flows`

## `Get` Get Flows

- **Endpoint:** `GET /`
- **Description:** Endpoint to retrieve all possible flows.
- **Response:**
  - `200 OK`: Timeseries data.
    ```json
    [
      {
        "id": 0,
        "name": "string",
        "description": "string",
        "iconUrl": "string",
        "iconLastUpdate": "2024-04-11T10:46:15.315Z"
      }
    ]
    ```
