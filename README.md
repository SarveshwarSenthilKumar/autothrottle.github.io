# Auto-Throttle Control System

A project that demonstrates computer-controlled throttle pedal actuation using an Arduino, servo motor, and web interface.

## Project Overview

This project involves controlling a vehicle's throttle pedal using computer inputs. The system replaces the traditional spring-loaded pedal mechanism with a servo motor controlled by an Arduino, which is then managed through a web-based interface.

## Features

- Computer-controlled throttle actuation
- Web-based control interface
- Real-time throttle position feedback
- Timeline visualization of project development
- Responsive design that works on various screen sizes

## Hardware Components

- Arduino board (compatible with Firmata)
- Servo motor (suitable for throttle actuation)
- Throttle pedal assembly
- Jumper wires and necessary connectors
- USB cable for Arduino communication

## Software Dependencies

- Arduino IDE
- Python 3.x
- Flask web framework
- PyFirmata library
- StandardFirmata firmware (for Arduino)

## Project Structure

- `index.html` - Main web interface
- Backend Python scripts (linked in the project timeline)

## Getting Started

1. Upload the StandardFirmata sketch to your Arduino using the Arduino IDE
2. Connect the servo motor to the Arduino as per the wiring diagram
3. Install the required Python packages:
   ```
   pip install flask pyfirmata
   ```
4. Run the Python backend server
5. Open the web interface in a browser

## Project Timeline

The development of this project was documented with key milestones:
- October 28, 2024: Project introduction and requirements gathering
- [Additional milestones documented in the web interface]

## Codebase

The project code is organized across multiple repositories:
- [Firmata Library](https://github.com/firmata/arduino#firmata-client-libraries)
- [Arduino Connection Setup (Firmata)](https://github.com/firmata/arduino/blob/main/examples/StandardFirmata/StandardFirmata.ino)
- [Constant Motor Oscillation Code](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/blob/main/oscillatingMotor.ino)

## Gallery

[Project showcase and demonstration images are available in the web interface]

## Team

- AutoThrottle

Contributors:
- Sarveshwar Senthil Kumar
- Marcus Moorlag-Lotz
- Bao Khanh Phan
- Sudeys Said

## Acknowledgments

- Thanks to the Arduino and Firmata communities for their open-source contributions
- [Any other acknowledgments]
