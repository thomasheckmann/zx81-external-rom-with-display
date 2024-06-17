# zx81-external-rom-with-display
ZX81 External ROM interface with partial display logic. The aim of this interface is to be able to run ZX81 ROMS with alternative character set, as found in different Forth ROMS and the ASZMIC rom, without having the need to open up your ZX81 and replace the internal ROM.

Partial display logic only, as this is what's available at the extension bus.

# version 1.0
Board populated with all components. Works great and can even downgrade your ZX81 to a ZX80 :-)

![IMG_1189](https://github.com/thomasheckmann/zx81-external-rom-with-display/assets/14136378/ac9a7b85-de8f-41bd-a00b-a454568ce17b)

With this interface it is now possible to run ROMs such as the ZX.ASZMIC, Skyware Forth and even the ZX80 ROM.

PLEASE NOTE: The display with this interface will make the ZX81 run as in FAST mode, since there is for now no way to implement the SLOW mode display externally. And one of the main goal is to avoid modifying your existing ZX81.

BOM for v1.0:
- [ ] M28C64 EEPROM (8K eeprom)
- [ ] 74LS157 x 3
- [ ] 74LS193
- [ ] 74LS374
- [ ] Diode 1N4148 x 3
- [ ] Resistor 10K
- [ ] 100nF Ceramic Capacitor x 6

## Planned for v1.1
Only some small changes are planned for v1.1 - mostly the NMI generator fix. When running the ZX80 ROM the NMI generator is not turned off, which means the initial state of the generator is unpredictible. For this reason running the ZX80 not always turns out to work, a few on/off should make it work. A simple fix is to make sure the NMI generator is turned off, by using a few resistors.

Will change the diode from 1N4148 to BAT85, as recommended for this type of usage.

Replace IC socket with ZIF Test socket, as it turns out that I'm swapping out EEPROMs based on needs and usage.
