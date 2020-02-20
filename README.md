# pax-devices

This is the repository that hosts the documentation for Calin Radoni's smart devices.

## Short description

Some devices can also work standalone (`Dev33-DLED`, `Dev34-DLED`), others (`Dev41-LHTSensor`) need a gateway (`Dev12-GW`) for integration in a Smart Home system.

- **Dev12-GW** is a gateway with ESP32 and RFM69 or RFM95 LoRa transceiver.
- **Dev33-DLED** is an ESP32 controller for digital LEDs. It is designed to support either:
  - two rows of WS2812, WS2812B, ... (*aka* NeoPixel) and derivatives like SK6812
  - APA102 (*aka* DotStar) and derivatives like SK9822
- **Dev34-DLEDGrid** is designed to use 64 WS2812* DLEDs like a single coloured LED.
- **Dev41-LHTSensor** (*built, not added yet, to be imported from PAx5 project*) is a sensor for Light, Humidity and Temperature.
- **Dev42-Relay** (*almost build, not added yet, to be imported from PAx5 project*) is a smart relay to control a heating system.

## Development

See the `Docs/Development.md` document.

## License

If not mentioned in other ways:

- software and documentation are released under the [GNU GPLv3](http://www.gnu.org/licenses/gpl-3.0.html) License. See the __LICENSE-GPLv3.txt__ file.
- hardware schematics are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
See the __LICENSE-CC-BY-SA-4.0.txt__ file.
