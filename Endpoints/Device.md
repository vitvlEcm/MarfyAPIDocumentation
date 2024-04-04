# DeviceDashboard

- Returns Dashboard for concrete device
- **method**: _HttpGet_
- **route**: /api/Device/DeviceDashboard/{deviceId}

## Request

- **parameters**:
  - **deviceId**: deviceId (node from tree, where has deviceId)
  - **preset**: use id from api/Stats/PossibleTimeseriesTimes, to use From and To times, set this to -1
  - **from**: datetime from
  - **to**: datetime to

## Response

- _"aggregatedData"_: historical data for timespan specified as preset input parameter

### Example

```Json
[
  {
    "variableName": "string",
    "variableId": 0,
    "aggregatedData": {
      "aggregationId": 0,
      "aggregationName": "string",
      "aggregationDescription": "string",
      "aggregationTypeId": 0,
      "first": {
        "value": "string",
        "abbr": "string",
        "desc": "string"
      },
      "second": {
        "value": "string",
        "abbr": "string",
        "desc": "string"
      },
      "order": 0,
      "elementId": 0,
      "valueSerialized": "string",
      "unit": "string",
      "value": 0,
      "readDateTime": "2024-04-02T07:05:31.970Z"
    },
    "timeseriesData": {
      "name": "string",
      "data": [
        {
          "timestamp": "2024-04-02T07:05:31.970Z",
          "value": 0
        }
      ]
    },
    "data": {
      "id": 0,
      "name": "string",
      "sourceUnit": "string",
      "unitCategory": 0,
      "unit": "string",
      "manualUnit": "string",
      "value": "string",
      "lastInsert": "2024-04-02T07:05:31.970Z",
      "significant": true,
      "primary": true,
      "timerSeconds": 0,
      "deviceName": "string",
      "modelRepositoryVariable": 0,
      "range": {
        "from": 0,
        "to": 0
      },
      "timeseries": {
        "name": "string",
        "data": [
          {
            "timestamp": "2024-04-02T07:05:31.970Z",
            "value": 0
          }
        ]
      }
    }
  }
]
```

# Variables

- Returns all vaviables for a specific device
- **method**: _HttpGet_
- **route**: /api/Device/Variables
- **parameters**:
  - **deviceId**: deviceId (node from tree, where has deviceId)

### Example

```Json
[
  {
    "id": 0,
    "name": "string",
    "sourceUnit": "string",
    "unitCategory": 0,
    "unit": "string",
    "manualUnit": "string",
    "value": "string",
    "lastInsert": "2024-04-03T09:03:29.583Z",
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
```
