---
layout: post
title: program arduino .ino file with sublime text 3
categories: [cs, software]
tags: [sublime, arduino, arduino-cli]
published: True
comments: True
---

Install `arduino-cli` with package control in sublime text 3. Use `Tool->Arduino->Open User Settings` and add following for Windows. Then <kbd>ctrl</kbd><kbd>shift</kbd><kbd>b</kbd> for build current `.ino` file.

```json
{
    "path": "C:\\Program Files (x86)\\Arduino\\arduino.exe",
    "board": "arduino:avr:uno",
    "port": "COM4"
}
```

Using following to build arduino program directly from cli.

```bash
# Common usage
arduino --upload --board arduino:avr:uno --port COM4 led.ino

# Start the Arduino IDE, with two files open:
arduino /path/to/sketch/sketch.ino /path/to/sketch/extra.ino

# Compile and upload a sketch using the last selected board and serial port
arduino --upload /path/to/sketch/sketch.ino

# Compile and upload a sketch to an Arduino Nano, with an Atmega168 CPU, connected on port /dev/ttyACM0:
arduino --board arduino:avr:nano:cpu=atmega168 --port /dev/ttyACM0 --upload /path/to/sketch/sketch.ino

# Compile a sketch, put the build results in the build directory an re-use any previous build results in that directory.
arduino --pref build.path=/path/to/sketch/build --verify /path/to/sketch/sketch.ino

# Change the selected board and build path and do nothing else.
arduino --pref build.path=/path/to/sketch/build --board arduino:avr:uno --save-prefs

# Install latest SAM board support
arduino --install-boards "arduino:sam"

# Install AVR board support, 1.6.2
arduino --install-boards "arduino:avr:1.6.2"

# Install Bridge library version 1.0.0
arduino --install-library "Bridge:1.0.0"

# Install Bridge and Servo libraries
arduino --install-library "Bridge:1.0.0,Servo:1.2.0"
```

[1]: https://github.com/arduino/Arduino/blob/ide-1.5.x/build/shared/manpage.adoc
