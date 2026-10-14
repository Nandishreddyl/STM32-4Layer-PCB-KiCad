# STM32F103C6T6 — Four-Layer PCB Design Using KiCad

## Project Overview

This project presents the schematic design and four-layer PCB layout of an STM32F103C6T6-based microcontroller board, developed using KiCad.

The board integrates a microcontroller, USB interface, power regulation, clock circuitry, reset and boot configuration, and external connector interfaces. The design workflow includes schematic capture, PCB component placement, copper routing, design-rule checking (DRC), and Gerber generation.

## Project Objectives

- Design a custom STM32-based microcontroller PCB.
- Create and organize the electronic schematic using KiCad.
- Develop a four-layer PCB layout with SMD components.
- Route electrical connections across the available copper layers.
- Generate manufacturing files for PCB fabrication.
- Prepare the design for future hardware prototyping and testing.

## Hardware and Components

| Component | Purpose |
|---|---|
| STM32F103C6T6 | Main microcontroller |
| AMS1117-1.5 | Voltage regulation stage, as labeled in the schematic |
| 16 MHz crystal | External clock source |
| USB Micro-B connector | USB interface and board power input |
| Capacitors | Decoupling and power-supply filtering |
| Resistors | Pull-up, configuration, and current-limiting functions |
| SPDT switch | Hardware configuration |
| Pin headers | External signal and power connections |
| Ferrite bead | Power-line filtering |

*Note: Verify the regulator output voltage and USB power arrangement against the final schematic before fabrication.*

## Design Tools

- **EDA Software:** KiCad
- **Schematic Design:** KiCad Schematic Editor
- **PCB Layout:** KiCad PCB Editor
- **Routing:** KiCad interactive routing and FreeRouting autorouter
- **Design Validation:** KiCad Electrical Rules Checker (ERC) and Design Rules Checker (DRC)
- **Manufacturing Outputs:** Gerber files and drill files

## Four-Layer PCB Stack-Up

The PCB is configured with four copper layers:

| Layer | Intended purpose |
|---|---|
| F.Cu | Component-side routing and signal connections |
| In1.Cu | Ground plane |
| In2.Cu | Power distribution and additional routing |
| B.Cu | Bottom-side signal routing |

The final copper-zone assignments and layer connectivity should be verified in the PCB project before manufacturing.

## PCB Design Workflow

1. Created the STM32 microcontroller schematic in KiCad.
2. Assigned component footprints and transferred the design to PCB Editor.
3. Arranged components and established the board layout.
4. Configured the four copper layers.
5. Routed connections using KiCad and FreeRouting.
6. Added vias to connect signals between copper layers where necessary.
7. Resolved design-rule violations, including via-diameter constraints and board-outline issues.
8. Generated Gerber and drill files for manufacturing preparation.

## Repository Contents

- `STM32_PCB.kicad_sch` — schematic source file
- `STM32_PCB.kicad_pcb` — PCB layout source file
- `STM32_PCB.kicad_pro` — KiCad project settings
- `Gerber/` — exported manufacturing files

## Design Validation

The PCB was checked using KiCad's Design Rules Checker. The reported DRC errors were resolved, and the latest check reported zero errors.

This confirms that the reported DRC checks passed at that stage; it does not independently verify electrical functionality or successful manufacturing.

## Current Project Status

**Status:** PCB layout and manufacturing-file preparation.

The schematic and PCB layout have been developed in KiCad. Physical fabrication, assembly, and hardware testing should be documented separately once completed.

## Future Improvements

- Fabricate the PCB and inspect manufacturing quality.
- Assemble the components and verify the power supply.
- Test the STM32 clock, reset, boot configuration, and USB interface.
- Validate the board using a multimeter and suitable debugging tools.
- Document measured results and update the design based on testing.

## Author

**Nandish Reddy L**

Electronics and Communication Engineering  
Interests: PCB Design, Embedded Systems, Digital VLSI, and Hardware Development.
