# Firmware flasher

Static Web Serial flasher for CYD firmware. Uses a vendored copy of
[esptool-js](https://github.com/espressif/esptool-js) 0.5.4 (Apache-2.0, see `vendor/`).

Select the CYD 2.8-inch, 3.5-inch, or 4-inch profile, then drop in the matching
board's `firmware.bin`. The firmware slot at `0x10000` is required. The
bootloader, partitions, and `boot_app0` slots are available but optional for
every profile; leaving them empty does not prevent flashing the firmware. The
profile does not download or build firmware.

Select **Custom board (4 slots)** for a different board or a full PlatformIO
flash. All profiles provide these slots:

- `bootloader.bin` at `0x1000` (optional)
- `partitions.bin` at `0x8000` (optional)
- `boot_app0.bin` at `0xe000` (optional)
- `firmware.bin` at `0x10000` (required)

The first three files are in `.pio/build/esp32dev/`, except `boot_app0.bin`,
which is in
`~/.platformio/packages/framework-arduinoespressif32/tools/partitions/`.
Only flash images built for the connected board. The flasher does not check
image compatibility.

Requires desktop Chrome, Edge or Opera, served over HTTPS.
