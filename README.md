# MM-Power-Module

This repository contains the complete design files, documentation, and output artifacts of the Power Subsystem used in a micro-mouse robot. It includes USB-C power negotiation, multi-rail regulation, Li-ion battery support, and load switching for motors and auxiliary peripherals

#### Repository Contents
| Folder/File      | Description                                                                    |
| ---------------- | ------------------------------------------------------------------------------ |
| `kicad_project/` | Full KiCad 8+ project files (`.kicad_sch`, `.kicad_pcb`, symbols, footprints). |
| `gerber/`        | Gerber files for PCB manufacturing (RS-274X standa.                         |
| `bom/`           | Bill of Materials in `.csv` and `.xlsx` formats.                               |
| `csv_exports/`   | CSV exports of netlist, components, positions for assembly.                    |
| `images/`        | High-res renderings of the board (3D view, top view, bottom view).             |
| `README.md`      | You're reading it.                                                             |

## Subsystem Overview
The power subsystem fulfills the following requirements:
- Provide 5V and 3V3 regulated rails to sensors, MCU, and logic.
- Interface with USB-C input and negotiate 9V via CH224K.
- Support auxiliary laods via two TPS22929D load switches.
- Power four DC motors via DRV8833 motor drivers.

#### Key Components
| Component      | Function                          |
| -------------- | --------------------------------- |
| CH224K         | USB-C PD negotiation (9 V out)    |
| LM296T-5       | 5 V linear regulator              |
| AMS1117-3.3    | 3.3 V LDO regulator               |
| TP4056         | Li-ion charger (w/ protection)    |
| DRV8833        | Dual H-bridge motor drivers       |
| TPS22929D      | Load switches for aux peripherals |
| INA219         | Current sensing (I²C telemetry)   |

#### Board Previews

## License
This project is released under the MIT License. Attribution is appreciated if reused or modified.
