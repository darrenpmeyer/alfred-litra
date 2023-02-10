# Alfred Litra

Controls Litra Glow and Litra Beam USB conferencing/streaming lights

Solution is thanks to two existing command-line tools, which we learned from to create our own solution:

* https://github.com/kharyam/litra-driver (a PyUSB driver that doesn't work on macOS)
* https://ultracrepidarian.phfactor.net/2022/03/09/controlling-the-logitech-litra-on-macos/ (instructions for using shell functions with 'hidapitester' to control a Litra Glow)

We ship amd64 and x86_64 versions of the hidapitester binary from https://github.com/todbot/hidapitester ; the correct one should be autoselected, which means **this works with both Intel and Apple Silicon M1/M2 chips**

You can also use the `hid-litra.py` script without Alfred, but only on macOS

## 0.1.0

Use 'litra [-d {glow,beam}] [-t TEMP] [-b PERCENT] [{on,off}]'

If you specify a TEMP or PERCENT value, 'on' is presumed unless 'off' is specified.