# Day 2 – Sequential Logic, DFF and Multiple Modules

## 📑 Index

1. [Objective](#objective)
2. [Theory](#theory)
3. [DFF with Asynchronous Set](#dff-with-asynchronous-set)
4. [DFF with Asynchronous Reset](#dff-with-asynchronous-reset)
5. [DFF with Synchronous Reset](#dff-with-synchronous-reset)
6. [Multiplier Designs](#multiplier-designs)
7. [Multiple Module Design](#multiple-module-design)
8. [Simulation](#simulation)
9. [Synthesis](#synthesis)
10. [Results](#results)
11. [What I Learned](#what-i-learned)
12. [Conclusion](#conclusion)

---

## Objective

In this experiment, I studied different sequential RTL designs using
Verilog HDL.

The experiments mainly focus on:

- D Flip-Flop with asynchronous set
- D Flip-Flop with asynchronous reset
- D Flip-Flop with synchronous reset
- 2-bit and 8-bit multiplier designs
- Multiple module designs
- RTL simulation and waveform analysis
- RTL synthesis and netlist generation

---

## Theory

### D Flip-Flop

A D Flip-Flop is a sequential logic element used to store one bit of
data. The output changes according to the input `D` at the active
clock edge.

### Asynchronous Set

An asynchronous set changes the output immediately when the set signal
is activated, without waiting for the clock edge.

### Asynchronous Reset

An asynchronous reset clears the output immediately when the reset
signal is activated, independent of the clock.

### Synchronous Reset

A synchronous reset operates only at the active clock edge. The reset
condition is checked along with the clock.

---

## DFF with Asynchronous Set

A D Flip-Flop with asynchronous set was designed and verified.

The asynchronous set allows the output to be set independently of the
clock signal.

### Block Diagram

![DFF Async Set Block Diagram](./dff_async_set%20blockdiagram.png)

### Netlist

![DFF Async Set Netlist](./dff_async_set%20netlist.png)

### Waveform

![DFF Async Set Waveform](./dff_async_set%20waveform.png)

The waveform verifies the operation of the D Flip-Flop with
asynchronous set.

---

## DFF with Asynchronous Reset

A D Flip-Flop with asynchronous reset was implemented and verified.

The asynchronous reset can clear the output independently of the
clock.

### Block Diagram

![DFF Async Reset Block Diagram](./dff_asyncres%20blockdiagram.png)

### Netlist

![DFF Async Reset Netlist](./dff_asyncres%20netlist.png)

### Waveform

![DFF Async Reset Waveform](./dff_asyncres%20waveform.png)

The waveform shows the response of the flip-flop when the asynchronous
reset is activated.

---

## DFF with Synchronous Reset

A D Flip-Flop with synchronous reset was designed to understand the
difference between synchronous and asynchronous reset.

In synchronous reset, the reset operation takes place only at the
active clock edge.

### Netlist and Block Diagram

![DFF Sync Reset Netlist and Block Diagram](./dff_syncres%20netlist%20and%20blockdiagram.png)

### Waveform

![DFF Sync Reset Waveform](./dff_syncres%20waveform.png)

The waveform verifies the synchronous reset operation.

---

## Multiplier Designs

A multiplier is a combinational digital circuit used to perform binary
multiplication.

Different multiplier sizes were synthesized during this experiment.

### 2-Bit Multiplier

![2 Bit Multiplier Netlist and Block Diagram](./mult%202%20netlist%20and%20blockdiagram.png)

### 8-Bit Multiplier

![8 Bit Multiplier Netlist and Block Diagram](./mult%208%20netlist%20and%20blockdiagram.png)

The synthesized designs show the hardware representation of the
different multiplier circuits.

---

## Multiple Module Design

Large RTL designs can be divided into multiple smaller Verilog
modules.

Each module performs a particular function and modules can be
connected together using module instantiation.

Multiple-module designs can be represented using:

- Flat hierarchy
- Hierarchical structure

---

### Flat Netlist 1

![Multiple Module Flat Netlist 1](./multiple_module_flat_netlist1.png)

### Flat Netlist 2

![Multiple Module Flat Netlist 2](./multiple_module_flat_netlist2.png)

### Flat Netlist 3

![Multiple Module Flat Netlist 3](./multiple_module_flat_netlist3.png)

The flat netlists represent the design after the module hierarchy has
been flattened.

---

### Hierarchical Netlist 1

![Multiple Module Hierarchical Netlist 1](./multiple_module_hier_netlist1.png)

### Hierarchical Netlist 2

![Multiple Module Hierarchical Netlist 2](./multiple_module_hier_netlist2.png)

The hierarchical netlists preserve the module-level structure of the
RTL design.

---

### Multiple Modules Netlist and Block Diagram

![Multiple Modules Netlist and Block Diagram](./multiple_modules%20netlist%20and%20blockdiagram.png)

This diagram shows the overall multiple-module design and its
corresponding netlist.

---

## Simulation

The RTL designs were simulated to verify their functionality.

Simulation waveforms were used to observe:

- Clock signal
- Data input
- Set and reset signals
- Output response
- Combinational logic behavior

The simulation results were checked before proceeding to synthesis.

---

## Synthesis

After successful RTL simulation, the designs were synthesized.

RTL synthesis converts the Verilog HDL description into a
hardware-level representation.

The generated netlists and block diagrams help in understanding how
the RTL designs are mapped into hardware.

---

## Results

The D Flip-Flop designs with asynchronous set, asynchronous reset and
synchronous reset were successfully designed and verified.

The 2-bit and 8-bit multiplier designs were successfully synthesized.

The multiple-module designs were also synthesized and their flat and
hierarchical netlists were observed.

The generated waveforms and netlists verified the expected behavior of
the designs.

---

## What I Learned

From this experiment, I learned:

- Basic operation of a D Flip-Flop.
- Difference between synchronous and asynchronous reset.
- Working of asynchronous set and reset.
- Working of synchronous reset.
- RTL coding using Verilog HDL.
- RTL simulation and waveform analysis.
- Basic multiplier design.
- Multiple Verilog module design.
- Difference between flat and hierarchical netlists.
- RTL synthesis and hardware representation.
- How RTL modules are converted into hardware netlists.

---

## Conclusion

Day 2 provided an understanding of sequential RTL design, multiplier
design and multiple-module hierarchy.

D Flip-Flops with asynchronous set, asynchronous reset and synchronous
reset were designed and verified.

The multiplier designs were synthesized and the flat and hierarchical
representations of multiple-module RTL designs were studied.

The experiments helped in understanding RTL coding, simulation,
synthesis, netlists and hardware representation.

---

### 🔝 Back to Index

[Back to Index](#-index)
