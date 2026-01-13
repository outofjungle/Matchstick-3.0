# Matchstick 3.0

An IoT-enabled control interface module based on the M5Stack StampS3, designed for industrial control and monitoring applications.

## Overview

Matchstick 3.0 is a compact PCB that combines WiFi/Bluetooth connectivity with signal buffering capabilities, making it ideal for interfacing modern microcontrollers with legacy or mixed-voltage industrial equipment.

## Features

- **WiFi/Bluetooth Connectivity** via M5StampS3 module
- **Signal Level Translation** using 74HCT125D quad buffer ICs
- **8-pin Screw Terminal Block** for external device connections
- **Power Management** with barrel jack input (5V) and robust filtering
- **Status Indicators** including LED and control button
- **Compact 2-Layer PCB** design (1.6mm thickness)
- **Mounting Holes** (3.5mm) for secure installation

## Hardware Specifications

### Compatibility

**IMPORTANT**: This board is designed specifically for the **M5StampS3** module only. It is **not compatible** with other M5Stack modules (M5Stamp, M5StampC3, M5Atom, etc.) due to specific pinout and footprint requirements.

### Main Components

| Component | Part Number | Description |
|-----------|-------------|-------------|
| U3 | M5StampS3 | M5Stack StampS3 module (REQUIRED - not compatible with other M5Stack modules) |
| U2 | 74HCT125D | Quad buffer/line driver (SOIC-14) |
| J3 | Barrel Jack | 5V power input connector |
| J4 | 8-pin Terminal | Screw terminal block for I/O connections |
| C1 | 0.1µF (0805) | Decoupling capacitor |
| C2 | 1000µF | Power supply bulk capacitor |
| R1 | 330Ω (0805) | LED current limiting resistor |
| D1 | LED (0805) | Status indicator |
| SW1 | COM-08720 | Control/reset switch |

### PCB Specifications

- **Layers**: 2 (Front and Back copper)
- **Thickness**: 1.6mm
- **Copper Weight**: 0.035mm (1 oz)
- **Material**: FR4
- **Surface Mount**: 0805 package for passives
- **Mounting**: 2x 3.5mm mounting holes

### Electrical Characteristics

- **Input Voltage**: 5V DC (via barrel jack)
- **Logic Levels**: 3.3V (M5StampS3) with 5V tolerant buffered I/O
- **Power Filtering**: 1000µF bulk capacitance + 0.1µF decoupling

## Project Structure

```
Matchstick 3.0/
├── Matchstick 3.0.kicad_pro    # KiCad project file
├── Matchstick 3.0.kicad_sch    # Schematic design
├── Matchstick 3.0.kicad_pcb    # PCB layout
├── Matchstick 3.0.kicad_prl    # Project local settings
├── Matchstick 3.0-backups/     # Automatic KiCad backups
└── README.md                   # This file
```

## Requirements

### Hardware

- **M5StampS3 module** (required - this board only supports M5StampS3, not other M5Stack modules)
- See component table above for complete BOM

### Software

- **KiCad 9.0** or later
- Custom libraries used:
  - `74xx_custom` - Custom 74-series logic definitions
  - `M5Stack_SMD` - M5Stack component footprints
  - `Connector_Custom` - Custom connector designs

## Getting Started

### Opening the Project

1. Install KiCad 9.0 or later
2. Clone this repository
3. Open `Matchstick 3.0.kicad_pro` in KiCad

### Viewing the Design

- **Schematic Editor**: Open the `.kicad_sch` file to view circuit connections
- **PCB Editor**: Open the `.kicad_pcb` file to view the physical layout
- **3D Viewer**: Use KiCad's 3D viewer to visualize the assembled board

### Manufacturing

The design is production-ready with all components marked for assembly (DNP = No). Standard PCB fabrication settings:

- 2-layer PCB, 1.6mm thickness
- HASL or ENIG finish recommended
- Minimum trace/space: Standard (6/6 mil or better)
- SMD assembly required for 0805 components and ICs

## Use Cases

- Industrial equipment monitoring and control
- IoT gateway for legacy systems
- WiFi-enabled sensor interfaces
- Remote monitoring applications
- Educational embedded systems projects

## Development Status

- **Current Version**: 9.0
- **Status**: Design complete, ready for fabrication
- **Last Updated**: January 2024 (KiCad 9.0 compatibility)

## Version History

- **v9.0** - Updated for KiCad 9.0 compatibility
- Earlier versions preserved in backup archives

## License

MIT License

Copyright (c) 2024 Matchstick 3.0

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Contributing

[Add contribution guidelines if applicable]

## Contact

[Add contact information here]

---

**Note**: This is a hardware design project. Ensure you have the necessary skills and tools for PCB assembly and embedded systems programming before attempting to build this project.
