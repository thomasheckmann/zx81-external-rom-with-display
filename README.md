# zx81-external-rom-with-display
ZX81 External ROM interface with partial display logic. The aim of this interface is to be able to run ZX81 ROMS with alternative character set, as found in different Forth ROMS and the ASZMIC rom, without having the need to open up your ZX81 and replace the internal ROM.

Partial display logic only, as this is what's available at the extension bus.

# version 1.0
Board populated with all components. Works great and can even downgrade your ZX81 to a ZX80 :-)

![IMG_1189](https://github.com/thomasheckmann/zx81-external-rom-with-display/assets/14136378/ac9a7b85-de8f-41bd-a00b-a454568ce17b)

## Planned for v1.1
Only some small changed planned for v1.1 - mostly the NMI generator fix. When running the ZX80 ROM the NMI generator is not turned off, which means the initial state of the generator is unpredictible. For this reason running the ZX80 not always turns out to work, a few on/off should make it work. A simple fix is to make sure the NMI generator is turned off, by using a few resistors.
