# PicoRV32 Physical Implementation & Timing Closure

This repository contains the physical design artifacts and implementation log for a PicoRV32 RISC-V core (350 µm x 350 µm) using the OpenLane 2 RTL-to-GDSII flow. The primary focus of this project was navigating tight area constraints, mitigating global routing congestion, and closing timing across multi-cycle logic paths.

**Key Implementation Highlights:**
* **Physical Verification:** Evaluated multi-corner PPA tradeoffs and resolved layout blockers, including a bounding layer XOR DRC violation analyzed in KLayout.
* **Congestion Mitigation:** Alleviated metal layer saturation by investigating OpenROAD routing heat maps and optimizing buffer configurations and placement densities.
* **Timing Closure:** Analyzed OpenSTA reports alongside visual timing paths and evaluated advanced Yosys/ABC synthesis strategies to navigate logic-depth limits. Successfully achieved a clean setup/hold baseline at 50 MHz (0.00 ns TNS) prior to scaling up the target frequency.

> **Note:** For the comprehensive analysis of PVT corners, detailed STA reports, and the full synthesis strategy sweep, please refer to the complete `picoRV32 Openlane2 Project.pdf` linked in this repository.

## Repository Contents

* **`picoRV32 Openlane2 Project.pdf`**: Comprehensive physical design report and timing analysis.
* **`config.json`**: OpenLane 2 configuration settings (e.g., target density, clock constraints).
* **`/reports/`**: Selected OpenSTA timing logs and Yosys synthesis summaries.
* **`/images/`**: OpenROAD GUI routing heatmaps and KLayout physical inspection screenshots.
