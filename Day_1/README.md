# Day 1 – Good MUX

## 📑 Index

1. [Objective](#objective)
2. [Design](#design)
3. [Simulation](#simulation)
4. [Synthesis](#synthesis)
5. [Results](#results)
6. [What I Learned](#what-i-learned)
7. [Conclusion](#conclusion)

---

## Objective

In this experiment, I designed and verified a simple 2:1 Multiplexer (MUX) using Verilog. The design was first simulated to verify its functional behavior and then synthesized using Yosys to observe how the RTL design is converted into a gate-level implementation.

---

## Design

The Good MUX has two data inputs, one select input, and one output.

- `i0` – First data input
- `i1` – Second data input
- `sel` – Select input
- `y` – Output

The operation of the MUX is:

- When `sel = 0`, `y = i0`
- When `sel = 1`, `y = i1`

The Verilog RTL describes the required MUX functionality, and the design was implemented and tested inside the VirtualBox-based VSD environment.

---

## Simulation

After writing the RTL and testbench, I simulated the Good MUX and observed the output waveform using GTKWave.

The waveform shows the signals `i0`, `i1`, `sel`, and `y` changing with time. The output `y` follows the input selected by `sel`, confirming the expected behavior of the 2:1 MUX.

### GTKWave Simulation Result

![Good MUX Waveform](./goodmuxwaveform.png)

---

## Synthesis

After verifying the simulation results, I synthesized the Good MUX using Yosys.

The synthesized design was mapped to the Sky130 standard cell library. The Yosys-generated block diagram shows the MUX implementation using the `sky130_fd_sc_hd__mux2_1` standard cell.

The synthesized design contains the inputs `i0`, `i1`, and `sel`, which are connected to the corresponding MUX cell inputs, with the resulting output connected to `y`.

### Yosys Synthesized Block Diagram

![Good MUX Netlist and Block Diagram](./goodmux_netlist_and_blockdiagram.png)

---

## Results

The Good MUX was successfully simulated and synthesized.

The GTKWave waveform verified that the output `y` correctly follows either `i0` or `i1` depending on the value of the select signal `sel`.

The Yosys synthesis result successfully converted the RTL design into a gate-level implementation using the Sky130 standard cell library. The synthesized block diagram clearly shows the mapping of the RTL MUX to the `sky130_fd_sc_hd__mux2_1` cell.

---

## What I Learned

From
