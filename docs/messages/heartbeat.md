# Message: `heartbeat`

Devices send `heartbeat` messages periodically to indicate they are online and operational.

## Fields

| Field        | Type    | Required | Description                                 |
|--------------|---------|----------|---------------------------------------------|
| `type`       | string  | ✓        | `"heartbeat"`                                |
| `uuid`       | string  | ✓        | UUID of the device                           |
| `id`         | string  | ✓        | URN of the device                            |
| `timestamp`  | string  | ✓        | When the heartbeat was sent (ISO 8601)       |
| `uptime`     | number  | optional | Seconds since boot                           |
| `firmware`   | string  | optional | Firmware version                             |
| `ip`         | string  | optional | IP address                                   |
| `rssi`       | number  | optional | WiFi signal strength (RSSI)                  |
| `metadata`   | object  | optional | Additional fields                            |

## Example

```json
{
  "type": "heartbeat",
  "uuid": "c2eab712-7e44-4d3d-9511-98a450cd9d0b",
  "id": "urn:device:office:rfid_01",
  "timestamp": "2025-06-02T16:42:10Z",
  "uptime": 4551,
  "firmware": "v1.2.0",
  "ip": "192.168.0.42",
  "rssi": -66,
  "metadata": {
    "battery": 94,
    "temperature": 23.1
  }
}
