# smart_plant_watering_system
An Arduino-based automated plant care system that monitors environmental conditions and controls irrigation to optimize plant health and reduce manual effort.
#Overview
Arduino-based automated plant care system that monitors environmental conditions and controls watering.

Hardware Required
Arduino-compatible Aries board
MD_MAX72XX LED Matrix
SSD1306 OLED Display (I2C)
BMP085/BMP180 Temperature Sensor
Light Dependent Resistor (LDR)
Touch Sensor
Relay Module
Buzzer
Water pump/solenoid valve
Pin Configuration
Touch Sensor: Pin 0 Relay: Pin 1
Buzzer: Pin 2 LED Matrix DIN: Pin 11 LED Matrix CLK: Pin 13 LED Matrix CS: Pin 10 LDR: Pin A0

Features
Temperature monitoring
Automated watering control
Light level sensing
LED matrix moisture display
Bluetooth connectivity
OLED status display
Touch sensor interface
Audio feedback
Dependencies
MD_MAX72xx.h
SPI.h
Wire.h
Adafruit_GFX.h
Adafruit_SSD1306.h
Adafruit_BMP085.h
UARTClass.h
Operation
System monitors temperature, light and moisture
Waters when:
Temp > 24°C
Light < 80
Moisture < Max level
5 minute safety timeout on watering
Touch increases moisture level (max 8)
LED matrix shows moisture level
OLED displays all sensor readings
Bluetooth sends data for remote monitoring
Safety Features
Max watering time limit
System init checks
Error indication via buzzer
Debug Mode
Set DEBUG to 1 for serial monitoring of:

Sensor readings
System status
Water events
Errors
Error Codes
Continuous short beeps = OLED init failed Continuous long beeps = Temp sensor init failed

Bluetooth Data Format
temperature,light_level,moisture_level,water_status
