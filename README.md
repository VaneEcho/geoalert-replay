# JamScope

JamScope is a lightweight web tool for replaying time-based alert events on a map timeline.

The system loads Excel files containing geographic coordinates and alert timestamps, then replays them on an OpenStreetMap map. This allows users to observe how interference events appear, persist, and disappear over time.

It is particularly useful for analyzing spatial-temporal patterns such as GNSS interference, RF anomalies, or other location-based alerts.

---

## Features

- Excel data upload
- Automatic field detection (Chinese / English headers)
- Timeline replay of events
- Adjustable playback speed
- Active alert visualization on map
- OpenStreetMap rendering

---

## Expected Excel Format

The Excel file should contain fields similar to:

| City | Longitude | Latitude | Start Time | End Time |
|-----|-----|-----|-----|-----|

Chinese headers are also supported:

| 地市 | 经度 | 纬度 | 告警发生时间 | 告警消除时间 |

Additional optional fields:

- 持续时间(秒)
- 持续时间排序编号

---

## How It Works

1. Upload an Excel file containing alert data.
2. The system parses geographic coordinates and timestamps.
3. Alerts are replayed on the map according to their active time window.
4. The map displays only alerts that are active at the current moment.

A polyline is drawn between active points to help visualize possible movement patterns of interference sources.

---

## Use Cases

- GNSS interference monitoring
- RF anomaly analysis
- Geographic alert visualization
- Spatiotemporal data replay

---

## Map Data

Map tiles are provided by **OpenStreetMap**.

OpenStreetMap attribution is preserved as required by the license.

---

## License

Apache License 2.0
