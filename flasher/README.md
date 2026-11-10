# Firmware flasher

Static Web Serial flasher for the ESP32 (`esp32dev`) firmware in this project.
Uses a vendored copy of [esptool-js](https://github.com/espressif/esptool-js) 0.5.4 (Apache-2.0, see `vendor/`).

Files to flash (from `.pio/build/esp32dev/`): `bootloader.bin` (0x1000), `partitions.bin` (0x8000),
`firmware.bin` (0x10000). `boot_app0.bin` (0xe000) lives in
`~/.platformio/packages/framework-arduinoespressif32/tools/partitions/`.

Requires desktop Chrome, Edge or Opera, served over HTTPS.
