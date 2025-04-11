# clean-analog-supply

Analog ±5 V power supply module built from 3.3–5.0 V input, using two DC-DC converters and an ultra-low-noise dual-channel LDO.

This board is being developed as a standalone analog supply module for use in future projects involving precision op-amps, ADCs, and signal processing chains.

The project is currently in the schematic and layout design phase.

---

## Architecture

- **Input voltage:** 3.3 V – 5.0 V
- **Intermediate rails:** +12 V (Boost), –12.3 V (Inverter)
- **Final rails:** ±5 V via TPS7A39 (dual-channel LDO)

---

## Design Goals

- Clean, low-noise, symmetric analog supply
- Designed for analog and mixed-signal systems (e.g., analog front ends, filters, RF detectors)
- Portable power module for lab and embedded integration


---

## Current Status

- Full schematics completed for all three stages
- Component selection and calculations done
- PCB layout in progress

---

## Schematics

### Boost Converter – TPS61287

![boost schematic](images/schematic_boost.png)

### Inverter – TPS63700

![inverter schematic](images/schematic_inverter.png)

### Dual LDO – TPS7A39

![ldo schematic](images/schematic_ldo.png)

---

## Simulation


- A custom PSPICE model was written for the **AO3400A** MOSFET, as no accurate vendor model was available. This enabled realistic simulation of switching behavior and thermal characteristics in the boost converter stage.


