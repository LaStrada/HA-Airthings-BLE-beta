# Changelog

Every release of the Airthings BLE HACS beta, newest first.

## 1.4.1b1 (2026-11-16)

- Discovery no longer connects to nearby Airthings devices; the device is identified from its Bluetooth advertisement, and only confirming the setup connects to it
- Devices the advertisement does not identify as supported (for example View devices) are no longer offered for setup and are not connected to
- A failed connection when confirming a discovered device shows an error and can be retried instead of aborting the setup
- A repair issue tells you when a device is connected to an Airthings hub (SmartLink) or has no connectivity configured, so it cannot be read over Bluetooth
- New radon 7-day, 30-day and 1-year average sensors for Corentium Home 2
- Duplicate devices left behind by incomplete reads are removed
- Requires Home Assistant 2026.11.0 or newer
- airthings-ble 1.4.1rc1 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.4.1rc1))
- Integration from home-assistant/core `dev` [`d22efd4d8506`](https://github.com/home-assistant/core/tree/d22efd4d8506e6264b79ee903aceb11c82f1ab88/homeassistant/components/airthings_ble); changes since the previous beta: [commits](https://github.com/home-assistant/core/compare/0152f6d9aae446db6aee94ca229c48f94efd4353...d22efd4d8506e6264b79ee903aceb11c82f1ab88)
- Plus changes that are not in home-assistant/core `dev` yet

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
