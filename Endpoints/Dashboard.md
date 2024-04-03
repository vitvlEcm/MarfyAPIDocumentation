# Dashboard

- returns dashboard data
- **route**: /api/Dashboard
- **parameters**:
  - nodeId: NodeId from tree
  - orgId: Current organization ID

## Response

### Description

- 2 objects

  - **significant values**:

    - collection
    - for boxes with values
    - Grouped to types
    - "values/size": 1 for small box, 2 for wide box

    - example:

    ```json
    "significantValues": [
      {
        "name": "Elektřina",
        "description": "",
        "technology": 12,
        "values": [
          {
            "id": 0,
            "name": "Výroba el.",
            "desctription": "",
            "value": "18",
            "unit": "Kw",
            "size": 2,
            "dateTime": "2024-03-27T16:47:07.241Z"
          },
          {
            "id": 0,
            "name": "Spotřeba el.",
            "desctription": "",
            "value": "32",
            "unit": "Kw",
            "size": 1,
            "dateTime": "2024-03-27T16:47:07.241Z"
          },
          {
            "id": 0,
            "name": "Frekvence",
            "desctription": "",
            "value": "50",
            "unit": "Hz",
            "size": 1,
            "dateTime": "2024-03-27T16:47:07.241Z"
          },
        ]
      },
    ],
    ```

  - **technologies**

### Example:

```Json
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

![Dashboard](../Images/Dashboard.png)
