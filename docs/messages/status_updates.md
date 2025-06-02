# Message: `status_update`

The `status_update` message is sent periodically by a device to report its current status and telemetry data. This acts as a heartbeat and ensures the controller knows the device is online.

## Fields

| Field         | Type    | Required | Description |
|---------------|---------|----------|-------------|
| `type`        | string  | ✓        | `"status_update"` |
| `uuid`        | string  | ✓        | Unique device identifier (UUID v4) |
| `id`          | string  | ✓        | Human-readable URN |
| `timestamp`   | string  | ✓        | ISO 8601 timestamp |
| `spec_version`| string  | ✓        | ERCS version (e.g. `1.0.0`) |
| `device_name` | string  | ✓        | Friendly name for display purposes |
| `theme`       | string  | ✓        | Puzzle theme (e.g. `Ancient Egypt`) |
| `puzzle_type` | string  | ✓        | Puzzle classification |
| `state`       | string  | ✓        | One of: `idle`, `active`, `solved`, `error`, etc. |
| `capabilities`| array   | ✓        | List of supported features |
| `sensors`     | array   | optional | List of current sensor readings |
| `meta`        | object  | optional | Misc metadata (e.g. uptime, version) |

## Example

See [example-status-update.json](../examples/example-status-update.json)

