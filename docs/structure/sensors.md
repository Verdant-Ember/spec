# Sensors Format

Sensors report physical values or internal telemetry (e.g., temperature, battery level, WiFi signal).

## Format

```json
{
  "name": "battery",
  "type": "percent",
  "value": 87,
  "unit": "%",
  "timestamp": "2025-06-02T15:04:00Z"
}
```

## Common Sensor Types

| Name         | Type    | Unit |
| ------------ | ------- | ---- |
| battery      | percent | %    |
| temperature  | float   | °C   |
| wifi\_signal | dBm     | dBm  |
| rssi         | integer | dBm  |
| humidity     | percent | %    |
| pressure     | float   | hPa  |

