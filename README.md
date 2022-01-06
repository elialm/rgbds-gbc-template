# rgbds-gbc-template
Template project for Gameboy Color game using the RGBDS assembler.

Information on the RGBDS tools can be found on the
[RGBDS home page](https://rgbds.gbdev.io/).
For other sources on Gameboy development, check the
[Awesome Game Boy Development](https://github.com/gbdev/awesome-gbdev)
Github page.

## Building

Building is done using `make`. `make` will compile and link all `*.z80` files
inside `src`. The script will create directories `obj` and `build`. `obj`
will contain all `*.o` files resulting from compilation. `build` will contain
the builded `*.gbc` file ready to be played.

## Including

Including a file in RGBDS assembly is done using the `include` directive:

```asm
include "hardware.inc"
```

The assembler will search `include` for the file being included.

## Naming the image

To name the image, change the `NAME` variable inside `Makefile`.

## Interrupt routines

The sections of the interrupt routines for the Gameboy interrupts are
included in the `layout.z80` file. Modify these if you need to use them.