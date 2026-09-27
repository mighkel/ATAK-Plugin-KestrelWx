# Tester Guide

## Before Testing

Collect these details first:

- ATAK version
- Android OS version
- device model
- plugin version

## What To Check

- plugin installs successfully
- ATAK discovers the plugin
- the plugin UI opens
- expected BLE/device/network workflows behave correctly
- no crashes during startup, connect, or normal use

## Good Bug Report Format

Please include:

- exact steps to reproduce
- expected behavior
- actual behavior
- whether it happens every time or intermittently
- screenshots or short screen recordings if available

## Which build to install

Install the APK that matches your ATAK version (5.6, 5.7 or 5.8), from the
Releases page. Builds here are signed by the TAK Product Center and only load
on official ATAK (tak.gov or the Play Store), not on a developer build.

After updating the plugin, fully close ATAK and reopen it before testing.

## If Install Fails

Please note:

- exact install error text
- whether an older plugin version was already installed
- whether ATAK or the plugin had to be removed first
