## Version history

### v2.0
Initial Arduino UNO clone design.
- Functional with external supply
- USB power path limitation discovered later

### v2.1 (recommended)
Power-path corrected using Schottky diode isolation.
- Safe USB + external power coexistence
- No backfeeding into CH340G
- Matches correct electrical behavior of Arduino-class boards
