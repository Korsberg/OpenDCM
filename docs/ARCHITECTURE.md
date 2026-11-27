# Architecture

Planned layout of `OpenDCM/` (SwiftUI, MVVM):

| Folder | Content |
|---|---|
| `App/` | App entry point and navigation |
| `Core/HA/` | REST and WebSocket client, entity models |
| `Core/Store/` | Settings and keychain |
| `Features/Flow/` | Flow diagram |
| `Features/History/` | Swift Charts views |
| `Features/Menus/` | Pump menu views |
| `Features/Alarms/` | Alarm views |
| `Resources/` | Own graphics, localisation |
| `Config/` | Example configuration |

The app is read-only: no code path may write to the pump or call Home Assistant services that change it.
