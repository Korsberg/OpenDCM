# Home Assistant

OpenDCM reads entities that the ESPHome firmware in
[thermia-itec-dcm-esphome](https://github.com/Korsberg/thermia-itec-dcm-esphome) publishes.

- Connection: REST and WebSocket, with a long-lived access token created in your own Home Assistant profile.
- Entity mapping: the app lets you pick the entities in settings. Nothing is hard-coded.
- Keep the token out of the repo. It belongs in the device keychain or in the git-ignored `Secrets.plist`.
