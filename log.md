# Dev Log – clean-analog-supply  
Project: 3.3–5 V input → ±12 V → ±5 V low-noise analog power supply  
Start date: 2025-04-09

---

## Day 1 – 2025-04-09

- Finalized core architecture:
  → Boost: 3.3–5 V in → +12 V  
  → Inverting DC-DC: 3.3–5 V in → –12 V  
  → Dual LDO (TPS7A39): ±12 V → ±5 V clean analog rails

- Created GitHub repository and project structure

- Selected main components:
  - **Boost converter:** TPS61287 — delivers +12 V @ 1 A from low-voltage input
  - **Inverting converter:** TPS63700 — provides –12 V from same rail
  - **LDO:** TPS7A39 — dual-channel ultra-low-noise linear regulator (±5 V out)

- Rationale for architecture:
  - Dual rails needed for op-amps and analog signal chain
  - LDOs chosen for low noise and high PSRR
  - Symmetry and noise performance prioritized over minimal BOM




