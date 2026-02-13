Unsere API liefert Zeitreihendaten in folgendem Format.
Teile deinen Bildschirm und zeige uns wie die TypeScript-Typen dafür aussehen sollen.

```json
{
  "dataset": {
    "id": "ds_abc123",
    "name": "Stromverbrauch Region Nord",
    "created_at": "2024-01-15T10:30:00Z",
    "series": [
      {
        "id": "ts_001",
        "name": "Verbrauch_kWh",
        "frequency": "hourly",
        "points": [
          { "timestamp": "2024-01-01T00:00:00Z", "value": 1234.5 },
          { "timestamp": "2024-01-01T01:00:00Z", "value": 1189.2 }
        ]
      }
    ]
  },
  "forecast": {
    "model": "AutoARIMA",
    "horizon": 48,
    "created_at": "2024-01-15T11:00:00Z",
    "predictions": [
      {
        "timestamp": "2024-01-02T00:00:00Z",
        "value": 1300.1,
        "lower_80": 1150.0,
        "upper_80": 1450.2,
        "lower_95": 1050.0,
        "upper_95": 1550.4
      }
    ]
  }
}
```