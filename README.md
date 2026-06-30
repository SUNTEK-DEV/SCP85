# SUNTEK SCP85 Ticket / Label Printer SDK Collection

This repository contains software development kits (SDKs) and drivers for the SUNTEK SCP85 series printers across multiple platforms, enabling developers to quickly integrate printing capabilities.

## Repository Contents

| File | Description | Version |
|------|-------------|---------|
| `Android+SDK+3.5.5.zip` | Android SDK with demo project | v3.5.5 |
| `SUNTEK Ticket Product SDK Development Kit+Windows+2.3.1.zip` | Windows SDK with CPCL / ESC / TSPL / ZPL sub-modules | v2.3.1 |
| `iOS+SDK+v3.2.7.7z` | iOS SDK | v3.2.7 |
| `Xprinter_2024.2_M-1.exe` | Windows printer driver installer | v2024.2 M-1 |

## Supported Printing Protocols

- **CPCL** — Mobile label printing command language
- **TSPL** — TSC printer command language
- **ZPL** — Zebra printer command language
- **ESC/POS** — Universal receipt printer command set
- **POS** — POS mode printing

## Supported Connection Methods

- Bluetooth
- Network (TCP / UDP)
- WiFi
- USB

## Android SDK

The Android SDK (v3.5.5) includes a complete Kotlin demo project with the following modules:

| Activity | Description |
|----------|-------------|
| `MainActivity` | Entry point for selecting connection method and printing protocol |
| `CpclActivity` | CPCL protocol printing |
| `TsplActivity` | TSPL protocol printing |
| `ZplActivity` | ZPL protocol printing |
| `PosActivity` / `PosTaskActivity` | POS mode printing |
| `EscMultiConnectionActivity` | ESC/POS multi-connection management |
| `SelectBluetoothActivity` | Bluetooth device selection |
| `SelectNetActivity` | Network device selection |

The core library is `printer-lib-3.5.5.aar`, which can be directly referenced in your project.

### Getting Started

1. Extract `Android+SDK+3.5.5.zip`
2. Open the `Android SDK 3.5.5/PrinterDemo` project in Android Studio
3. Build and run the demo app, and refer to each Activity's source code for integration

### Documentation

The SDK archive includes the following developer manuals (in both English and Chinese):

- Android CPCL Program Manual / CPCL 编程手册
- Android Port Program Manual / 接口编程手册
- Android POS Program Manual / POS 编程手册
- Android TSPL Program Manual / TSPL 编程手册
- Android ZPL Program Manual / ZPL 编程手册

## Windows SDK

The Windows SDK (v2.3.1) is developed in C++ and organized into four sub-directories by printing protocol:

| Sub-directory | Protocol | Contents |
|---------------|----------|----------|
| `cpcl/` | CPCL | SDK libraries (x86/x64) + WinSDKDemo + developer manual |
| `esc/` | ESC/POS | SDK libraries (x86/x64) + WinSDKDemo + developer manual |
| `tspl/` | TSPL | SDK libraries (x86/x64) + WinSDKDemo + developer manual |
| `zpl/` | ZPL | SDK libraries (x86/x64) + WinSDKDemo + developer manual |

Each sub-directory contains:

- `lib/` — Dynamic link library (`printer.sdk.dll`) and import library (`printer.sdk.lib`), supporting both x86 and x64
- `Sample/` — Pre-built WinSDKDemo executable
- `WinSDKDemo/` — Visual Studio project source code (`.sln` + `.vcxproj`)
- SDK Manual (English) and command development guide (Chinese)

### Getting Started

1. Extract `SUNTEK Ticket Product SDK Development Kit+Windows+2.3.1.zip`
2. Open `WinSDKDemo.sln` in the relevant protocol sub-directory with Visual Studio
3. Or run `Sample/x64/WinSDKDemo.exe` directly to try the demo

## iOS SDK

The iOS SDK (v3.2.7) is provided as a 7z archive. Extract it to access the iOS printing library and sample project.

## Driver Installation

On Windows, run `Xprinter_2024.2_M-1.exe` to install the printer driver.

## Links

- GitHub Repository: [https://github.com/SUNTEK-DEV/SCP85](https://github.com/SUNTEK-DEV/SCP85)

## License

This project is provided for development reference only. For specific licensing terms, please contact SUNTEK directly.
