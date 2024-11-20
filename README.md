
# Project: Raspberry Pi DC Motor Control with L298N Driver

## Description

This project demonstrates how to control a DC motor using a Raspberry Pi, an L298N motor driver, and Python. The L298N driver allows you to drive high-power motors with your Raspberry Pi, making it an ideal choice for various robotic and motor control applications.

In this setup, we will rotate a DC motor at a constant speed using the L298N motor driver. The Raspberry Pi will handle the logic for controlling the motor's rotation direction and speed using Python scripts.

## Components Used

- Raspberry Pi (any model, e.g. Raspberry Pi 3/4/Zero)
- L298N Motor Driver Module
- DC Motor
- Jumper wires (male-to-male, male-to-female)
- Power supply (e.g. 12V DC battery pack)
- Breadboard

## Circuit Diagram

### Breadboard Connections

1. **Raspberry Pi GPIO Pins to L298N Motor Driver:**
   - **Raspberry Pi GPIO Pin 5 (Ground) to L298N VSS**
   - **Raspberry Pi GPIO Pin 3.3V to L298N VCC**
   - **Raspberry Pi GPIO Pin 17 (GPIO17) to L298N IN1**
   - **Raspberry Pi GPIO Pin 18 (GPIO18) to L298N IN2**
   - **Raspberry Pi GPIO Pin 27 (GPIO27) to L298N IN3**
   - **Raspberry Pi GPIO Pin 22 (GPIO22) to L298N IN4**
   - **Motor’s positive terminal (+) connected to VCC pin on L298N**
   - **Motor’s negative terminal (-) connected to one of the output terminals (e.g. Motor 1)**
   - **Motor GND connected to the ground rail on the breadboard**

### Power Supply Connections

- **12V power supply connects to L298N VSS pin**
- **Motor ground connects to breadboard ground rail**
- **The power supply's positive terminal connects to motor positive terminal (e.g. Motor 1)**

## Python Code

### Main Script: `motor_control.py`



### Installation and Setup

1. **Install RPi.GPIO Python Library:**
   ```bash
   pip install RPi.GPIO
   ```

2. **Ensure GPIO pins are enabled on your Raspberry Pi:**
   - Open the terminal and run `sudo raspi-config`
   - Navigate to `Interfacing Options`
   - Enable `GPIO`
   - Reboot your Raspberry Pi

3. **Power your motor circuit:**
   - Connect a 12V battery pack to the VSS pin on the L298N motor driver.
   - Ensure your Raspberry Pi is powered on via micro-USB.

## Running the Code

1. Make sure the above circuit diagram and connections are correctly made.
2. Open your terminal on the Raspberry Pi.
3. Navigate to the folder where `motor_control.py` is located.
4. Run the Python script:
   ```bash
   python motor_control.py
   ```
5. You should see the motor rotate at a constant speed for 10 seconds as per the script's configuration.

## Troubleshooting

- **Motor does not rotate:** 
  - Check the power connections and battery voltage.
  - Verify all connections are properly made.
  - Ensure GPIO pins are correctly configured in the Python script.

- **Motor runs erratically:** 
  - Check wiring.
  - Confirm the power supply to the L298N is stable.
  - Try different PWM speeds.

## Notes

- **Safety Precautions:** 
  - Ensure to use appropriate current ratings for the motors.
  - Double-check all connections before powering the circuit.
  - Don’t touch the circuit while it’s powered to prevent electrical shock.
