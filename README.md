
RPI Install
===========

```bash
    pip3 install adafruit-circuitpython-fingerprint
```

To install system-wide (this may be required in some cases):

```bash
    sudo pip3 install adafruit-circuitpython-fingerprint
```

To install in a virtual environment in your current project:

```bash
    python3 -m venv .venv
    source .venv/bin/activate
    pip3 install adafruit-circuitpython-fingerprint
```

Remove from /boot/firmware/cmdline.txt:

```bash
    console=serial0,115200
```

Add to /boot/firmware/config.txt:

```bash
    enable_uart=1
```

## RPI4 Connection diagram
|     R503 Sensor      |     Raspberry PI     |
| -------------------- | ------------------------- |
| RED (Power 3V)       | [3.3V](https://pinout.xyz/pinout/3v3_power)  |
| BLACK (GND)          | [Ground](https://pinout.xyz/pinout/ground)  |
| YELLOW (TXD)         | [UART RX](https://pinout.xyz/pinout/pin10_gpio15)  |
| GREEN (RXD)          | [UART TX](https://pinout.xyz/pinout/pin8_gpio14)  |
| BLUE (Wakeup)        | [GPIO 26](https://pinout.xyz/pinout/pin37_gpio26)  |
| WHITE (3.3VT)        | Not connected  |
