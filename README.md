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
2. Install the libraries located under `Arduino/libraries` if required.
3. Compile and upload the sketch to your board.
4. If compilation fails because `lv_conf.h` cannot be found, copy it from
   `Arduino/libraries/lvgl/src` into your sketchbook directory and restart the
   IDE.

### ESP‑IDF
1. Open the folder `ESP-IDF/ESP32-S3-Touch-LCD-2.8C-Test` in VS Code with the ESP‑IDF extension installed.
2. Run `idf.py -p PORT build flash monitor` to build and flash the firmware.

If compilation fails after a successful build, re-extract the project and try again.

## 中文说明

本仓库为 ESP32‑S3 触摸屏 LCD 2.8 吋的示例代码和固件，包含 Arduino 与 ESP‑IDF 两种示例。

### 目录结构
- **Arduino/**：Arduino 示例及编译所需库
  - `examples/`：可直接编译的 Arduino 示例
  - `libraries/`：本工程使用的 LVGL 等库
- **ESP-IDF/**：可在 VS Code 中打开的 ESP‑IDF 工程
- **Firmware/**：使用 `flash_download_tool_3.9.5` 在地址 `0x00` 烧录的固件

### 编译示例

#### Arduino
1. 在 Arduino IDE 打开 `Arduino/examples/LVGL_Arduino`。
2. 如有需要，将 `Arduino/libraries` 下的库复制到 IDE 的 `libraries` 目录。
3. 编译并上传到开发板。
4. 如果提示找不到 `lv_conf.h`，请从 `Arduino/libraries/lvgl/src` 复制该文件到你的草稿目录根目录并重启 IDE。

#### ESP‑IDF
1. 在已安装 ESP‑IDF 扩展的 VS Code 中打开 `ESP-IDF/ESP32-S3-Touch-LCD-2.8C-Test`。
2. 执行 `idf.py -p PORT build flash monitor` 编译并烧录。

若首次编译成功后出现编译失败，可重新解压项目后再试。

## License

The code in this repository is licensed under its respective source files. Refer to the headers inside the project for more details.
