# Desktop test project

[Download the latest installer](https://github.com/khaphan97/test-project/releases/latest)

This repository contains Windows installers, SHA-256 checksums and the signed update feed. Application source is maintained separately.

## Install

Download the `MapleExpTracker-<version>-x64.msi` asset from the latest release. Close the tracker and run the installer. It upgrades the existing installation without requiring an uninstall, retains saved sessions and settings, and creates desktop and Start menu shortcuts.

Windows 10 version 1903 or later (x64) or Windows 11 is required. No Python, Rust, .NET, CUDA or Windows OCR language packs are needed on the receiving PC.

## Saved sessions

From 1.0.4, open **History** and choose **Delete → Delete permanently** on the saved session you want to remove. **Cancel** keeps it. Deletion is saved immediately, and the current tracking session continues.

## Updates

Users on 0.1.x must install 1.0.0 or later once. Subsequent releases can be downloaded and installed from the app's update notification or its right-click **Check for updates…** menu. No GitHub account is needed. From version 1.0.3, the app checks in the background every time it opens and shows an update-available popup when a newer version is found. Each launch requests a fresh feed to avoid stale release redirects. Current versions and network failures stay quiet. Installation only runs when requested.

From 1.0.5, the notification is a borderless Maple-style card with Vietnamese release notes and matching **Cập nhật ngay** / **Để sau** buttons. It sizes itself to the content, supports Vietnamese accents and scrolls long changelogs. Older clients keep their existing notification until upgraded. Mini's right-click menu also scrolls so every command stays reachable.

After you choose to update, WinSparkle shows download progress, verifies the installer signature, checkpoints the current session, and closes the tracker to run the upgrade. Reopen the tracker after installation. Postponing an update leaves tracking running. Version 1.0.5 also fixes older clients incorrectly filtering out updates because their EXE lacks a Windows compatibility manifest.

The MSI has an Ed25519 update signature, but does not currently carry a Windows Authenticode publisher certificate.

## Recognition and licenses

Game capture and EXP recognition run locally on CPU. The app uses Windows Graphics Capture, ONNX Runtime, PaddleOCR and an Ultralytics YOLO HUD detector. Their applicable license texts are included with the installed application. No game memory is read or game input sent.
