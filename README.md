# Smart Home Automation using ESP32 & Blynk

## Introduction
This project demonstrates an IoT-based home automation system using the ESP32 microcontroller and the Blynk IoT platform. The system allows users to remotely control home appliances such as lights from anywhere using a smartphone.

The ESP32 connects to Wi-Fi and communicates with the Blynk Cloud server. When a button is pressed in the Blynk app, a signal is sent to the ESP32, which controls a relay module to switch the connected appliance ON or OFF.

## Components Required
- ESP32 Development Board
- 5V Relay Module
- Bulb with Holder
- Breadboard
- Jumper Wires
- 5V Power Supply
- Wi-Fi Connection
- Smartphone with Blynk IoT App



## Connections

### Relay to ESP32
- Relay VCC → ESP32 VIN (5V)
- Relay GND → ESP32 GND
- Relay IN → ESP32 GPIO 23

### Bulb to Relay
- Live wire → COM terminal of relay
- NO (Normally Open) → One terminal of bulb
- Other bulb terminal → Neutral


## Working

1. ESP32 connects to Wi-Fi.
2. ESP32 connects to Blynk Cloud using Auth Token.
3. User presses the button in Blynk mobile app.
4. Blynk sends command to ESP32 via Virtual Pin (V0).
5. ESP32 sets GPIO HIGH or LOW.
6. Relay switches ON/OFF.
7. Light turns ON/OFF accordingly.



  Blynk.run();
}
