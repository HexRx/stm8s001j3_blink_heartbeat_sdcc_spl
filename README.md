# STM8S001J3 blink heartbeat :heartbeat: example for STM8 SPL and SDCC

This example compiles by SDCC (tested v4.0.0) and works with [STM8 SPL (STSW-STM8069)](https://www.st.com/en/embedded-software/stsw-stm8069.html) v2.3.1 patched by [STM8-SPL_SDCC_patch](https://github.com/gicking/STM8-SPL_SDCC_patch).

The LED connected to the `PA1` pin. It's how the LED connected on the [STM8S001J3 tiny board](https://github.com/HexRx/STM8S001J3_tiny_board).

To delay function uses the timer `TIM4`, CPU runs on 16Mhz.

To flash firmware to STM8S001J3 uses ST-Link and [stm8flash](https://github.com/vdudouyt/stm8flash).

## Build & Flash
```
make
make flash
```

If needed use the command `make size` to get the size of the binary firmware before actual flashing. 