# Message: `deregister`

The `deregister` message is sent by a device before shutting down or rebooting intentionally, allowing the control system to update its status cleanly.

## Fields

| Field       | Type    | Required | Description                          |
|-------------|---------|----------|--------------------------------------|
| `type`      | string  | ✓        | `"deregister"`                        |
| `uuid`      | string  | ✓        | UUID of the device                    |
| `id`        | string  | ✓        | URN                                   |
| `timestamp` | string  | ✓        | ISO 8601 timestamp                    |
| `reason`    | string  | optional | Reason for shutdown/reboot           |

## Example

```json
{
  "type": "deregister",
  "uuid": "acbbd0ee-28cb-42fa-a4d1-8efabf3bcddd",
  "id": "urn:device:office:lightstrip01",
  "timestamp": "2025-06-02T17:05:00Z",
  "reason": "rebooting for firmware update"
}
