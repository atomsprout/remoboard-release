# Remoboard for Mac

The desktop companion for [Remoboard](https://atomsprout.com/remoboard/), the keyboard app that lets you type on your phone from your computer.

Remoboard normally works in a browser over Wi-Fi. This app adds **Bluetooth**: the computer and the phone no longer need to be on the same network. It can also open the keyboard's Wi-Fi address, so it works as a window for the normal Wi-Fi mode too.

Version **0.1.0**. Requires **macOS 11 or later**, Intel or Apple silicon. Signed and notarized.

> **Bluetooth needs Remoboard 8.3 or later on the phone** (iOS and Android), where it is part of Remoboard Pro. With 8.2 this app can only be used over Wi-Fi.

## Install

```sh
brew tap atomsprout/tap
brew install --cask atomsprout/tap/remoboard
```

Or [download the disk image](https://github.com/atomsprout/remoboard-release/releases/tag/v0.1.0), open it and drag Remoboard to Applications.

## Use

1. On the phone, open Remoboard, choose **Bluetooth** as the connection mode, and switch to the Remoboard keyboard in any text field.
2. Open Remoboard on the Mac. The first time, macOS asks to allow Bluetooth.
3. Pick your phone in the list, enter the PIN shown on the keyboard, and type.

For Wi-Fi mode, type the address shown on the keyboard into the Wi-Fi field instead.

The app also listens on `127.0.0.1:7777`, speaking the phone's own protocol, so the [Node, Python and MCP clients](https://www.npmjs.com/package/remoboard) work over Bluetooth unchanged.

## Notes

- Bluetooth mode always asks for the PIN (or uses a trusted computer). The image clipboard is not available over Bluetooth.
- The link is encrypted end to end between the phone and this app, on top of Bluetooth itself.
- Run one copy of the app at a time; a second one does not find phones.
- There is no auto-update yet: `brew upgrade --cask atomsprout/tap/remoboard`.
- Windows and Linux builds are not published. They have not been tested with real Bluetooth hardware.

## Uninstall

```sh
brew uninstall --cask atomsprout/tap/remoboard
```

## Feedback

Open an issue here, or join [Discord](https://discord.gg/eGzEaP6TzR) or [Telegram](http://t.me/atomsprout).

---

## 中文

[Remoboard](https://atomsprout.com/remoboard/) 的 Mac 桌面端。Remoboard 是一个手机输入法：在电脑上打字，文字实时出现在手机上。

平时它在浏览器里通过 Wi-Fi 使用。这个应用增加了**蓝牙**连接：电脑和手机不需要在同一个网络里。它也可以打开键盘上显示的 Wi-Fi 地址，当作普通 Wi-Fi 模式的窗口来用。

版本 **0.1.0**。需要 **macOS 11 或更高版本**，Intel 和 Apple 芯片都支持。已签名并通过公证。

> **蓝牙模式需要手机上的 Remoboard 8.3 或更高版本**（iOS 和 Android），属于 Remoboard Pro 功能。手机上是 8.2 时，这个应用只能通过 Wi-Fi 使用。

安装：

```sh
brew tap atomsprout/tap
brew install --cask atomsprout/tap/remoboard
```

也可以[直接下载安装包](https://github.com/atomsprout/remoboard-release/releases/tag/v0.1.0)。

使用：手机上打开 Remoboard，连接方式选**蓝牙**，切换到 Remoboard 键盘；在 Mac 上打开 Remoboard，第一次会请求蓝牙权限；在列表里选择手机，输入键盘上显示的 PIN，开始打字。

问题反馈：在这里提 issue，或加入 [Discord](https://discord.gg/eGzEaP6TzR)、[Telegram](http://t.me/atomsprout)。
