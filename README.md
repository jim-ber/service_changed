# OTA Firmware Updating
This project contains a working example of OTA Firmware updating using the ESP32 libraries and Mongoose Webserver.

To see it in action, first change the EXAMPLE_SENTENCE to indicate that the version is a factory version. Next run `make erase_flash flash` to completely erase the flash memory and flash the factory app into the factory partition.

Next, we can alter the EXAMPLE_SENTENCE define to indicate that this new image is a OTA 1 image. Run `make` and copy the resulting bin file into scripts, rename it to `hub.bin`, and run `node post.js`. Once complete, the device will restart automatically.