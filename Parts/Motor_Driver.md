Certainly! Below is a comprehensive Markdown document detailing the functional and technical specifications of the **DAOKI L298N Dual H-Bridge Motor Driver Module**, incorporating information from the official L298 datasheet.

---

# DAOKI L298N Dual H-Bridge Motor Driver Module

## Overview

The DAOKI L298N Dual H-Bridge Motor Driver Module is a robust and versatile component designed to control the speed and direction of two DC motors or a single stepper motor. It integrates the STMicroelectronics L298N chip, allowing for high-current and high-voltage motor control in various applications.

## Functional Features

- **Motor Control**: Controls two DC motors or one stepper motor
- **Control Modes**: Supports direction and speed control via PWM
- **Voltage Regulator**: Onboard 78M05 5V regulator
- **LED Indicators**: Power-on LED indicator
- **Heat Dissipation**: Equipped with a heatsink for improved thermal performance

## Technical Specifications

| Parameter               | Specification                                  |
|-------------------------|------------------------------------------------|
| **Driver Chip**         | L298N Dual H-Bridge
| **Motor Supply Voltage**| 5V to 35V
| **Logic Voltage**       | 5V
| **Motor Drive Current** | Up to 2A per channel
| **Logic Current**       | 0mA to 36mA
| **Maximum Power**       | 25W
| **Operating Temperature**| -25°C to +130°C
| **Dimensions**          | Approximately 43mm x 43mm x 27mm
| **Weight**              | Approximately 26g

## Pinout Details

The following table provides a comprehensive overview of the pinout options for the DAOKI L298N Motor Driver Module:

| Pin Name | Type         | Description                                                                 |
|----------|--------------|-----------------------------------------------------------------------------|
| IN1      | Input        | Controls Motor A direction (with IN2)
| IN2      | Input        | Controls Motor A direction (with IN1)
| IN3      | Input        | Controls Motor B direction (with IN4)
| IN4      | Input        | Controls Motor B direction (with IN3)
| ENA      | Input        | Enables PWM signal for Motor A
| ENB      | Input        | Enables PWM signal for Motor B
| OUT1     | Output       | Motor A output 1
| OUT2     | Output       | Motor A output 2
| OUT3     | Output       | Motor B output 1
| OUT4     | Output       | Motor B output 2
| 12V      | Power Input  | Motor power supply (VMS)
| 5V       | Power Output | 5V output from onboard regulator (when jumper is in place)
| GND      | Power        | Ground connection

**Note**: The onboard 5V regulator (78M05) is enabled when the jumper is placed across the 5V and ENA pins. This allows the module to provide 5V to the logic circuitry. If the motor supply voltage exceeds 12V, it is recommended to remove the jumper and supply 5V directly to the 5V pin to prevent overheating the regulator.

## Electrical Characteristics (from L298 Datasheet)

The L298N chip, at the core of this module, has the following electrical characteristics:

| Parameter                     | Test Conditions                    | Min | Typ | Max | Unit |
|-------------------------------|------------------------------------|-----|-----|-----|------|
| Supply Voltage (VS)           | Operative condition | +2.5 |     | 46 | V    |
| Logic Supply Voltage (VSS)    |                                    | 4.5 | 5 | 7 | V    |
| Quiescent Supply Current (IS) | Ven = H; Vi = L; IL= 0 | 13 |     | 22 | mA   |
| Input Low Voltage (ViL)       | pins 5, 7, 10, 12 |     |     | 1.5 | V    |
| Input High Voltage (ViH)      | pins 5, 7, 10, 12 | 2.3 |     | VSS | V    |
| Peak Output Current (IO)      | Non-repetitive (t = 100 ms) |     |     | 3 | A    |
| Total Power Dissipation (Ptot)| Tcase = 75°C |     |     | 25 | W    |
| Junction Operating Temperature (Top)|                            | -25 |     | 130 | °C   |

*Source: [STMicroelectronics L298 Datasheet](https://www.st.com/resource/en/datasheet/l298.pdf)*

## Applications

- Driving DC motors in robotic applications
- Controlling stepper motors
- Smart car motor control
- DIY electronics projects 