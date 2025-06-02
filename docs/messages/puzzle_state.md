# Message: `puzzle_state`

The `puzzle_state` message is used to update the control software on the current internal state of the puzzle — e.g. when the player makes progress or regresses.

## Fields

| Field       | Type    | Required | Description                                    |
|-------------|---------|----------|------------------------------------------------|
| `type`      | string  | ✓        | `"puzzle_state"`                               |
| `uuid`      | string  | ✓        | UUID of the device                             |
| `id`        | string  | ✓        | Human-readable URN                             |
| `timestamp` | string  | ✓        | ISO 8601 timestamp                             |
| `state`     | string  | ✓        | Puzzle state: `idle`, `in_progress`, `solved`, `failed`, etc. |
| `progress`  | number  | optional | Progress percentage (0–100)                    |
| `details`   | object  | optional | Arbitrary details (e.g. stage, hint_used)      |

## Example

```json
{
  "type": "puzzle_state",
  "uuid": "e1d7e840-a102-4b2c-a6e7-2fd8047a508a",
  "id": "urn:puzzle:office:keypad_01",
  "timestamp": "2025-06-02T16:25:00Z",
  "state": "in_progress",
  "progress": 40,
  "details": {
    "stage": "first_code",
    "hint_used": false,
    "attempts": 2
  }
}

