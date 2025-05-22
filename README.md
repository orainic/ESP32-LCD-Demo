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

## Installing the Bundled Arduino Libraries

1. **Remove any LVGL library installed via the Library Manager.**
2. Copy `Arduino/libraries/lvgl` from this repository to your `Documents/Arduino/libraries/` folder.
3. Copy `Arduino/libraries/lvgl/src/lv_conf.h` into the same folder (next to `lvgl`).
4. Restart the Arduino IDE.

If you encounter a message such as `text section exceeds available space in board`, choose a larger *Partition Scheme* from the **Tools** menu (for example, `Huge APP`).

### Arduino库的安装

1. **删除通过 Library Manager 安装的 LVGL 库。**
2. 将本仓库的 `Arduino/libraries/lvgl` 文件夹复制到 `Documents/Arduino/libraries/`。
3. 把 `Arduino/libraries/lvgl/src/lv_conf.h` 复制到同一目录，与 `lvgl` 文件夹同级。
4. 重新启动 Arduino IDE。

如出现 `text section exceeds available space in board` 错误，可在 **Tools** 菜单中把 *Partition Scheme* 设置为 `Huge APP` 或其他更大的选项。


### ESP‑IDF
1. Open the folder `ESP-IDF/ESP32-S3-Touch-LCD-2.8C-Test` in VS Code with the ESP‑IDF extension installed.
2. Run `idf.py -p PORT build flash monitor` to build and flash the firmware.

If compilation fails after a successful build, re-extract the project and try again.

## License

The code in this repository is licensed under its respective source files. Refer to the headers inside the project for more details.
