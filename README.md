# SUNTEK SCP85 票据/标签打印机 SDK 合集

本仓库收集了 SUNTEK SCP85 系列打印机在各平台下的开发工具包（SDK）及驱动程序，方便开发者快速集成打印功能。

## 仓库内容

| 文件 | 说明 | 版本 |
|------|------|------|
| `Android+SDK+3.5.5.zip` | Android 平台 SDK，含 Demo 工程 | v3.5.5 |
| `SUNTEK Ticket Product SDK Development Kit+Windows+2.3.1.zip` | Windows 平台 SDK，含 CPCL / ESC / TSPL / ZPL 四个子模块 | v2.3.1 |
| `iOS+SDK+v3.2.7.7z` | iOS 平台 SDK | v3.2.7 |
| `Xprinter_2024.2_M-1.exe` | Windows 打印机驱动安装程序 | v2024.2 M-1 |

## 支持的打印协议

- **CPCL** — 移动标签打印指令语言
- **TSPL** — TSC 打印机指令语言
- **ZPL** — Zebra 打印机指令语言
- **ESC/POS** — 票据打印机通用指令集
- **POS** — POS 模式打印

## 支持的连接方式

- 蓝牙（Bluetooth）
- 网络（TCP / UDP）
- WiFi
- USB

## Android SDK

Android SDK（v3.5.5）提供完整的 Kotlin Demo 工程，涵盖以下功能模块：

| Activity | 说明 |
|----------|------|
| `MainActivity` | 主入口，选择连接方式与打印协议 |
| `CpclActivity` | CPCL 协议打印 |
| `TsplActivity` | TSPL 协议打印 |
| `ZplActivity` | ZPL 协议打印 |
| `PosActivity` / `PosTaskActivity` | POS 模式打印 |
| `EscMultiConnectionActivity` | ESC/POS 多连接管理 |
| `SelectBluetoothActivity` | 蓝牙设备选择 |
| `SelectNetActivity` | 网络设备选择 |

核心库文件为 `printer-lib-3.5.5.aar`，开发者可直接引用。

### 快速开始

1. 解压 `Android+SDK+3.5.5.zip`
2. 用 Android Studio 打开 `Android SDK 3.5.5/PrinterDemo` 工程
3. 编译运行 Demo App，参照各 Activity 代码进行集成

### 文档

SDK 压缩包内附以下开发手册（中英文）：

- Android CPCL Program Manual / CPCL 编程手册
- Android Port Program Manual / 接口编程手册
- Android POS Program Manual / POS 编程手册
- Android TSPL Program Manual / TSPL 编程手册
- Android ZPL Program Manual / ZPL 编程手册

## Windows SDK

Windows SDK（v2.3.1）基于 C++ 开发，按打印协议分为四个子目录：

| 子目录 | 协议 | 内容 |
|--------|------|------|
| `cpcl/` | CPCL | SDK 库（x86/x64）+ WinSDKDemo + 开发手册 |
| `esc/` | ESC/POS | SDK 库（x86/x64）+ WinSDKDemo + 开发手册 |
| `tspl/` | TSPL | SDK 库（x86/x64）+ WinSDKDemo + 开发手册 |
| `zpl/` | ZPL | SDK 库（x86/x64）+ WinSDKDemo + 开发手册 |

每个子目录均包含：

- `lib/` — 动态链接库（`printer.sdk.dll`）和导入库（`printer.sdk.lib`），同时支持 x86 和 x64
- `Sample/` — 预编译的 WinSDKDemo 可执行文件
- `WinSDKDemo/` — Visual Studio 工程源码（`.sln` + `.vcxproj`）
- SDK Manual（英文）和 指令开发手册（中文）

### 快速开始

1. 解压 `SUNTEK Ticket Product SDK Development Kit+Windows+2.3.1.zip`
2. 用 Visual Studio 打开对应协议子目录下的 `WinSDKDemo.sln`
3. 或直接运行 `Sample/x64/WinSDKDemo.exe` 体验 Demo

## iOS SDK

iOS SDK（v3.2.7）以 7z 压缩包形式提供，解压后可获取 iOS 平台下的打印开发库及示例工程。

## 驱动安装

在 Windows 系统下，运行 `Xprinter_2024.2_M-1.exe` 即可安装打印机驱动。

## 相关链接

- GitHub 仓库：[https://github.com/SUNTEK-DEV/SCP85](https://github.com/SUNTEK-DEV/SCP85)

## 许可证

本项目仅供开发参考使用，具体许可条款请联系 SUNTEK 官方确认。
