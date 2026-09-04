# ESP32 RGB LED Matrix Sign

A 64×32 RGB LED matrix sign driven directly by an ESP32.

Rather than using a high-level LED matrix library, the ESP32 controls
the panel's RGB data, row-address, clock, latch, and output-enable
signals directly.

## Features

- 64×32 framebuffer
- Custom 5×7 bitmap font
- Letters A–Z and numbers 0–9
- Scrolling text
- Configurable text color
- Manual row multiplexing and refresh timing
- Direct GPIO control of HUB75-style display signals

## Hardware

- ESP32 development board
- 64×32 RGB LED matrix panel
- 5 V switching power supply
- Jumper wiring

## How It Works

Text is converted into pixels using a custom bitmap font and written
into a framebuffer. The ESP32 repeatedly scans the display rows,
shifts pixel data into the panel, latches each row, and controls the
output-enable timing to produce a persistent image.

## Future Improvements

- Additional characters and symbols
- Multiple colors / improved color control
- Easier message configuration
- Single-power-source enclosure
