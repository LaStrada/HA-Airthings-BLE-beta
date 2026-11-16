# Airthings BLE beta for Home Assistant

A beta of the built-in [Airthings BLE](https://www.home-assistant.io/integrations/airthings_ble/) integration, for testing a new [airthings-ble](https://github.com/Airthings/airthings-ble) release and the latest integration code before they reach a Home Assistant release.

## Current beta

- Version: **1.4.1b1**
- airthings-ble: **1.4.1rc1** ([release notes](https://github.com/Airthings/airthings-ble/releases/tag/1.4.1rc1))
- Integration code: home-assistant/core `dev` at [`d22efd4d8506`](https://github.com/home-assistant/core/tree/d22efd4d8506e6264b79ee903aceb11c82f1ab88/homeassistant/components/airthings_ble)
- Requires Home Assistant **2026.11.0** or newer

What to test in this beta:

- Discovery no longer connects to nearby Airthings devices; the device is identified from its Bluetooth advertisement, and only confirming the setup connects to it
- Devices the advertisement does not identify as supported (for example View devices) are no longer offered for setup and are not connected to
- A failed connection when confirming a discovered device shows an error and can be retried instead of aborting the setup
- A repair issue tells you when a device is connected to an Airthings hub (SmartLink) or has no connectivity configured, so it cannot be read over Bluetooth
- New radon 7-day, 30-day and 1-year average sensors for Corentium Home 2
- Duplicate devices left behind by incomplete reads are removed
- Requires Home Assistant 2026.11.0 or newer

All releases: [CHANGELOG.md](CHANGELOG.md).

## Install

1. In HACS, open the menu, select **Custom repositories**, add `https://github.com/LaStrada/HA-Airthings-BLE-beta` with type **Integration**.
2. Install **Airthings BLE (beta)** and restart Home Assistant.

The beta replaces the built-in integration and uses the same domain, so existing devices and entities are kept.

## Go back to the built-in integration

Remove the repository in HACS, make sure `custom_components/airthings_ble` is gone, and restart Home Assistant. Devices and entities are kept.

## Report a problem

Open an issue in [LaStrada/HA-Airthings-BLE-beta](https://github.com/LaStrada/HA-Airthings-BLE-beta/issues) with the beta version and a debug log (`custom_components.airthings_ble` and `airthings_ble` at debug level).
