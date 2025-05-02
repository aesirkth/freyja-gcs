freyja ground control station. talks with launchpad controller surtr over lora through brage and to fjaelar over brage.

![overview system diagram](overview_diagram.png)

## goals
- pcb should be able to run standalone from raspberry in case of raspberry malfunction
- every part from lcsc so that pcb can be assembled by jlcpcb. only select parts that have lot in stock. 
- 4-layer pcb. mainly for usb signal integrity

## tools
kicad + the plugin [impartGUI](https://github.com/Steffen-W/Import-LIB-KiCad-Plugin). impartGUI makes it really easy to get symbols and footprints downloaded directly from lcsc.

## TODO PCB
- ESD/TVS diodes on every connecter and button
- Layout
- configure stackup according to jlcpcb specs
- usb 90 ohm diff-z
- valve toggle switches (we need 6 of them)
- 10n cap on every switch for manual debounce, will do in software as well
- lockout switch or key
- initiate countdown button
- 7-segment (or ssd1306 oled?) countdown for redundancy operation without rpi
- abort countdown button
- leds:
  - HOT/READY led indicator
  - led for every valve toggle. should only be activated if surtr confirms position. 
  - connection status with surtr
  - connection status with fjaelar
  - alarm
- eeprom or sd card for saving telemetry
- battery charging circuit
- raspberry pi power
- 2 can ports
  - one for brage 
  - one for connecting directly to 
- buzzer? for alarms
