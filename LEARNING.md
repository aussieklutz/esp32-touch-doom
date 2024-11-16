# ESP32-Doom Exploration

## Hardware
I am using the lonely binary variant of the ESP32-S3-DEVKITC-1 V1.3 as the base.
For a display, a 1.8" LCD with a ST7735S controller

## Process
- Soldered pin headers to the ESP32 board
- Soldered pins to the Display board
- Found the default LCD pinout in /components/prboom-esp32-compat/spi_lcd.c
  - #define PIN_NUM_MISO 25 -> 
  - #define PIN_NUM_MOSI 23
  - #define PIN_NUM_CLK  19
  - #define PIN_NUM_CS   22
  - #define PIN_NUM_DC   21
  - #define PIN_NUM_RST  18
  - #define PIN_NUM_BCKL 5
- Uses a SPI interface, by default for a ILI9341 display driver chip
- Our display uses an ST7735S driver and I2C interface
- Need to replace the existing SPI Display driver library
- 
