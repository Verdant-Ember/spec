# Message Structure

This document outlines the common fields that appear in all ERCS messages.

## Required Fields

| Field         | Type   | Description |
|---------------|--------|-------------|
| `type`        | string | Type of message |
| `uuid`        | string | Unique device ID (UUID v4) |
| `id`          | string | Human-readable URN |
| `timestamp`   | string | ISO 8601 timestamp |
| `spec_version`| string | Version of the protocol |
| `device_name` | string | Friendly name for display |
| `theme`       | string | Puzzle theme context |
| `puzzle_type` | string | Type of puzzle (e.g. memory, lock, sensor) |
| `state`       | string | Current device state |
| `capabilities`| array  | List of device functions |

## Optional Fields

- `sensors[]`: Array of current sensor readings
- `meta`: Extra metadata (firmware, uptime, etc.)

