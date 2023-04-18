# Kinetic2MQTT

This project is a proof-of-concept receiver for kinetic wireless switches such as those from the Quinetic range from TLC
Direct: https://www.tlc-direct.co.uk/Main_Index/Quinetic/index.html.  This project is demonstrated in the following YouTube
video: https://youtu.be/tz_F4Tjhap0

This project is an Arduino sketch designed to run on ESP8266 microcontrollers connected to a CC1101 433MHz receiver.  As the
sketch is currently configured, the CC1101 should be connected to the ESP8266 over SPI with the CS pin connected to 15 on the
ESP and GDO0 pin on the CC1101 connected to pin 5 on the ESP.

This project uses IotWebConf to provide a setup and configuration interface.  When first powered on, the ESP will broadcast a
WiFi network with an SSID of "kinetic2mqtt" - connnect to this using the password in the sketch and navigate to 192.168.4.1 in
a web browser.  You will then be presented with a web interface allowing you to set a management password, WiFi connection details
and MQTT broker settings.

## Limitations

This project is still very much a proof of concept with very little testing and documentation.  If you wish to use this, you
should be familar with Arduino and ESP8266 development to be able to resolve any issues that occur.

Also bear in mind the following:
* Connecting to MQTT brokers that require SSL or a username/password is not currently implemented
* This has only been tested with the following switches: Quinetic QU WS1S, Quinetic QU GDMK.  Other switches may or may not work.

## Requirements

The following libraries are used by Kinetic2MQTT.  They should be installed in your Arduino development environment prior to building:
* IotWebConf version 3.2.1: https://github.com/prampec/IotWebConf
* PubSubClient version 2.8.0: https://github.com/knolleary/pubsubclient/
* RadioLib version 5.3.0: https://github.com/jgromes/RadioLib
* AceCRC version 1.0.1: https://github.com/bxparks/AceCRC
