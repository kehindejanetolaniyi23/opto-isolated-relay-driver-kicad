# Opto-Isolated Relay Driver PCB Design in KiCad

This repository contains a complete KiCad PCB design project for an opto-isolated relay driver circuit. The board is designed to allow a low-voltage microcontroller control signal to switch an external load through a relay while using optocoupler isolation between the control input and relay driver stage.

## Project Overview

The circuit demonstrates a practical embedded electronics interface commonly used in automation, control systems, and microcontroller-based switching applications.

The design includes:

* Microcontroller control input
* PC817 optocoupler isolation stage
* NPN transistor relay driver
* 5V SPDT relay
* Flyback diode protection
* Input indicator LED
* Relay status LED
* 5V power input terminal
* COM, NO, and NC relay output terminal
* Fully routed PCB layout
* Clean DRC result
* 3D PCB view
* Gerber fabrication outputs

## Design Purpose

The purpose of this project is to demonstrate a complete KiCad PCB design workflow, from schematic capture to PCB layout and fabrication output generation.

The relay driver circuit is useful for switching external devices using a microcontroller signal while keeping the control side separated from the relay-driving stage through optocoupler isolation.

## Tools Used

* KiCad
* KiCad Schematic Editor
* KiCad PCB Editor
* KiCad 3D Viewer
* KiCad Gerber Viewer

## Main Circuit Blocks

### 1. Control Input Stage

The microcontroller control input is connected through a resistor and input indicator LED. This section provides a visual indication when a control signal is applied.

### 2. Optocoupler Isolation Stage

A PC817 optocoupler is used to provide electrical separation between the microcontroller input side and the relay driver side. This improves protection and reduces direct electrical coupling between the two sections.

### 3. Transistor Relay Driver Stage

An NPN transistor is used to drive the relay coil. The transistor allows the low-current control signal from the optocoupler output to control the higher current required by the relay coil.

### 4. Flyback Protection

A 1N4007 diode is connected across the relay coil to protect the transistor from reverse voltage spikes generated when the relay coil turns off.

### 5. Relay Output Stage

The relay output is routed to a three-pin terminal block with COM, NO, and NC connections. This allows the board to switch an external load depending on the relay state.

## Project Files

The repository includes:

* `.kicad_pro` — KiCad project file
* `.kicad_sch` — schematic design file
* `.kicad_pcb` — routed PCB layout file
* `gerbers/` — exported PCB fabrication files
* `Screenshots/` — schematic, layout, DRC, 3D view, and Gerber verification screenshots

## Verification

The PCB layout was checked using KiCad Design Rules Checker.

Result:

* Violations: 0
* Unconnected items: 0
* Errors: 0
* Warnings: 0

This confirms that the board layout is fully routed and passes the KiCad DRC check.

## Screenshots

### Schematic Overview

![Schematic Overview](Screenshots/kicad_schematic_overview.png)

### PCB Layout Overview

![PCB Layout Overview](Screenshots/kicad_pcb_layout_overview.png)

### Clean DRC Result

![DRC Result](Screenshots/kicad_drc_clean_result.png)

### 3D Board View

![3D Board View](Screenshots/kicad_3d_board_view.png)

### Gerber Viewer Verification

![Gerber Viewer](Screenshots/kicad_gerber_viewer_verification.png)

## Fabrication Output

The `gerbers/` folder contains the exported Gerber and drill files required for PCB fabrication.

Included manufacturing layers:

* Front copper
* Back copper
* Front silkscreen
* Back silkscreen
* Front solder mask
* Back solder mask
* Board outline
* Drill files

## Status

Completed portfolio PCB design project.

The project demonstrates schematic capture, footprint assignment, PCB routing, DRC verification, 3D board inspection, and Gerber file export using KiCad.
