# ⬡ Kraken LED Dashboard

A single HTML file that provides a **live pixel preview** for multiple WLED-based LED controllers simultaneously.

**[⬇ Download kraken-dashboard_beta.html](https://github.com/krakenled/Kraken_dashboard/raw/main/kraken-dashboard_beta.html)**

Connect via WebSocket to each controller and see the live LED output in real time — the same data shown in the WLED web UI GFX preview. Designed for event and production use where controllers are mounted out of direct sightlines.

![Kraken LED Dashboard](preview.jpg)

---

## Features

- Live pixel preview for all controllers simultaneously
- Landscape and Portrait orientation modes
- Add / remove devices by IP address and LED count
- Per-device pixel direction reverse
- Auto-reconnect if a controller goes offline
- Persistent device config saved between sessions
- FPS counter, preset number and device name per controller
- Click any IP to open that controller's WLED web UI
- No install required — single HTML file, open in browser

---

## Requirements

- WLED or WLED MoonModules firmware
- WebSockets must be enabled in firmware (do NOT use `-D WLED_DISABLE_WEBSOCKETS`)
- Laptop and all controllers on the same WiFi network
- Google Chrome recommended

---

## Setup

1. Download `kraken-dashboard_beta.html`
2. Connect your laptop to the same WiFi network as your WLED controllers
3. Double-click the file to open it in Chrome
4. Controllers will connect automatically — no server or install required

---

## Adding Devices

1. Click **EDIT DEVICES**
2. Enter IP address, device name and LED count
3. Select Landscape or Portrait orientation
4. Click **+ ADD**

Tick the **Rev** checkbox to flip pixel direction if the preview appears reversed.

---

## Default Configuration

Preconfigured for 8 Kraken LED Bars at `192.168.16.201–208` with 96 LEDs each.
Edit the device list to match your own controller IPs and LED counts.

---

## Troubleshooting

| Issue | Fix |
|---|---|
| All dots red | Check laptop is on the same network as controllers |
| Preview shows black | Rebuild firmware without `-D WLED_DISABLE_WEBSOCKETS` |
| Portrait mode black | Switch to landscape and back — page auto-reloads |
| FPS drops | Enable `WLEDMM_FASTPATH` in firmware build flags |
| Controller offline but LEDs on | Close other browser tabs with WLED web UI open |

---

## Beta

This is a beta release. Tested with WLED MoonModules mdev on ESP32-PICO-D2 (Athom Slimline).
Feedback and bug reports welcome.

---

## Kraken LED

Custom wireless DMX LED bars with onboard audio reactive processing.
Built on WLED MoonModules with E1.31 preset mode DMX control.

[github.com/krakenled](https://github.com/krakenled)
