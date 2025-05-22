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
2. Copy the contents of `Arduino/libraries` to your Arduino sketchbook's `libraries` folder (e.g. `Documents/Arduino/libraries`) and remove any `lvgl` library installed via the Library Manager.
3. If compilation reports missing `lv_conf.h` or `demos/lv_demos.h`, copy `Arduino/libraries/lvgl/src/lv_conf.h` to your sketchbook root.
4. Compile and upload the sketch to your board.

### ESP‑IDF
1. Open the folder `ESP-IDF/ESP32-S3-Touch-LCD-2.8C-Test` in VS Code with the ESP‑IDF extension installed.
2. Run `idf.py -p PORT build flash monitor` to build and flash the firmware.

If compilation fails after a successful build, re-extract the project and try again.

## License

The code in this repository is licensed under its respective source files. Refer to the headers inside the project for more details.


## 简体中文
- 将本仓库 `Arduino/libraries` 下的库复制至 Arduino `libraries` 目录，并删除其他 LVGL 库
- 如果编译提示缺少 `lv_conf.h` 或 `demos/lv_demos.h`，请将 `Arduino/libraries/lvgl/src/lv_conf.h` 复制到草稿目录
- ESP-IDF 示例位于 `ESP-IDF` 文件夹，可在 VS Code 中直接编译
- 若编译失败，请重新解压项目再尝试

