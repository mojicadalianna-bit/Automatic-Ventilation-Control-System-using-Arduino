# Automatic Ventilation Control System using Arduino

## Abstract
This project presents an intelligent ventilation control system implemented with Arduino. The system automatically activates a fan based on three independent conditions: motion detection using a PIR sensor, temperature monitoring using a DS18B20 sensor, and a programmable schedule using a DS3231 Real-Time Clock (RTC). The project includes circuit design, simulation in Tinkercad, and Arduino code, providing a practical example of embedded systems for environmental control.

## Introduction
Efficient environmental control is essential for comfort and energy savings. Traditional ventilation systems rely on manual operation, which can be inefficient and inconvenient. This project demonstrates the development of an automated system capable of responding to environmental and temporal conditions. Using Arduino as the central controller, the system integrates sensors and a relay module to intelligently manage fan operation. The implementation showcases fundamental principles of embedded systems, sensor integration, and real-time scheduling using a RTC module.

## Objectives
- Implement automatic fan control using Arduino.
- Integrate motion and temperature sensors (PIR and DS18B20).
- Use DS3231 RTC for scheduled operation.
- Simulate and test the circuit in Tinkercad.
- Document the project for future improvements.
- Provide a clear reference for future developers or students.

## Components
- Arduino Uno R3
- PIR motion sensor
- DS18B20 temperature sensor
- DS3231 Real-Time Clock (RTC)
- Relay module
- EZ Chill box fan with a dial
- LCD Display
- Wires, breadboard

## Circuit Design and Explanation
The circuit consists of an Arduino Uno R3 microcontroller connected to the following components:
- **PIR Motion Sensor:** Detects human presence and triggers the fan.
- **DS18B20 Temperature Sensor:** Measures ambient temperature and activates the fan when a predefined threshold is exceeded.
- **DS3231 RTC Module:** Provides real-time clock functionality to allow scheduled fan operation.
- **Relay Module:** Controls the on/off state of the fan based on signals from Arduino.
- **LCD Display:** It displays real-time information, including the time, date, and temperature.

The system works by continuously monitoring sensor inputs and comparing them with predefined conditions. If any condition is met, the relay switches the fan on; otherwise, it remains off. The LCD provides feedback for easier monitoring and debugging.

## How It Works
1. The Arduino continuously reads the PIR and DS18B20 sensor values.
2. If motion is detected, the system immediately turns on the fan.
3. If the temperature exceeds the set threshold, the fan is activated.
4. The DS3231 RTC checks if the current time is within the programmed schedule and turns the fan on/off accordingly.
5. LCD display updates every second, showing current time, date and temperature.
6. The system prioritizes safety and avoids simultaneous conflicting signals.

- Add a menu system on the LCD to adjust time, temperature threshold, or schedules directly from the hardware.
- Implement data logging (temperature, motion, fan activation) using the AT24C32 memory or SD-card module.
- Add hysteresis control to prevent the fan from turning on/off repeatedly around the threshold temperature.
- Develop a WiFi or Bluetooth version using ESP32 or HC-05 to control and monitor the system remotely.
- Optimize power consumption by using sleep modes when no motion is detected.

## References
- Arduino Official Documentation: [https://www.arduino.cc](https://www.arduino.cc)
- Tinkercad Circuits: [https://www.tinkercad.com/circuits](https://www.tinkercad.com/circuits)
- DS18B20 Sensor Guide: [https://www.maximintegrated.com/en/products/analog/sensors-and-sensor-interface/DS18B20.html](https://www.maximintegrated.com/en/products/analog/sensors-and-sensor-interface/DS18B20.html)
- DS3231 RTC Module Guide: [https://www.maximintegrated.com/en/products/analog/sensors-and-sensor-interface/DS3231.html](https://www.maximintegrated.com/en/products/analog/sensors-and-sensor-interface/DS3231.html)
