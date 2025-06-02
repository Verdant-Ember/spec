# Message: `event`

The `event` message is used to notify the control system about discrete, meaningful occurrences like a button press, RFID scan, or incorrect entry.

## Fields

| Field        | Type    | Required | Description                                    |
|--------------|---------|----------|------------------------------------------------|
| `type`       | string  | ✓        | `"event"`                                      |
| `uuid`       | string  | ✓        | UUID of device                                 |
| `id`         | string  | ✓        | URN string                                     |
| `timestamp`  | string  | ✓        | ISO 8601 timestamp                             |
| `event_name` | string  | ✓        | Event type (e.g. `rfid_scanned`, `button_pressed`) |
| `data`       | object  | optional | Event-specific data (e.g. scanned tag ID)      |

## Example

```json
{
  "type": "event",
  "uuid": "fd4a6893-9cd2-490a-bf3c-117f2f5a213c",
  "id": "urn:sensor:main_room:button_01",
  "timestamp": "2025-06-02T16:32:00Z",
  "event_name": "button_pressed",
  "data": {
    "button": "green",
    "pressure": 0.82
  }
}

