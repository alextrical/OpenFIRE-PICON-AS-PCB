# OpenFIRE-PICON-AS-PCB

This repository contains the hardware design files for a PCB implementation of the OpenFIRE ESP32 firmware project:
https://github.com/alessandro-satanassi/OpenFIRE-Firmware-ESP32
It provides a reproducible, manufacturable circuit design to simplify building OpenFIRE-compatible hardware without relying on point-to-point wiring or prototyping boards.
Overview
The goal of this repository is to:
	•	Provide a clean, documented PCB design for OpenFIRE
	•	Reduce assembly complexity and wiring errors
	•	Enable repeatable manufacturing (JLCPCB / PCBWay / in-house CNC)
	•	Offer a base for further hardware customisation
This is a companion hardware project — firmware development and updates remain in the upstream OpenFIRE repository.
Features
	•	ESP32-based design (module footprint configurable depending on variant)
	•	Integrated support for OpenFIRE input/output peripherals
	•	Clearly separated power, logic, and I/O domains
	•	Designed with manufacturability in mind (2-layer, standard stackup)
	•	Compatible with common assembly workflows (hand assembly or PCBA)
Repository Structure
	•	 /kicad  — KiCAD project files (schematic, PCB, libraries)
	•	 /manufacturing  — Gerbers, drill files, pick-and-place, BOM
	•	 /docs  — Documentation, wiring diagrams, and notes
	•	 /images  — Renders and board previews
Hardware Design
The PCB is designed in KiCAD and follows standard open hardware practices:
	•	Fully annotated schematic with consistent net naming
	•	Library components aligned with LCSC/JLCPCB where possible
	•	DRC-clean layout with attention to grounding and routing integrity
	•	Designed for straightforward panelisation or isolation milling
Manufacturing
JLCPCB / PCBWay
Manufacturing files are provided in  /manufacturing :
	•	Gerber files
	•	Drill files
	•	Pick-and-place (if applicable)
	•	BOM (LCSC-aligned where possible)
Typical fabrication settings:
	•	Layers: 2
	•	Thickness: 1.6 mm
	•	Copper: 1 oz
	•	Finish: HASL or ENIG
CNC / Isolation Milling
The design is also suitable for CNC workflows:
	•	Trace clearances chosen to be isolation-mill friendly
	•	Single-sided variants may be possible depending on configuration
	•	Export from KiCAD using standard CAM workflows
Assembly
Assembly depends on the selected configuration, but generally includes:
	•	ESP32 module
	•	Passive components (resistors, capacitors)
	•	Connectors for OpenFIRE peripherals
	•	Optional regulators or power circuitry
Refer to  /docs  for assembly notes and pin mappings.
Firmware
This board is designed to work with:
https://github.com/alessandro-satanassi/OpenFIRE-Firmware-ESP32
Follow the firmware repository instructions for:
	•	Flashing the ESP32
	•	Configuration
	•	Calibration
Status
	•	Hardware: In development / prototype (update as needed)
	•	Tested: (add revision notes here)
	•	Known issues: (track errata here)
Contributing
Contributions are welcome, especially:
	•	PCB layout improvements
	•	Alternate form factors
	•	BOM optimisation (cost or availability)
	•	Additional peripheral support
Please open an issue or submit a pull request.
License
Specify your preferred open hardware license here (e.g. CERN-OHL-S, MIT for design files, etc.).
Notes
This project is not affiliated with the original OpenFIRE firmware repository but is designed to complement it.