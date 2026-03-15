# HearthGuard Firmware Changelog

All notable firmware changes are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## Scout

### [0.16.3] - 2026-03-15

#### Fixed
- Captive portal first-load bug (AP stabilization delay)
- Config portal now loads immediately on first connection (HTTP 200 instead of redirect)

#### Added
- WiFi settings in config portal (scan, connect, status)
- MQTT broker auto-discovery in config portal

---

### [0.16.2] - 2026-03-13

#### Changed
- WiFi Signal and Uptime entities now always visible in Home Assistant (no longer require developer mode)

---

### [0.16.1] - 2026-02-27

#### Fixed
- OTA update check no longer triggers an immediate re-check loop after first check
- MQTT reconnect now publishes current sensor state instead of stale defaults

---

### [0.16.0] - 2026-02-27

#### Added
- Multi-sensor presence fusion (radar + PIR + noise + BLE proximity)
- BLE proximity detection feeds into presence
- Ultra sensitivity radar preset for stationary detection
- Raw Radar entity always visible in Home Assistant

#### Changed
- Radar sensitivity improved ~50% for stationary presence detection (breathing/typing)
- Radar unmanned timeout increased to 5s to reduce false absence
- Presence cooldown resets when any input becomes active

#### Fixed
- Ultra sensitivity preset was silently clamped to High

---

### [0.15.1] - 2026-02-27

#### Added
- Instant noise detection with 1-second auto-clearing cooldown
- Noise Alarm entity for sustained noise confirmation
- Developer mode increases sensor publish rate to 500ms
- Noise settings in config portal (threshold, timeout, cooldown)

#### Changed
- Noise detection refactored to dual-output system (instant + alarm)

---

### [0.10.6] - 2026-02-21

#### Fixed
- Tamper detection LED now clears properly when vibration stops
- System LED no longer stays orange after transient MQTT disconnect during boot
- System LED stays solid green during normal operation

---

### [0.10.1] - 2026-02-20

#### Fixed
- Ghost Battery/Battery Voltage entities removed from Home Assistant (conditional discovery)
- OTA URL corrected to public release repository

*First release on the public OTA update repository.*
