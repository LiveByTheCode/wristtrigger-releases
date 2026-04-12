# WristTrigger

Trigger Tasker tasks from your Amazfit watch.

WristTrigger lets you configure buttons on your Amazfit smartwatch that fire Tasker tasks on your Android phone. Tap a button on your wrist, and your phone does the rest.

## How it works

```
Watch button tap → BLE → Zepp app (side service) → HTTP localhost → WristTrigger app → Tasker broadcast
```

Two components work together:
- **Android companion app** — runs a local HTTP server, manages button config, dispatches Tasker intents
- **Zepp OS watch app** — shows a button grid on your watch, communicates with the phone via Zepp's BLE bridge

## Requirements

- Amazfit watch running Zepp OS 3.0+ (e.g., Amazfit Active 2)
- Zepp app installed and paired with the watch
- [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) installed with "Allow External Access" enabled
- Android 9.0+ (API 28)

## Download

### Android App
Download the latest APK from [Releases](https://github.com/LiveByTheCode/wristtrigger-releases/releases).

### Watch App
The watch app will be available on the Zepp App Store. For now, sideload via Developer Mode — see setup guide below.

## Setup

1. Install the Android APK and open WristTrigger
2. Tap **Start** to launch the bridge server
3. Configure your buttons — set a label and Tasker task name for each
4. Tap **Test** to verify each button fires the correct Tasker task
5. Install the watch app (Zepp App Store or sideload)
6. Open the watch app — your buttons will appear automatically
7. Tap a button on the watch to trigger the mapped Tasker task

## Tasker Configuration

1. Open Tasker → **Preferences** → **Misc**
2. Enable **Allow External Access**
3. When prompted, grant WristTrigger permission to trigger tasks
4. Create tasks in Tasker that you want to trigger from the watch
5. Use the exact task name (case-sensitive) in WristTrigger's button config

## Features

- 1–8 configurable buttons with custom labels and colors
- Tap-to-trigger with feedback (Sent / Failed / Phone unreachable)
- Foreground service survives app close, optional start-on-boot
- Config export/import (JSON backup)
- Recent activity log for debugging
- No internet access — everything runs over local Bluetooth + loopback

## License

MIT
