# Detail

- returns technology details for concrete technology

- **parameters**:

  - _orgId:_ Current organization ID
  - _nodeId:_ Current nodeID
  - _technologyId:_ technology from _/api/Technology/List_
  - _preset:_ use id from api/Stats/PossibleTimeseriesTimes, to use From and To times, set this to -1
  - _from:_ datetime from
  - _to:_ datetime to

- _response_

```Json
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

# TechnologiesForNode

- _/api/Technology/TechnologiesForNode_
- Returns all technologies in children nodes
- **parameters**:
  - _orgId:_ Current organization ID
  - _nodeId:_ Current nodeID

# List

- _/api/Technology/List_
- returns all possible technologies

```Json
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
