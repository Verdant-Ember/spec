# Message: `error`

The `error` message is sent when a device or subsystem encounters an error. This can help with diagnostics and debugging.

## Fields

| Field        | Type    | Required | Description                                  |
|--------------|---------|----------|----------------------------------------------|
| `type`       | string  | ✓        | `"error"`                                     |
| `uuid`       | string  | ✓        | UUID of the device reporting the error        |
| `id`         | string  | ✓        | URN of device                                 |
| `timestamp`  | string  | ✓        | ISO 8601 timestamp                            |
| `error_code` | string  | ✓        | Unique error identifier or code               |
| `message`    | string  | optional | Human-readable message                        |
| `details`    | object  | optional | Arbitrary diagnostic data                     |

## Example

```json
{
  "type": "error",
  "uuid": "fa76d1d4-3e3a-4131-857a-ec9f6c783bc0",
  "id": "urn:sensor:control_room:temp_01",
  "timestamp": "2025-06-02T16:40:00Z",
  "error_code": "TEMP_SENSOR_FAIL",
  "message": "Temperature sensor disconnected",
  "details": {
    "last_value": 22.5,
    "uptime": 8123
  }
}

