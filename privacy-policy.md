# WristTrigger Privacy Policy

**Last updated:** April 13, 2026

## Overview

WristTrigger is a utility app that triggers Tasker tasks on your Android phone from your Amazfit watch. Your privacy is important to us.

## Data Collection

WristTrigger does **not** collect, store, or transmit any personal data.

## Network Access

WristTrigger does **not** access the internet. All communication occurs locally on your device:
- The app runs a local HTTP server on `127.0.0.1` (localhost) that only accepts connections from the same device.
- Watch commands are received over Bluetooth via the Zepp app and forwarded to this local server.

No data is sent to external servers, cloud services, or third parties.

## Data Storage

Button configuration (labels, colors, and Tasker task names) is stored locally on your device using Android DataStore. This data never leaves your device.

## Analytics & Tracking

WristTrigger contains no analytics, tracking, advertising, or telemetry of any kind.

## Third-Party Services

WristTrigger interacts with:
- **Tasker** — sends broadcast intents to trigger tasks you have configured. No data is shared beyond the task name.
- **Zepp app** — receives button tap commands from your watch over Bluetooth. No data is shared with Zepp Health.

## Changes to This Policy

If we update this policy, the changes will be posted on this page with an updated date.

## Contact

If you have questions about this privacy policy, please open an issue at [github.com/LiveByTheCode/wristtrigger-releases](https://github.com/LiveByTheCode/wristtrigger-releases/issues).
