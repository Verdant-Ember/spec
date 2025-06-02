# Naming Convention

Devices are identified with a structured URN string.

## Format

```
urn:{role}:{location}:{name}
```

## Examples

- `urn:puzzle:main_room:torch_01`
- `urn:controller:core:main_hub`
- `urn:sensor:lobby:temp_01`

## Roles

| Role        | Description |
|-------------|-------------|
| `puzzle`    | Puzzle logic or controller |
| `sensor`    | Telemetry-only device |
| `controller`| Main game controller |
