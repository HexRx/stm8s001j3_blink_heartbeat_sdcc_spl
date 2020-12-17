# STM8S001J3 blink heartbeat :heartbeat: example for STM8 SPL and SDCC

This example compiles by SDCC (tested v4.0.0) and works with [STM8 SPL (STSW-STM8069)](https://www.st.com/en/embedded-software/stsw-stm8069.html) v2.3.1 patched by [STM8-SPL_SDCC_patch](https://github.com/gicking/STM8-SPL_SDCC_patch).

The LED connected to the `PA1` pin. It's how the LED connected on the [STM8S001J3 tiny board](https://github.com/HexRx/STM8S001J3_tiny_board).

To delay function uses the timer `TIM4`, CPU runs on 16Mhz.

To flash firmware to STM8S001J3 MCU uses ST-Link and [stm8flash](https://github.com/vdudouyt/stm8flash) tool.

## Download binary
The compiled `ihx` firmware for STM8S001J3 can be downloaded from [Releases](https://github.com/HexRx/stm8s001j3_blink_heartbeat_sdcc_spl/releases) section. The last version can be downloaded by the [blink_heartbeat_spl.ihx](https://github.com/HexRx/stm8s001j3_blink_heartbeat_sdcc_spl/releases/download/1.0/blink_heartbeat_spl.ihx) link.

To flash it through stm8flash and ST-Link programmer just run:
```
stm8flash -c stlinkv2 -p stm8s001j3 -w blink_heartbeat_spl.ihx
```

## Build from source & Flash
```
make
make flash
```

If needed use the command `make size` to get the size of the binary firmware before actually flashing into MCU. 
