# Kinetic2MQTT

This project is a proof-of-concept receiver for kinetic wireless switches such as those from the Quinetic range from TLC Direct: https://www.tlc-direct.co.uk/Main_Index/Quinetic/index.html.  This project is demonstrated in the following YouTube video: https://youtu.be/tz_F4Tjhap0

This project is an Arduino sketch designed to run on ESP8266 microcontrollers connected to a CC1101 433MHz receiver.  As the sketch is currently configured, the CC1101 should be connected to the ESP8266 over SPI with the CS pin connected to 15 on the ESP and GDO0 pin on the CC1101 connected to pin 5 on the ESP.
