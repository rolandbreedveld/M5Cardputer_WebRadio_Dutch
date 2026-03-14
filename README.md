# M5Cardputer WebRadio Danish version

This project is a WebRadio player for the M5Stack Cardputer, specifically customized with Danish radio stations. It is based on the [M5Cardputer_WebRadio](https://github.com/cyberwisk/M5Cardputer_WebRadio) project.

## Features

*   **Danish Radio Stations:** Pre-configured with a list of popular Danish radio streams (DR, Nova, Pop FM, etc.).
*   **M3U/PLS Support:** Automatically parses `.m3u` and `.pls` playlist files to play the underlying audio stream.
*   **Stable Boot:** Optimized memory usage to run smoothly on the M5StampS3 (Cardputer core) without PSRAM.
*   **Robust WiFi:** Improved WiFi connection logic with auto-retry and scanning.
*   **Volume & Station Control:** Use the keyboard to change stations and volume.
*   **Visualizer:** FFT and Waveform visualization on the screen.

## Firmware

The latest compiled firmware is available in this repository as `M5Cardputer_WebRadio_danish.bin`. You can flash this directly to your Cardputer using tools like [esptool](https://github.com/espressif/esptool) or the [M5Burner](https://docs.m5stack.com/en/download).

## Usage

1.  **WiFi Setup:** On first boot, the device will scan for networks. Select your network and enter the password using the Cardputer keyboard. Settings are saved to EEPROM.
2.  **Controls:**
    *   `/` : Next Station
    *   `,` : Previous Station
    *   `;` : Volume Up
    *   `.` : Volume Down
    *   `m` : Mute/Unmute
    *   `BtnA` (Orange Button): Next Station (Click), Previous Station (Double Click)

## Libraries Required

To compile from source, you need the following Arduino libraries:

*   [M5Unified](https://github.com/m5stack/M5Unified)
*   [ESP8266Audio](https://github.com/earlephilhower/ESP8266Audio)
*   [M5Cardputer](https://github.com/m5stack/M5Cardputer)
*   [M5GFX](https://github.com/m5stack/M5GFX)

![image](https://github.com/rolandbreedveld/M5Cardputer_WebRadio_Dutch/blob/main/M5Cardputer_WebRadio_NL.jpeg)

## Compilation Instructions

If you want to modify and compile the code yourself using the Arduino IDE:

1.  **Board Selection:** Select `M5Stack` -> `M5StampS3`.
2.  **Partition Scheme:** Select `"No OTA(2MB APP/2MB FATFS)"`.
    *   *Note: This is critical. The default partition scheme may not have enough app space or may cause memory issues.*
3.  **Compile:** Verify and Upload.

To generate a binary file: `Sketch` -> `Export Compiled Binary`.
