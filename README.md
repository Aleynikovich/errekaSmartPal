# Erreka SmartPal

A KUKA robot programming repository for the Erreka SmartPal robotic palletizing system.

## Overview

This repository contains KUKA Robot Language (KRL) programs for automated palletizing operations. The system is designed to handle various manufacturing and material handling tasks, including multi-lathe operations and conveyor belt integration.

## System Information

- **Robot Name**: 848663
- **IR Serial Number**: 848663
- **KUKA Version**: V4.1.7 SP08
- **Archive Date**: 2025-05-22

## Repository Structure

```
.
├── KRC/                    # KUKA Robot Control directory
│   ├── R1/                # Robot 1 programs and configuration
│   │   ├── Program/       # Main program directory
│   │   │   ├── GENERALES/           # General utility programs
│   │   │   ├── Programas2Tornos/    # Two-lathe programs
│   │   │   ├── CINTA/               # Conveyor belt programs
│   │   │   └── ViejosEnCaballete/   # Legacy programs
│   │   ├── Mada/          # Machine data
│   │   ├── System/        # System files
│   │   └── TP/            # Teach pendant programs
│   └── STEU/              # Control system files
├── C/                     # System C drive backup
└── am.ini                 # Archive metadata
```

## Programs

### General Utilities (`GENERALES/`)
- **paro**: Emergency stop and brake control
- **mos_mens**: Message display system
- **delmens**: Message deletion utility

### Two-Lathe Programs (`Programas2Tornos/`)
- **paletizado860**: Palletizing program for 860 pattern
- **paletizadoM90x695**: Palletizing program for M90x695 dimensions
- **m72x860**: M72 x 860 dimensions handling
- **cnc5916**: CNC control interface
- **pat62_65** / **pat65_62**: Pattern switching programs between positions 62-65
- **patron**: Master pattern program
- **patron_2a_atada**: Secondary tied pattern

### Conveyor Belt Programs (`CINTA/`)
- **cinta**: Conveyor belt control and integration

### Main Programs
- **programa_patr**: Master pattern program with full initialization

## File Types

- **`.src`**: Source code files (KUKA Robot Language)
- **`.dat`**: Data files containing variables and configurations
- **`.upg`**: Upgrade/configuration files
- **`.$*.dat`**: System-generated data files

## Getting Started

### Prerequisites
- KUKA KRC4 controller or compatible system
- KUKA WorkVisual (for offline programming)
- Access to the robot controller network

### Installation
1. Clone this repository or download the archive
2. Use KUKA WorkVisual to import the project
3. Transfer programs to the robot controller using KRL transfer tools
4. Verify machine data matches your robot configuration

### Usage
1. Load the desired program from the teach pendant
2. Verify all safety systems are active
3. Test in manual mode (T1) before automatic operation
4. Switch to automatic mode (T2/EXT) for production

## Safety Notes

⚠️ **Important Safety Information**:
- Always test programs in T1 mode first
- Verify workspace is clear before automatic operation
- Ensure all emergency stop buttons are functional
- Follow all KUKA safety guidelines and local regulations
- This code controls industrial robots - improper use can cause injury or death

## Development

### Program Structure
All KRL programs follow the standard KUKA structure:
- Initialization section with interrupt declarations
- Main program logic
- Fold sections for code organization
- Data files for parameters and configurations

### Modifications
When modifying programs:
1. Create backups of existing programs
2. Test changes in simulation or T1 mode
3. Document changes in the program header
4. Verify all related .dat files are updated

## Contributing

When contributing to this repository:
1. Follow KUKA KRL coding standards
2. Test all changes thoroughly in simulation
3. Document program changes
4. Update relevant .dat files
5. Create meaningful commit messages

## License

Please ensure compliance with KUKA licensing agreements and your organization's policies regarding robot programming.

## Contact

For questions or issues related to this robot system, please contact the system administrator or integrator.

---

**Note**: This repository contains industrial robot control programs. Only qualified personnel should modify or deploy these programs.
