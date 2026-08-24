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
- Multiplier designs
- Multiple module designs
- RTL simulation and waveform analysis
- RTL synthesis and netlist generation

The designs were simulated and synthesized to understand their
behavior and hardware implementation.

---

## Theory

### D Flip-Flop

A D Flip-Flop is a sequential logic element used to store one bit of
data.

The output changes according to the input `D` at the active clock edge.

A D Flip-Flop can also have additional control signals such as
asynchronous set/reset or synchronous reset.

### Asynchronous Set

An asynchronous set allows the output of the flip-flop to be set
without waiting for the clock edge.

When the asynchronous set signal is activated, the output is
immediately set to the required state.

### Asynchronous Reset

An asynchronous reset clears the flip-flop output immediately when
the reset signal is activated, independent of the clock.

### Synchronous Reset

A synchronous reset works only at the active clock edge. The reset
condition is checked along with the clock.

---

# DFF with Asynchronous Set

In this experiment, a D Flip-Flop with an asynchronous set input was
designed.

The asynchronous set can change the output independently of the
clock signal.

### Block Diagram

![DFF Async Set Block Diagram](./dff_async_set_blockdiagram.png)

### Netlist

![DFF Async Set Netlist](./dff_async_set_netlist.png)

### Waveform

![DFF Async Set Waveform](./dff_async_set_waveform.png)

The waveform verifies the behavior of the D Flip-Flop with
asynchronous set.

---

# DFF with Asynchronous Reset

A D Flip-Flop with asynchronous reset was also implemented.

The reset signal can clear the output independently of the clock.

### Block Diagram

![DFF Async Reset Block Diagram](./dff_asyncres_blockdiagram.png)

### Netlist

![DFF Async Reset Netlist](./dff_asyncres_netlist.png)

### Waveform

![DFF Async Reset Waveform](./dff_asyncres_waveform.png)

The waveform shows the response of the flip-flop when the asynchronous
reset is activated.

---

# DFF with Synchronous Reset

A D Flip-Flop with synchronous reset was designed to understand the
difference between synchronous and asynchronous control signals.

In synchronous reset, the reset operation takes place only with the
active clock edge.

### Netlist and Block Diagram

![DFF Sync Reset Netlist and Block Diagram](./dff_syncres%20netlist%20and%20blockdiagram.png)

### Waveform

![DFF Sync Reset Waveform](./dff_syncres%20waveform.png)

The waveform verifies that the reset operation is synchronized with
the clock.

---

# Multiplier Designs

Multipliers are combinational digital circuits used to perform
binary multiplication.

Different multiplier configurations were studied and synthesized
during this experiment.

### 2-Bit Multiplier

![2 Bit Multiplier Netlist and Block Diagram](./mult_2_netlist%20and%20blockdiagram.png)

### 8-Bit Multiplier

![8 Bit Multiplier Netlist and Block Diagram](./mult_8_netlist%20and%20blockdiagram.png)

These synthesized representations show the hardware generated for
the multiplier designs.

---

# Multiple Module Design

A digital design can contain multiple Verilog modules.

Modules can be connected hierarchically, where one module can
instantiate another module.

This helps in creating large designs by dividing them into smaller
and reusable blocks.

### Flat Netlist – Module 1

![Multiple Module Flat Netlist 1](./multiple_module_flat_netlist1.png)

### Flat Netlist – Module 2

![Multiple Module Flat Netlist 2](./multiple_module_flat_netlist2.png)

### Flat Netlist – Module 3

![Multiple Module Flat Netlist 3](./multiple_module_flat_netlist3.png)

### Hierarchical Netlist – Module 1

![Multiple Module Hierarchical Netlist 1](./multiple_modules_hier_netlist1.png)

### Hierarchical Netlist – Module 2

![Multiple Module Hierarchical Netlist 2](./multiple_module_hier_netlist2.png)

### Multiple Modules Netlist and Block Diagram

![Multiple Modules Netlist and Block Diagram](./multiple_modules_netlist%20and%20blockdiagram.png)

The above diagrams show the difference between flat and hierarchical
representations of multiple RTL modules.

---

# Simulation

The RTL designs were simulated to verify their functionality.

Simulation waveforms were used to observe the behavior of the
different sequential circuits.

The D Flip-Flop waveforms show the relationship between:

- Clock
- Data input
- Set/Reset signals
- Output

The multiplier and other RTL designs were also verified before
synthesis.

---

# Synthesis

After successful simulation, the RTL designs were synthesized.

Synthesis converts the Verilog RTL description into a hardware
representation.

The generated netlists and block diagrams help in understanding how
the RTL code is mapped into actual hardware structures.

The experiments also demonstrate the difference between flat and
hierarchical module representations.

---

# Results

The D Flip-Flop designs with asynchronous set, asynchronous reset and
synchronous reset were successfully simulated.

The multiplier designs were successfully synthesized.

The multiple-module designs were also synthesized and their flat and
hierarchical netlists were observed.

The waveforms and netlists confirm the expected behavior of the
designed circuits.

---

# What I Learned

From this experiment, I learned:

- Basic operation of a D Flip-Flop.
- Difference between synchronous and asynchronous control signals.
- Working of asynchronous set and reset.
- Working of synchronous reset.
- How to design sequential circuits using Verilog HDL.
- How to simulate RTL designs and analyze waveforms.
- Basic multiplier implementation.
- How multiple Verilog modules can be connected.
- Difference between flat and hierarchical netlists.
- How RTL designs are converted into synthesized hardware.
- How to analyze synthesis results and block diagrams.

---

# Conclusion

Day 2 provided an understanding of sequential RTL design and
different synthesis structures.

D Flip-Flops with asynchronous set, asynchronous reset and synchronous
reset were designed and verified through simulation.

Multiplier designs were synthesized and multiple-module designs were
studied using flat and hierarchical netlists.

The experiments helped in understanding RTL coding, simulation,
synthesis, module hierarchy and hardware representation.

---

### 🔝 Back to Index

[Back to Index](#-index)
