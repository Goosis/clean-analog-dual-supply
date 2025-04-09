# Dev Log – boost-ldo-rail
Project: 3.3–5 V in → 12 V → ±5 V analog-friendly power architecture  
Start date: 04.09.2025

---

## Day 1 – 04.09

- Defined core architecture:  
  → Boost converter: 3.3–5 V input to 12 V output  
  → LDO for 5 V @ 100 mA analog rail  
  → Optional inverting stage for -5 V @ 50 mA (op-amp rail)

- Created GitHub repo and project structure

- Chose main components:
  - **Boost converter:** [TPS61287] – handles 12 V @ 1 A, clean and compact
  - **LDO:** [TPS7A39] – dual-channel ±5 V, ultra-low noise
  - Negative rail will be derived from 12 V rail, not from LDO

- Set target goals:
  - Stable, low-noise analog power system
  - Compact design, real-world usable
  - Learn & document every decision made

- TODO:
  - Select inductor for boost stage (10 µH, ≥1.5 A, low DCR)
  - Start schematic in KiCad
  - Run basic simulations
  - Document cap selection and π-filter layout

