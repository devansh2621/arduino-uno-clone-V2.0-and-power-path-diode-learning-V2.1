## Version history

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
