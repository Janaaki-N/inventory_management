# Inventory Management System

## Overview
The Inventory Management System is a project designed to monitor the stock levels of products using ultrasonic sensors and an ESP8266 microcontroller. This system tracks the quantities of Product 1 and Product 2 and sends the data to ThingSpeak for remote monitoring.

## Features
- Measures product levels using ultrasonic sensors.
- Updates stock quantities to ThingSpeak.
- Monitors two products: Product 1 and Product 2.

## Prerequisites
- ESP8266 microcontroller
- Ultrasonic sensors (HC-SR04 or similar)
- ThingSpeak account and API key
- Wi-Fi network

## Installation
1. *Hardware Setup:*
   - Connect the ultrasonic sensors to the ESP8266 according to the pin configuration:
     - trigPin and echoPin for Product 1
     - trig1Pin and echo1Pin for Product 2

2. *Software Setup:*
   - Install the required libraries in the Arduino IDE:
     - ESP8266WiFi
     - WiFiClient
     - ThingSpeak
   - Include these libraries in your sketch.

3. *Configuration:*
   - Replace the placeholders in the code with your actual credentials:
     - myWriteAPIKey: Your ThingSpeak write API key
     - ssid: Your Wi-Fi network name
     - pass: Your Wi-Fi password
     - myChannelNumber: Your ThingSpeak channel number

## Usage
1. Upload the code to your ESP8266 using the Arduino IDE.
2. Open the Serial Monitor to view the status messages and product levels.
3. The system will continuously measure the stock levels of Product 1 and Product 2 and update ThingSpeak with the latest data.

## Code Summary
- *Product1()*: Measures the stock level of Product 1 using the ultrasonic sensor and updates ThingSpeak.
- *Product2()*: Measures the stock level of Product 2 using the ultrasonic sensor and updates ThingSpeak.

## Notes
- Ensure the ultrasonic sensors are properly calibrated for accurate measurements.
- The system updates the stock levels based on predefined distance thresholds.
- For remote monitoring, check the ThingSpeak dashboard associated with your channel.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
