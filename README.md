# Sequence Detector — Mealy vs Moore FSM

A comparative implementation of a sequence detector using both **Mealy** and **Moore** finite state machine architectures, built to explore the tradeoffs between the two models in terms of output timing, state count, and hardware resource usage.

## 🚧 Status: In Progress

This project is currently in the design phase. Progress so far:

- [x] Defined target sequence to detect
- [x] Hand-drawn state diagrams for both Mealy and Moore implementations
- [ ] Verilog/VHDL implementation — Mealy FSM
- [ ] Verilog/VHDL implementation — Moore FSM
- [ ] Testbench development
- [ ] Simulation & waveform verification
- [ ] Synthesis / resource utilization comparison
- [ ] FPGA deployment (optional, if hardware available)

## Overview

A sequence detector is a classic FSM design problem: given a serial input stream, the circuit asserts an output whenever a specific bit pattern (e.g., `1011`) is detected. This project implements the detector two ways to directly compare:

| | Mealy FSM | Moore FSM |
|---|---|---|
| Output depends on | State + Input | State only |
| Output timing | Combinational (faster reaction) | Registered (glitch-free) |
| Typical state count | Fewer states | More states |

## Planned Approach

1. **State diagram design** — completed on paper for both FSM types (photos to be added to `/docs`).
2. **RTL implementation** — Verilog modules for each FSM variant.
3. **Testbench & simulation** — verify detection across overlapping and non-overlapping sequences.
4. **Synthesis comparison** — compare LUT/FF usage and timing between the two designs.

## Repository Structure (planned)

```
├── docs/           # State diagrams, notes, design writeups
├── mealy/          # Mealy FSM RTL
├── moore/          # Moore FSM RTL
├── testbenches/    # Simulation testbenches
└── README.md
```

## Tools

- HDL: Verilog (planned)
- Simulation: [ModelSim / Vivado — TBD]
- Target hardware: [TBD, if applicable]

## Notes

This repo will be updated incrementally as the design moves from paper to RTL to verified hardware. Check commit history for progress.
