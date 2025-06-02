# Message: `command`

A `command` message is sent by the controller to instruct a device to perform an action: turn on lights, reset itself, play a sound, etc.

## Fields

| Field          | Type    | Required | Description                                   |
|----------------|---------|----------|-----------------------------------------------|
| `type`         | string  | ✓        | `"command"`                                   |
| `uuid`         | string  | ✓        | UUID of the target device                     |
| `id`           | string  | ✓        | URN of target device                          |
| `timestamp`    | string  | ✓        | When the command was sent (ISO 8601)          |
| `command_name` | string  | ✓        | Command (e.g. `reset`, `play_sound`)          |
| `params`       | object  | optional | Parameters relevant to the command            |

## Example

```json
{
  "type": "command",
  "uuid": "a1b2c3d4-e5f6-47a9-82ab-33813f79082e",
  "id": "urn:puzzle:lab:audio_unit",
  "timestamp": "2025-06-02T16:35:00Z",
  "command_name": "play_sound",
  "params": {
    "clip": "victory",
    "volume": 0.8
  }
}

