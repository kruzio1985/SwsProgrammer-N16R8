# Firmware — N16R8 build

Prebuilt, frozen image for the `ESP32-S3-DevKitC-1-N16R8`
(**16 MB (Quad SPI)** flash, **8 MB (Octal SPI)** PSRAM).

| File | Size | SHA-256 |
|---|---|---|
| `sws_programmer_esp32s3_n16r8_v1.1.bin` | 963488 B | `3bf587d90ea74de097f38dd48f981671294572a846f76cfe7acf0d00a6f3f230` |

- **target:** `ESP32-S3-DevKitC-1-N16R8` (PlatformIO env `esp32s3n16r8`)
- **pins (all functions):** SWS=42, RST=41, UART TX/RX=17/18, RS485=33/34/35,
  SD SCK/MISO/MOSI/CS=14/15/16/21, SPI flash SCK/MISO/MOSI/CS=12/13/11/10,
  I²C=8/9, 1-Wire=4, ESP bridge IO0/EN=5/6, console UART0 GPIO43/44
- **build:** `pio run -e esp32s3n16r8`
- **flash:** `pio run -e esp32s3n16r8 -t upload --upload-port COMx`
- **web UI:** SoftAP `SWS-Programmer` / `12345678` → `http://192.168.4.1`

## Verify

```powershell
Get-FileHash firmware\sws_programmer_esp32s3_n16r8_v1.1.bin -Algorithm SHA256
```