# ESP32 LCD Demo

This repository provides demo code and firmware for the ESP32-S3 Touch LCD 2.8" board. It contains Arduino and ESP-IDF examples as well as a pre-built firmware image.

## Repository Layout

- **Arduino/** – Arduino sketches and required libraries
  - `examples/` – ready-to-build Arduino example
  - `libraries/` – LVGL and other libraries used by the example
- **ESP-IDF/** – ESP-IDF example project which can be opened in VS Code
- **Firmware/** – pre-built firmware image (`.bin`) that can be flashed via `flash_download_tool_3.9.5` at address `0x00`

## Building the Examples

### Arduino
1. Open `Arduino/examples/LVGL_Arduino` in the Arduino IDE.
2. Copy `Arduino/libraries/lvgl/src/lv_conf.h` to your Arduino sketchbook root (e.g. `Documents/Arduino/lv_conf.h`).
   This allows the LVGL library to locate its configuration file.
3. Copy the folders under `Arduino/libraries` into your `Documents/Arduino/libraries` directory and remove any LVGL version installed via the Library Manager.
4. Compile and upload the sketch to your board.


### ESP‑IDF
1. Open the folder `ESP-IDF/ESP32-S3-Touch-LCD-2.8C-Test` in VS Code with the ESP‑IDF extension installed.
2. Run `idf.py -p PORT build flash monitor` to build and flash the firmware.

If compilation fails after a successful build, re-extract the project and try again.

## License

The code in this repository is licensed under its respective source files. Refer to the headers inside the project for more details.
