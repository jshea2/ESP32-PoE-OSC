# StageMod

Send OSC messages from sensors.. 

Uses Olimex-ESP32-PoE Microcontroller and a web app for updateing configurations

Use ESP32-PoE with sensor to send OSC filtered by Touchdesigner.


https://github.com/user-attachments/assets/ff4cd534-56c4-4b7e-a54d-fffd37521076



## Hardware Requirements:
- [ESP32-PoE-ISO](https://www.digikey.com/en/products/detail/olimex-ltd/ESP32-POE-ISO/10258716)
- [Sensor Example](https://www.amazon.com/HiLetgo-TTP223B-Capacitive-Digital-Raspberry/dp/B00HFQEFWQ/ref=sr_1_1_sspa)
- [PoE Switch or Injector](https://www.amazon.com/Injector-Compliant-Compatible-TL-POE150S-TPE-113GI/dp/B09BFBM6PQ/ref=sr_1_9)
- [Breadboard Jumper Wire](https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/)

## Setup:

- Download repo and flash ESP32-PoE-ISO with file

<img width="400" height="690" alt="Screenshot 2026-01-26 at 8 51 30 PM" src="https://github.com/user-attachments/assets/e934f9db-e3cc-465f-af28-504c3eafb878" />


- Configure all settings

- Connect computer to ESP32-PoE-ISO via PoE network
- Open [Touchdesigner project]([url](https://github.com/jshea2/conductive_sensor/releases/tag/1.0))
  - It should read "Online" if connected. This knows its online because the ESP32-PoE sends a "/*/ping" to check heartbeat.

Features:
- Touchdesigner UI
- Online / Offline indicator
- Feild for amount of time for cooldown state. This is incase the sensor is triggered too quickly. 
- It also shows an indicator everytime it is touched
- "Test" button is included to test trigger without ESP32-PoE online
- Feilds to edit ping and sensor trigger OSC address
- OSC Out Client configure
  - IP, Port, OSC Address & Argument

## Credits:

Original project is by [Facing Tomorrow](https://github.com/facingtomorrow). This repository added OSC support and other TD UI components.
