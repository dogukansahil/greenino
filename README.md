# GreenIno: Wireless Sensor Network Project with Atmel ATmega328P

## Introduction
GreenIno is a compact and energy-efficient wireless sensor network project designed to monitor various environmental parameters in the face of climate change. The system comprises two devices: one that transmits an array of sensor data and another that displays this data on a custom circuit.

## Components
- 9V Battery (For the transmitter)
- Atmel ATmega328P (For the transmitter)
- 7805 Voltage Regulator + 0.33µF Capacitor + 0.1µF Capacitor (For the transmitter)
- LM1117T 3.3V Voltage Regulator + 10µF Capacitor + 22µF Capacitor (For the transmitter)
- BMP180 Temperature and Pressure Sensor (For the transmitter)
- MQ135 Gas Sensor (For the transmitter)
- SSD1306 OLED Screen (For the transmitter)
- NRF24L01 + PA + LNA SMA Anten 2.4GHz Wireless Module (For both receiver and transmitter)
- Arduino Nano (For the receiver)
- LED (It will be attached to the antenna for the receiver)

## Step by Step Project

### 1. Initial Idea
The project started with the aim of wirelessly monitoring environmental parameters such as temperature, pressure, and gas concentration.

### 2. Energy Efficiency and Compact Design
To achieve energy savings and a more compact design, an Atmel ATmega328P microcontroller was used instead of a full-sized Arduino board for the receiver.

### 3. Wireless Communication
Wireless communication between the devices was established using NRF24L01 + PA + LNA SMA Anten 2.4GHz modules.

### 4. Integration of Sensors
Environmental parameters such as temperature and pressure were measured using the BMP180 sensor, while gas concentrations were captured with the MQ135 sensor.

### 5. Power Supply
The transmitter device was powered by a 9V battery for portability. A 7805 voltage regulator was integrated to drop the voltage from 9V to 5V, and an LM1117T regulator was used to further drop the voltage from 5V to 3.3V, providing suitable power supply for the different components of the device.

### 6. Data Logging
Real-time data logging was a crucial aspect of the project. CoolTerm, a versatile tool, was utilized for real-time data capture directly to a computer. Its user-friendly interface and robust features ensured a seamless data logging experience.

## Conclusion
GreenIno offers an energy-efficient, compact, and portable solution for environmental monitoring. The wireless technology enables data gathered at one point to be wirelessly received and processed at another location. It provides an ideal solution for monitoring environmental parameters at home, in the office, or any given location.

## Pin Outs
### Transmitter

#### BMP180 and MQ135 with ATmega328P (or Arduino Uno)
- VCC (for both sensors) -> 3.3V
- GND (for both sensors) -> GND
- SDA (for BMP180) -> A4 (I2C SDA pin for ATmega328P)
- SCL (for BMP180) -> A5 (I2C SCL pin for ATmega328P)
- A0 (for MQ135) -> A0 (Analog input)

#### NRF24L01+ with ATmega328P (or Arduino Uno)
- GND -> GND
- VCC -> 3.3V (Important! The module should not be powered by 5V)
- CE -> D9
- CSN/CS -> D10
- SCK -> D13
- MOSI -> D11
- MISO -> D12

#### SSD1306 OLED Display with ATmega328P (or Arduino Uno)
- VCC -> 5V
- GND -> GND
- SDA -> A4
- SCL -> A5

### Receiver

#### ATmega328P with NRF24L01+
- GND -> GND
- VCC -> 3.3V (Important! The module should not be powered by 5V)
- CE -> D9
- CSN/CS -> D10
- SCK -> D13
- MOSI -> D11
- MISO -> D12

#### LED
- Anode (+) -> D8
- Cathode (-) -> GND

For more details and instructions on setting up the GreenIno project, please refer to the corresponding source code and documentation. Happy monitoring!

Licence: https://dogukansahil.dev/blog.php?id=8
