# arduino uno clone v1.0 to v2.0 to v2.1 to v2.2
Arduino Uno clone using ATmega328P and CH340G module - schematic, PCB layout, and design learnings.

This repository documents the **second iteration** of an Arduino Uno–compatible board
designed using **ATmega328P** and a **CH340G USB–UART interface**.

The focus of this project is not just replication, but **learning through iteration** —
specifically:
- Power integrity
- Decoupling and grounding
- Crystal oscillator layout
- Reset behavior
- Practical PCB layout constraints

## Project Status
- ✔ Schematic completed
- ✔ PCB layout completed
- ⏳ Fabrication pending
- ⏳ Assembly and bootloader programming pending

## Repository Structure
- `schematic/` – Circuit diagrams and notes
- `pcb/` – PCB layout files, Gerbers, drill files
- `docs/` – Design decisions and learnings
- `images/` – Renders, layout screenshots, assembled board photos

## Version history

### v1.0
- First iteration, done made a schematic and layou and iterated on zero PCB
- had many debugging issues, mentioned in documentation
- (addition, not mentioned in documentaion) the correction that was made in v2.2 was a issue here also.

### v2.0
Initial Arduino UNO clone design.
- Functional with external supply
- USB power path limitation discovered later

### v2.1
Power-path corrected using Schottky diode isolation.
- Safe USB + external power coexistence
- No backfeeding into CH340G
- Matches correct electrical behavior of Arduino-class boards

### v2.2 (recommended)
Corrected basic module input error
- Earlier RX pin of CH340G module was connected to RX pin of ATmega328P, now it is corrected and attached to TX of ATmega328P
- Same goes with TX pin of CH340G
- bottom layer was also grounded, top and bottom ground is stitched using vias, in empty places, to further improve return paths

## Author
**Devansh Sharma**
