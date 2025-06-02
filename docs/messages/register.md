# Message: `register`

The `register` message is sent by a device when it starts up or reconnects. It announces its presence and functional capabilities to the control system.

## Fields

| Field               | Type    | Required | Description                                      |
|---------------------|---------|----------|--------------------------------------------------|
| `type`              | string  | ✓        | `"register"`                                     |
| `uuid`              | string  | ✓        | UUID of the device                               |
| `id`                | string  | ✓        | URN of the device                                |
| `timestamp`         | string  | ✓        | ISO 8601 timestamp                               |
| `theme`             | string  | ✓        | Name of the theme the device belongs to          |
| `firmware`          | string  | optional | Firmware version                                 |
| `capabilities`      | array   | ✓        | List of capability strings                       |
| `capability_metadata` | object | optional | Attributes related to the capabilities           |
| `metadata`          | object  | optional | Any other identifying or custom info             |

## Example

```json
{
  "type": "register",
  "uuid": "1e9080ec-0eb0-49a6-bd94-54f03a49234a",
  "id": "urn:puzzle:egyptian:ankh_dial",
  "timestamp": "2025-06-02T17:02:00Z",
  "theme": "Ancient Egypt",
  "firmware": "v0.9.3",
  "capabilities": [
    "sensor.rfid",
    "puzzle.pattern_match"
  ],
  "capability_metadata": {
    "sensor.rfid": {
      "antenna": "circular",
      "range_cm": 8
    },
    "puzzle.pattern_match": {
      "pattern_slots": 4
    }
  },
  "metadata": {
    "location": "Main Chamber",
    "manufacturer": "RoomTech",
    "board": "ESP32"
  }
}

