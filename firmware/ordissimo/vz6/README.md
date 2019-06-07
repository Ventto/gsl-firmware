# Ordissimo / VZ6

**Caution: this is a prototype platform**

## Description

--------------------------------------
| Item                      | Description |
|---------------------------|-------------|
| Manufacturer              | Ordissimo   |
| Device                    | VZ6 (prototype) |
| Website                   | https://www.ordissimo.fr |
| Vendor driver (Windows)   | Silead         |
| Extracted firmware        | SileadTouch.fw |
| Firmware for gslx680-acpi | silead\_ts.fw   |
| Display resolution        | 1920x1080       |
| Touch panel resolution    | 2660x1940       |
| Touch controller          | GSL1680        |
| Multitouch support        | No "for now" |
| Finger tracking           | Yes  |
| Mirrored horizontally     | No   |
| Mirrored vertically       | No   |
| Axes swapped              | No   |
--------------------------------------

## Calibration


```
../../../tools/fwtool -c SileadTouch.fw -m 1680 \
                                        -w 2660 -h 1940 \
                                        -t 10 \
                                        silead_ts.fw
```

## Installation

The `silead_ts.fw` must be copied into the `/lib/firmware` directory on the
target.
