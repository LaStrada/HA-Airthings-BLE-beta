# Changelog

Every release of the Airthings BLE HACS beta, newest first.

## 1.3.0b2 (2026-10-14)

- airthings-ble 1.3.0 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.0)), the same code as 1.3.0rc1
- A sensor without a value in the latest reading shows as unknown instead of unavailable
- Integration from home-assistant/core `dev` [`0152f6d9aae4`](https://github.com/home-assistant/core/tree/0152f6d9aae446db6aee94ca229c48f94efd4353/homeassistant/components/airthings_ble), with `__init__.py` kept compatible with Home Assistant 2026.10

## 1.3.0b1 (2026-10-10)

- No more dropped ESPHome Bluetooth proxy connections when a device disconnects
- Wave Enhance and Corentium Home 2 work through proxies with a small MTU (fragmented responses)
- Temperatures below 0 °C are reported correctly
- Wave Mini no longer reports 1310.7 hPa / 100 % light right after power-up
- Steadier connections: shorter command timeout, notifications always stopped
- airthings-ble 1.3.0rc1 ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.0rc1))
- Integration from home-assistant/core `dev` [`94122d5a95b0`](https://github.com/home-assistant/core/tree/94122d5a95b094855e99377518a2cd9102418cba/homeassistant/components/airthings_ble)
