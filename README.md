# Auto-Throttle Control System

A project that demonstrates computer-controlled throttle pedal actuation using an Arduino, servo motor, and web interface.

## Project Overview

This project involves controlling a vehicle's throttle pedal using computer inputs. The system replaces the traditional spring-loaded pedal mechanism with a servo motor controlled by an Arduino, which is then managed through a web-based interface. The project was developed by a team of Grade 11 Computer Engineering students working with a 2009 Nissan Sentra.

## Features

- Computer-controlled throttle actuation
- Web-based control interface with command-line style commands
- Real-time throttle position feedback
- Timeline visualization of project development
- Responsive design that works on various screen sizes
- Interactive image and video galleries showcasing project progress

## Hardware Components

- Arduino board (compatible with Firmata)
- Servo motor (suitable for throttle actuation)
- Throttle pedal assembly (modified with servo attachment)
- Jumper wires and necessary connectors
- USB cable for Arduino communication
- Gears for mechanical advantage (small gear on motor, large gear on pedal)

## Software Dependencies

- Arduino IDE
- Python 3.x
- Flask web framework
- PyFirmata library
- StandardFirmata firmware (for Arduino)

## Project Structure

```
autothrottle.github.io/
├── README.md                          # This file - project documentation
├── index.html                         # Main web interface with timeline and galleries
├── media-links.md                     # Extracted list of all media links (images, videos, repos)
└── media-downloads/                  # Downloaded media assets
    ├── download-summary.md            # Summary of downloaded files
    ├── images/                        # 15 project images (schematics, diagrams, photos)
    │   ├── 01-schematic-accelerator-pedal.jpg
    │   ├── 02-wiring-diagram-throttle-ecu.jpg
    │   ├── 03-electronic-throttle-control-diagram.jpg
    │   ├── 04-uncaptioned-image.jpg
    │   ├── 05-arduino.jpg
    │   ├── 06-fuse-box-diagram.jpg
    │   ├── 07-obd2-throttle-readings.jpg
    │   ├── 08-car-details.jpg
    │   ├── 09-original-pedal-housing.jpg
    │   ├── 10-auto-throttle-vs-regular.jpg
    │   ├── 11-close-up-auto-throttle.jpg
    │   ├── 12-engine-compartment.jpg
    │   ├── 13-auto-throttle-on-car.jpg
    │   ├── 14-auto-throttle-webapp-ui.png
    │   └── 15-team-picture.jpg
    └── videos/                        # 4 project videos (MP4 format)
        ├── nissan_sentra_normal_revs_v1 (2160p).mp4
        ├── jingle_bells_attempt_v1 (720p).mp4
        ├── finished_project_overview_v1 (2160p).mp4
        └── code_walkthrough_v1 (2160p).mp4
```

## Getting Started

1. Upload the StandardFirmata sketch to your Arduino using the Arduino IDE
2. Connect the servo motor to the Arduino as per the wiring diagram
3. Install the required Python packages:
   ```
   pip install flask pyfirmata
   ```
4. Run the Python backend server (see backend codebase links below)
5. Open the web interface (index.html) in a browser

## Webapp Commands

The Auto-Throttle webapp supports the following commands:

- `rev x` - Revs the car for x seconds at full throttle (e.g., "rev 2")
- `sleep x` - Stops the program momentarily for x seconds (e.g., "sleep 1")
- `angletest x-y` - Revs to angle x for y seconds (e.g., "angletest 60-2")
- `reset x` - Resets throttle position back to 0 degrees and sleeps for x seconds (e.g., "reset 2")

## Project Timeline

The development of this project was documented with key milestones:

- **October 28, 2024**: Project introduction and requirements gathering from Mr. Andrade
- **November 11, 2024**: Two weeks spent evaluating the vehicle (2009 Nissan Sentra) and logistics
- **November 25, 2024**: Research phase working through OBD2 Port and testing diagnostic software (Car Scanner ELM OBD2, EcuFlash, MaxxECU MTune, ScanXL)
- **December 15, 2024**: Shifted approach from OBD2 to direct throttle signal manipulation via pigtail connector (ultimately unsuccessful due to proprietary Nissan pins)
- **January 15, 2025**: Pivoted to mechanical solution using spare throttle pedal with servo motor and Arduino
- **Final Phase**: Implemented gear system for mechanical advantage, developed Python Flask webapp with PyFirmata for throttle control

*Full timeline with details available in index.html*

## Codebase

The project code is organized across multiple repositories:

### Core Libraries
- [Firmata Library](https://github.com/firmata/arduino#firmata-client-libraries) - Arduino communication protocol
- [Arduino Connection Setup (Firmata)](https://github.com/firmata/arduino/blob/main/examples/StandardFirmata/StandardFirmata.ino) - StandardFirmata firmware

### Backend Codebase
- [Constant Motor Oscillation Code (Arduino)](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/blob/main/oscillatingMotor.ino) - Arduino C++ code
- [Constant Motor Oscillation Code (Python)](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/blob/main/alwaysSpin.py) - Python implementation
- [Manual Motor Adjustment Code (Python)](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/blob/main/motor.py) - Manual control script
- [Auto-Throttle Control Webapp Front-End](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/tree/main/templates) - HTML & CSS templates
- [Auto-Throttle Control Webapp Back-End](https://github.com/SarveshwarSenthilKumar/Auto-Throttle-Backend-Codebase/blob/main/app.py) - Flask Python backend

### Software Tools Tested
- [Car Scanner ELM OBD2](https://www.carscanner.info) - OBD2 diagnostic tool
- [EcuFlash](http://www.openecu.org/index.php?title=EcuFlash) - ECU programming software
- [MaxxECU MTune](https://www.maxxecu.com/mtune) - ECU tuning software
- [ScanXL](https://www.palmerperformance.com/products/scanxlstd/index.php) - OBD2 scanning software

## Gallery

### Images
All project images are available in the `media-downloads/images/` folder and include:
- Schematics of accelerator pedal position sensor
- Wiring diagrams from throttle to ECU
- Electronic throttle control diagrams
- Arduino setup photos
- Fuse box diagrams
- OBD2 throttle position readings
- Car details and documentation
- Original pedal housing
- Auto-throttle vs regular throttle comparison
- Close-up images of the auto-throttle system
- Engine compartment photos
- Auto-throttle installed on vehicle
- Webapp UI screenshots
- Team photo

### Videos
All project videos are available in the `media-downloads/videos/` folder:
- Nissan Sentra Normal Revs (2160p)
- Jingle Bells Attempt (720p)
- Finished Project Overview (2160p)
- Code Walkthrough (2160p)

*See [media-links.md](media-links.md) for a complete list of all media links*

## Future Plans

- Custom design and manufacture a sleek housing enclosure for the project
- Fine-tune the UI to make it more user friendly
- Add a feature for manual adjustment of throttle pedal rotation degrees
- Motorize the brake pedal
- Motorize the gear selector
- Add system of cameras to view around the vehicle
- Develop codebase to control brake, gear, and throttle in accordance with cameras for autonomous driving

## Team

**Project Name:** AutoThrottle (aka "Throttle House")

### Contributors
- Sarveshwar Senthil Kumar
- Marcus Moorlag-Lotz
- Bao Khanh Phan
- Sudeys Said

### Course
Grade 11 Computer Engineering Class

## Acknowledgments

- Thanks to the Arduino and Firmata communities for their open-source contributions
- Mr. Andrade for project guidance and requirements
- Nissan dealerships and OEM dealers for technical feedback (15+ dealers consulted)
