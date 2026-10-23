# Desktop test project

[Download the latest installer](https://github.com/khaphan97/test-project/releases/latest)

This repository contains Windows installers, SHA-256 checksums and the signed update feed. Application source is maintained separately.

## Install

Download the `MapleExpTracker-<version>-x64.msi` asset from the latest release. Close the tracker and run the installer. It upgrades the existing installation without requiring an uninstall, retains saved sessions and settings, and creates desktop and Start menu shortcuts.

Windows 10 version 1903 or later (x64) or Windows 11 is required. No Python, Rust, .NET, CUDA or Windows OCR language packs are needed on the receiving PC.

## Updates

Users on 0.1.x must install 1.0.0 or later once. Subsequent releases can be downloaded and installed from the app's update notification or its right-click **Check for updates…** menu. No GitHub account is needed. The app checks in the background at its daily interval and installs only when requested.

The updater verifies the installer signature, checkpoints the current session, and closes the tracker to run the upgrade. Reopen the tracker after installation. Postponing an update leaves tracking running.

The MSI has an Ed25519 update signature, but does not currently carry a Windows Authenticode publisher certificate.

## Recognition and licenses

Game capture and EXP recognition run locally on CPU. The app uses Windows Graphics Capture, ONNX Runtime, PaddleOCR and an Ultralytics YOLO HUD detector. Their applicable license texts are included with the installed application. No game memory is read or game input sent.
