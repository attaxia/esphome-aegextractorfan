# AEG Extractor Fan IR Controller

Control an AEG extractor fan via infrared using an M5Stack Atom Lite using its built-in infrared transmitter, running ESPHome.

## Hardware

- [M5Stack Atom Lite](https://shop.m5stack.com/products/atom-lite-esp32-development-kit)


## Features

- **Toggle power** – Turn the fan on/off
- **Toggle light** – Turn the built-in light on/off
- **Increase speed** – Increase fan speed
- **Decrease speed** – Decrease fan speed
- **Physical button** – The Atom's built-in button toggles the light for testing

## Installation

1. Install [ESPHome](https://esphome.io/guides/installing_esphome.html)
2. Copy `extractorfan.yaml` to your ESPHome config directory
3. Create a `secrets.yaml` file with your WiFi credentials:
   ```yaml
   wifi_ssid: "your_ssid"
   wifi_password: "your_password"
   ```
4. Flash the device:
   ```bash
   esphome run extractorfan.yaml
   ```

## Home Assistant Integration

The device will auto-discover in Home Assistant. Four buttons will appear:

- `button.extractorfan_toggle_power`
- `button.extractorfan_toggle_light`
- `button.extractorfan_increase_speed`
- `button.extractorfan_decrease_speed`


## IR Codes

Codes were captured using `remote_receiver` with `dump: all` and are in Pronto format.

## Notes

- The IR Unit has limited range (~1-2m). Position it with line-of-sight to the fan's IR receiver.
- For longer range, consider a transistor-driven IR LED circuit or an external IR blaster.
