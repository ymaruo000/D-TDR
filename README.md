# D-TDR: Duty-Ratio Time Domain Reflectometry

A low-cost, open-source soil moisture sensor that measures apparent relative permittivity (Ka) using duty-ratio modulation of TDR pulse travel time.

## Overview

D-TDR converts the two-way electromagnetic travel time in a TDR probe into a DC voltage proportional to the square root of Ka, using three analog circuits:

1. **Oscillator** — generates a repetitive pulse into the waveguide probe
2. **Comparator** — encodes the travel time as a duty ratio
3. **Integrator** — converts the duty ratio into a stable DC voltage

The output voltage V_DTDR is linearly proportional to sqrt(Ka), enabling direct use of established Ka-theta calibration relationships developed for conventional TDR.

## Features

- No waveform digitization or dedicated TDR instrumentation required
- Medium-independent calibration using air and water only
- Full compatibility with established Ka-theta relationships (e.g., Topp et al., 1980)

## Repository Contents

```
kicad/          KiCad project files (schematic, PCB layout)
docs/
  TDR20260220.pdf       Circuit schematic (PDF)
  TDR20260220_pcb.pdf   PCB layout (PDF)
  TDR20260220.csv       Bill of materials
```


## Requirements

- [KiCad](https://www.kicad.org/) 9.0 or later to open and edit the design files (the files were saved with KiCad 9.0 and cannot be opened in earlier versions)
- PDF viewer to browse the schematic and PCB layout

## Notes on Components

- The comparator (U2, NJM360, Nisshinbo Micro Devices) has been discontinued.

## Reference

Maruo, Y., Fujita, Y. and Noborio, K. (2026): A low-cost Duty-ratio Time Domain Reflectometry (D-TDR) for soil permittivity measurement. J. Jpn. Soc. Soil Phys., 164 (in press).

## License

This project is licensed under the [CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P v2)](https://ohwr.org/cern_ohl_p_v2.txt). See [LICENSE](LICENSE) for details.
