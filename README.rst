===============================================================================
pax-devices
===============================================================================

.. image:: https://readthedocs.org/projects/pax-devices/badge/?version=latest
    :target: https://pax-devices.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status

This repository hosts the documentation for `pax-devices` and related ESP-IDF
components.

Devices
===============================================================================

There is a gateway, ESP32 based devices and STM32 + RFM69 based devices.

pax-Gateway
-------------------------------------------------------------------------------

The purpose of this gateway is to either:

* connect a RFM69-based network to Wi-Fi using RFM69HCW and ESP32-WROOM
* connect a LoRa\ |trade| transceiver to Wi-Fi using RFM95/96/97/98(W) and ESP32-WROOM

The gateway was designed for power efficiency without sacrificing functionality.

Devices based on ESP32
-------------------------------------------------------------------------------

**pax-DLED** is an ESP32 controller for digital LEDs. It is designed to support either:

* two rows of WS2812, WS2812B, ... (*aka* NeoPixel) and derivatives like SK6812
* APA102 (*aka* DotStar) and derivatives like SK9822

**pax-DLEDGrid** is designed to use 64 WS2812* DLEDs like a single coloured LED.
It stays in Access Point mode and is controlled through HTTP. The firmware is updated over-the-air.

STM32
-------------------------------------------------------------------------------

* Light, Humidity and Temperature sensor powered by AAA batteries (*built,
  not added yet, to be imported from PAx5 project*).
* Light, Humidity and Temperature sensor powered by Li-Ion / Li-Polymer battery
  charged by a solar panel (*almost built, not added yet, to be imported from
  PAx5 project*).
* Smart relay to control a heating system (*almost build, not added yet, to be
  imported from PAx5 project*).

Development
===============================================================================

See `Development of this documentation <https://pax-devices.readthedocs.io/en/latest/DevDocs/index.html>`_ for actual procedure.

License
===============================================================================

If not mentioned in other ways:

* software and documentation are released under the
  `GNU GPLv3 <http://www.gnu.org/licenses/gpl-3.0.html>`_ License.
  See the `LICENSE-GPLv3.txt <LICENSE-GPLv3.txt>`_ file.
* hardware schematics are licensed under a
  `Creative Commons Attribution-ShareAlike 4.0 International License <http://creativecommons.org/licenses/by-sa/4.0/>`_.
  See the `LICENSE-CC-BY-SA-4.0.txt <LICENSE-CC-BY-SA-4.0.txt>`_ file.

This repository includes the `Read the Docs Sphinx Theme <https://github.com/readthedocs/sphinx_rtd_theme>`_ .
See that link for it's license.

.. |copy|   unicode:: U+000A9 .. COPYRIGHT SIGN
.. |trade|  unicode:: U+02122 .. TRADE MARK SIGN
