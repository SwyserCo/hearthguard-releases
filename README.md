# HearthGuard Firmware Releases

Public repository for HearthGuard OTA firmware updates.

**Source code** is maintained in a separate private repository.

## Devices

| Device | Asset Name | Tag Prefix |
|--------|-----------|------------|
| Scout | `scout_firmware.bin` | `scout-v*` |
| Keep | `keep_firmware.bin` | `keep-v*` |

## How OTA Works

HearthGuard devices check this repository's GitHub Releases API for new firmware versions every 24 hours. When a newer version is found, the firmware binary is downloaded over HTTPS and installed automatically with rollback support.
