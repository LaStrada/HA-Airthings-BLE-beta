# Airthings BLE beta for Home Assistant

A beta of the built-in [Airthings BLE](https://www.home-assistant.io/integrations/airthings_ble/) integration, for testing a new [airthings-ble](https://github.com/Airthings/airthings-ble) release and the latest integration code before they reach a Home Assistant release.

## Current beta

- Version: **1.3.0b3**
- airthings-ble: **1.3.1** ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.3.1))
- Integration code: home-assistant/core `dev` at [`94122d5a95b0`](https://github.com/home-assistant/core/tree/94122d5a95b094855e99377518a2cd9102418cba/homeassistant/components/airthings_ble)
- Requires Home Assistant **2026.10.0** or newer

What to test in this beta:

- No more dropped ESPHome Bluetooth proxy connections when a device disconnects
- Wave Enhance and Corentium Home 2 work through proxies with a small MTU (fragmented responses)
- Temperatures below 0 °C are reported correctly
- Wave Mini no longer reports 1310.7 hPa / 100 % light right after power-up
- Steadier connections: shorter command timeout, notifications always stopped

All releases: [CHANGELOG.md](CHANGELOG.md).

## Install

1. In HACS, open the menu, select **Custom repositories**, add `https://github.com/LaStrada/HA-Airthings-BLE-beta` with type **Integration**.
2. Install **Airthings BLE (beta)** and restart Home Assistant.

The beta replaces the built-in integration and uses the same domain, so existing devices and entities are kept.

## Go back to the built-in integration

Remove the repository in HACS, make sure `custom_components/airthings_ble` is gone, and restart Home Assistant. Devices and entities are kept.

## Report a problem

Open an issue in [LaStrada/HA-Airthings-BLE-beta](https://github.com/LaStrada/HA-Airthings-BLE-beta/issues) with the beta version and a debug log (`custom_components.airthings_ble` and `airthings_ble` at debug level).
