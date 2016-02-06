# Motorcycle Computer
A microcontroller (arduino/spark/photon) based system to provide additional functions to a motorcycle.

This project will be to create a computer to augment a motorcycle to provide additional features.

## Short Feature List:
* Auxillary lighting
  * Turn signals
  * Tail light
  * Brake light
  * other
* Temperature (outside, not engine)
* Motorcycle Battery Gauge (Volts & Amps)
* Compass
* GPS Tracking
* Alarm
* Garage door Opener
  * Most Likely will splice in a keychain remote for this
  * Use a custom sequence to trigger
    * Flash brights 3 times while braking?

## Parts:
* Particle Photon
* NeoPixels (or similar)
* GPS
* Bluetooth
* Motion Sensor
* Battery
* WiFi Module
* RFID
* Cellular Modem

## Detailed Features:

### Compass
  * Provide a simple N,NE,E,SE,S,SW,W,NW output
  * Maybe show on a NeoPixel ring with N as Red, ring could be used for other output as well.

### GPS Tracking
  * Starts new tracked trip each time bike is started
  * Sends position every 30 minutes via cell modem to tracker app
  * Stores position every 15 seconds in GPS memory
  * Uploads data from memory to cloud when returning home via wifi
  * Uses bike for power, but has battery so it can run for a minute after bike shuts down
  * Wifi module for downloading tracking data in non emergency situations

### Temperature Guage

### Alarm/Anti-theft
  * Potentially use bike battery to run as alarm when parked
  * Lean angle sensor
  * If bike starts & doesn't connect to Bluetooth/phone start tracking & send location to phone
  * Add sensor for jostling/theft
	* RFID
		* Use to enable starter
### Auxillary Lights
  * Deceleration sensor to run lights
  * Brake light output
  * Turn signal output
  * If using full color LED strips set lights up to have a secret cop mode to flash blue/red

### Connect to helmet via Bluetooth to give info.
  * Alerts for rear ending.
  * Option to alert when deceleration sensor is activated for testing

### Sonic sensor in rear to warn of fast approaching cars

### Connectivity
  * Cellular Modem
    * Cellular connectivity for  messaging
  * Set to auto connect to wifi @ home and upload data to home/cloud when returning. Use battery power to do so.

### Garage Door Opener
  * Garage door opener output ( to be sent to a keychain remote )

### Other
  * Attach to action camera to monitor battery & memory card usage?
  * Connect to dash to determine Rpm, speed, odometer
  * Log odometer data automatically for tracking service & ride length
    * Maybe just use GPS for this if it tracks every ride
  * Crash detection sensor
  * Redline indicator in helmet
  * 2 minute timer that starts when coming to a stop - used to time traffic lights, maybe use small LEDs to indicate 30 second increments.
    * could use NeoPixel ring for this
