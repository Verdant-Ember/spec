# Message: `status_update`

The `status_update` message is used to report non-error, non-puzzle state sensor or subsystem values (e.g. current temperature, lighting level, battery, etc.).

## Fields

| Field        | Type    | Required | Description                                  |
|--------------|---------|----------|----------------------------------------------|
| `type`       | string  | ✓        | `"status_update"`                             |
| `uuid`       | string  | ✓        | UUID of the device                            |
| `id`         | string  | ✓        | URN                                           |
| `timestamp`  | string  | ✓        | ISO 8601 time                                 |
| `sensors`    | array   | ✓        | List of sensor readings                       |

### Sensor Object Format

Each item in `sensors[]` is an object:

| Field     | Type    | Required | Description                      |
|-----------|---------|----------|----------------------------------|
| `name`    | string  | ✓        | Sensor name                      |
| `type`    | string  | ✓        | Sensor type (e.g. `temperature`) |
| `unit`    | string  | optional | e.g. `"C"`, `"%"`, `"dBm"`       |
| `value`   | number  | ✓        | Current reading                  |
| `meta`    | object  | optional | Additional details               |

## Example

```json
{
  "type": "status_update",
  "uuid": "2a31f910-587a-4704-9119-b13b04a8d12f",
  "id": "urn:device:lab:envsensor_02",
  "timestamp": "2025-06-02T16:45:00Z",
  "sensors": [
    {
      "name": "temp",
      "type": "temperature",
      "unit": "C",
      "value": 21.7
    },
    {
      "name": "humidity",
      "type": "humidity",
      "unit": "%",
      "value": 58.2
    },
    {
      "name": "wifi",
      "type": "rssi",
      "unit": "dBm",
      "value": -61
    }
  ]
}
