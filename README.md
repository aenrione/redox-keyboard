<h3 align="center">Redox keyboard</h3>
<h5 align="center">aenrione</h5>

---

The Redox project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, ergonomic split mechanical keyboard. [The Official repository](https://github.com/mattdibi/redox-keyboard) has information about the project and instruction on how to use and assemble the Redox keyboard. This repository has the firmware I use and all the modifications I make throughout the way.

<p align="center">
<img src="img/redox_V0.jpg" alt="Redox" width="600" style="border-radius:3%"/>
</p>
<h5 align="center">My first build</h5>

## Building

To customize the framework you should replace the qmk_firmware/redox folder with the one in this repository. Then you can build the firmware with the following command:

```bash
qmk config user.keyboard=redox/rev1
qmk config user.keymap=default
qmk compile
```

In order to flash the right Pro Micro you should uncomment `#define MASTER_LEFT` or `#define MASTER_RIGHT` in the `config.h` file.

```c
//#define MASTER_LEFT
#define MASTER_RIGHT
// #define EE_HANDS
```

## Flashing
To flash the firmware you should use the following command:

```bash
qmk flash <.hex file>
```
