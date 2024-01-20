# IBM EGA Card Reference Layout

The EGA card (Enhanced Graphics Adapter) was IBM's followup to the original two graphics cards, the MDA and the CGA cards, that came out with the 5150 PC. While retaining backwards compatibility, it added several new graphics modes supporting up to 640x350 graphics at up to 16 colors from a palette of 64.

Unlike the previous cards which used only off-the-shelf logic chips, the EGA used four different custom gate array chips developed by IBM. The chips added some advanced functionality including bit plane math. The same functionality was later supported and extended somewhat by the VGA standard, which clever programmers used to speed up bitblt operations and to create nonstandard video modes (such as Mode X). Unfortunately, this also makes cloning the card a bit too challenging, although several companies including ATI made compatible and improved EGA graphics cards in the 1980s.

To help people who want to repair their vintage IBM EGA cards, I've put together this reference schematic and layout. The schematic is closely modeled after the schematic in the IBM technical reference material but with mistakes corrected and more information added. The PCB layout is closely matched to the original card. Using KiCad, you can click on a component on the schematic and it will automatically highlight it in the layout, so it's perfect if you need to probe pins with a scope, logic analyzer, or even just a multimeter.

You might be excited about fabricating this board so you can have your very own clone of the EGA card, but unless you have the full set of custom chips, the board will be useless.

![Board layout image](https://github.com/schlae/EGACard/blob/main/EGACard.png)

## ROM Images

The video BIOS extension ROM can be found [here](https://minuszerodegrees.net/rom/rom.htm).

There are two other small PROM chips (82S137 devices). The binaries are linked below for reference.

* U48 ([1504181.bin](https://github.com/schlae/EGACard/blob/main/proms/1504181.BIN)) - Decodes the RAM framebuffer and ROM address regions
* U34 ([1502045.bin](https://github.com/schlae/EGACard/blob/main/proms/1502045.BIN)) - Decodes the I/O address space

## License
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0
International License. See [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).

