# Message: `ack`

Acknowledgement message used to confirm receipt of a message, usually a `command`.

## Fields

| Field        | Type    | Required | Description                              |
|--------------|---------|----------|------------------------------------------|
| `type`       | string  | ✓        | `"ack"`                                   |
| `uuid`       | string  | ✓        | UUID of responding device                |
| `id`         | string  | ✓        | URN of device                            |
| `timestamp`  | string  | ✓        | When the ack was sent (ISO 8601)         |
| `message_id` | string  | optional | Original message ID, if available        |
| `status`     | string  | optional | `ok`, `received`, `queued`, `executed`   |

## Example

```json
{
  "type": "ack",
  "uuid": "ab12cd34-5678-4ef0-9a09-1234567890ab",
  "id": "urn:puzzle:main_room:light_controller",
  "timestamp": "2025-06-02T16:36:12Z",
  "message_id": "msg-3421",
  "status": "executed"
}
