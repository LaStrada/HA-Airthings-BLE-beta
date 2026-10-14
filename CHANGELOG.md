# Changelog

Every release of the Airthings BLE HACS beta, newest first.

## 1.3.0b3 (2026-10-14)

#### airthings-ble
- Updated to 1.3.1 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.1)): accepts cbor2 5.9 and newer instead of requiring 6.1.5, so it installs alongside integrations that need cbor2 5.x (for example Snoo)
- Wave Enhance and Corentium Home 2 responses decode with every supported cbor2 version, and a malformed response is skipped instead of failing the whole update

#### Home Assistant integration (core)
- Unchanged since 1.3.0b2 (home-assistant/core `dev` [`0152f6d9aae4`](https://github.com/home-assistant/core/tree/0152f6d9aae446db6aee94ca229c48f94efd4353/homeassistant/components/airthings_ble), with `__init__.py` kept compatible with Home Assistant 2026.10)

## 1.3.0b2 (2026-10-14)

#### airthings-ble
- Updated to 1.3.0 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.0)): the same code as 1.3.0rc1 in 1.3.0b1, now as a final release

#### Home Assistant integration (core)
- A sensor without a value in the latest reading shows as unknown instead of unavailable
- From home-assistant/core `dev` [`0152f6d9aae4`](https://github.com/home-assistant/core/tree/0152f6d9aae446db6aee94ca229c48f94efd4353/homeassistant/components/airthings_ble), with `__init__.py` kept compatible with Home Assistant 2026.10

## 1.3.0b1 (2026-10-10)

- No more dropped ESPHome Bluetooth proxy connections when a device disconnects
- Wave Enhance and Corentium Home 2 work through proxies with a small MTU (fragmented responses)
- Temperatures below 0 °C are reported correctly
- Wave Mini no longer reports 1310.7 hPa / 100 % light right after power-up
- Steadier connections: shorter command timeout, notifications always stopped
- airthings-ble 1.3.0rc1 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.0rc1))
- Integration from home-assistant/core `dev` [`94122d5a95b0`](https://github.com/home-assistant/core/tree/94122d5a95b094855e99377518a2cd9102418cba/homeassistant/components/airthings_ble)
