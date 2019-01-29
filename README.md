# fridgemonitor
Monitor temperature through a lightweight IoT device. Meant for HVAC and food service solutions.


## Here's how it works
1. Set up the device and flash your software onto the ESP8266. 
2. Turn on the device. If this is your first time setting it up, the device will open up a wifi access point called "Fridgemonitor".
3. Connect to the wifi point through another device like your phone. It will lead you to a splash page asking for wifi information.
4. Follow the instructions and input your preferred settings to connect the device to your local wifi.
5. Once your wifi is connected, the device is now able to send you text messages.
6. Test this out by leaving the fridge monitor in an environment that is above freezing temperature. You should get the text message pretty quickly.
7. You can reset the wifi information by reconnecting to the access point. This can be done by leaving the monitor in any above freezing environment so that it goes into the notification loop.


## Technical Details
- You need an ESP8266 and a BME680 temperature, altitude, and humidity sensor. Use platformio for flashing your hardware.

### Hardware Prototyping Setup
- Connect your BME680 to the ESP through I2C. 
- You also need to enable deep sleep cycles on the ESP8266, so connect the ESP8266 with the following schematic:
![schematic](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/esp-12.png?w=609&ssl=1)

