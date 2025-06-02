# Message: `config`

The `config` message is sent when the device starts up or reconnects. It declares the device’s identity, theme, capabilities, and metadata.

## Fields

| Field         | Type    | Required | Description |
|---------------|---------|----------|-------------|
| `type`        | string  | ✓        | `"config"` |
| `uuid`        | string  | ✓        | UUID v4 for the device |
| `id`          | string  | ✓        | Human-readable URN |
| `timestamp`   | string  | ✓        | ISO 8601 UTC timestamp |
| `spec_version`| string  | ✓        | Version of ERCS this device follows |
| `device_name` | string  | ✓        | Friendly name of the device |
| `theme`       | string  | ✓        | Theme context for puzzle |
| `puzzle_type` | string  | ✓        | Puzzle classification |
| `capabilities`| array   | ✓        | Supported hardware features |
| `meta`        | object  | optional | Arbitrary metadata like firmware version |

## Use Case

- Sent on startup or reconnection
- Helps the control software dynamically map and assign roles

