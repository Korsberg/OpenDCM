# OpenDCM

An open-source, **read-only** iPhone and iPad app for Thermia iTec heat pumps, built with SwiftUI. It shows live data from your own Home Assistant: a flow diagram, history charts and the pump's menus.

OpenDCM is **not affiliated with, endorsed by or connected to Thermia**. It does not use Thermia's name, graphics or cloud service.

## How it works

```
Thermia iTec  --RS485-->  ESP32 (ESPHome)  --API-->  Home Assistant  --REST/WebSocket-->  OpenDCM
```

The app never talks to the pump. It only reads entities from Home Assistant. The firmware that exposes the pump data is a separate project: [thermia-itec-dcm-esphome](https://github.com/Korsberg/thermia-itec-dcm-esphome).

## Status

Early development. Read-only. See [docs/ROADMAP.md](docs/ROADMAP.md).

## Requirements

- Home Assistant with the Thermia iTec entities (see [docs/HOME_ASSISTANT.md](docs/HOME_ASSISTANT.md))
- A Mac with Xcode 17 or later (iOS 18 or later target)
- An Apple ID (a free account works, but needs re-signing every 7 days)

## Build

1. Clone the repo and open the Xcode project in `OpenDCM/`.
2. Copy `OpenDCM/Config/Secrets.example.plist` to `Secrets.plist` (it is git-ignored) and fill in your own Home Assistant address and token, or enter them in the app's settings.
3. Select your device and run.

No address, token or entity id is built into the app.

## Privacy

Everything stays between your phone and your Home Assistant. No analytics, no third-party servers.

## License

MIT, see [LICENSE](LICENSE).
