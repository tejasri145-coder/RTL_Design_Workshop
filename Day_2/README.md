# Day 2 - Sequential Logic, DFF and Multiple Module Synthesis

Day 2 focuses on understanding sequential logic circuits, different types of D flip-flops, multiplication circuits, and multiple module synthesis using Yosys.

In this session, I worked with D flip-flops using asynchronous set, asynchronous reset, synchronous reset, multiplication circuits, and multiple module designs.

The designs were simulated to verify their functionality and synthesized using Yosys to understand the generated netlists and block diagrams.

---

# Index

1. [Objective](#1-objective)
2. [Theory](#2-theory)
3. [DFF with Asynchronous Set](#3-dff-with-asynchronous-set)
4. [DFF with Asynchronous Reset](#4-dff-with-asynchronous-reset)
5. [DFF with Synchronous Reset](#5-dff-with-synchronous-reset)
6. [2-Bit Multiplication](#6-2-bit-multiplication)
7. [8-Bit Multiplication](#7-8-bit-multiplication)
8. [Multiple Module Design](#8-multiple-module-design)
9. [Hierarchical Synthesis](#9-hierarchical-synthesis)
10. [Flattened Synthesis](#10-flattened-synthesis)
11. [Overall Learning](#11-overall-learning)
12. [Conclusion](#12-conclusion)

---

# 1. Objective

The main objective of Day 2 was to understand sequential logic and how different RTL designs are synthesized into hardware.

The main concepts covered were:

- Sequential logic
- D flip-flops
- Asynchronous set
- Asynchronous reset
- Synchronous reset
- RTL simulation
- Waveform analysis
- Multiplication circuits
- Multiple module designs
- Hierarchical synthesis
- Flattened synthesis
- Netlist generation
- Block diagram analysis
- RTL synthesis using Yosys

---

# 2. Theory

## Sequential Logic

Sequential logic is a type of digital logic in which the output depends on both the present input and the previous state of the circuit.

Unlike combinational logic, sequential circuits contain memory elements.

Flip-flops are commonly used as memory elements in sequential circuits.

## D Flip-Flop

A D flip-flop stores one bit of information.

The main signals of a D flip-flop are:

- `D` - Data input
- `clk` - Clock input
- `Q` - Output
- `reset` or `set` - Control signals

Normally, the value present at the D input is transferred to the output at the active edge of the clock.

Different types of reset and set conditions can be used depending on the design.

---

# 3. DFF with Asynchronous Set

## What I designed

In this experiment, I worked with a D flip-flop having an asynchronous set signal.

An asynchronous set can change the output immediately without waiting for the active edge of the clock.

When the set signal becomes active, the output is forced to logic `1`.

When the set signal is inactive, the flip-flop operates normally according to the clock and data input.

## Simulation

The design was simulated and the waveform was observed.

The waveform was used to analyze:

- Clock signal
- Data input
- Asynchronous set
- Output

The output changes immediately when the asynchronous set is activated.

### Waveform Result

![DFF Asynchronous Set Waveform](./dff_async_set%20waveform.png)

## Netlist

After synthesis, the generated netlist was analyzed.

The netlist represents the hardware connections generated from the RTL design.

### Netlist Result

![DFF Asynchronous Set Netlist](./dff_async_set%20netlist.png)

## Block Diagram

The synthesized block diagram shows the hardware structure of the D flip-flop with asynchronous set.

### Block Diagram Result

![DFF Asynchronous Set Block Diagram](./dff_async_set%20blockdiagram.png)

## Result

This experiment helped me understand that an asynchronous set affects the output independently of the clock.

## Files

- `dff_async_set waveform.png` - Simulation waveform
- `dff_async_set netlist.png` - Synthesized netlist
- `dff_async_set blockdiagram.png` - Block diagram

---

# 4. DFF with Asynchronous Reset

## What I designed

In this experiment, I worked with a D flip-flop having an asynchronous reset.

An asynchronous reset changes the output immediately when the reset signal becomes active.

It does not need to wait for the active edge of the clock.

When reset is active, the output is forced to logic `0`.

When reset is inactive, the D flip-flop operates normally.

## Simulation

The design was simulated and the waveform was observed.

The waveform shows the behavior of the clock, reset, input, and output signals.

### Waveform Result

![DFF Asynchronous Reset Waveform](./dff_asyncres%20waveform.png)

## Netlist

The RTL design was synthesized and the generated netlist was observed.

### Netlist Result

![DFF Asynchronous Reset Netlist](./dff_asyncres%20netlist.png)

## Block Diagram

The synthesized block diagram was used to understand the hardware implementation of the asynchronous reset D flip-flop.

### Block Diagram Result

![DFF Asynchronous Reset Block Diagram](./dff_asyncres%20blockdiagram.png)

## Result

This experiment helped me understand that an asynchronous reset can reset the output immediately without waiting for the clock edge.

## Files

- `dff_asyncres waveform.png` - Simulation waveform
- `dff_asyncres netlist.png` - Synthesized netlist
- `dff_asyncres blockdiagram.png` - Block diagram

---

# 5. DFF with Synchronous Reset

## What I designed

In this experiment, I worked with a D flip-flop having a synchronous reset.

Unlike an asynchronous reset, a synchronous reset affects the output only at the active edge of the clock.

When the reset signal is active at the clock edge, the output is reset.

Otherwise, the data input is transferred to the output.

## Simulation

The design was simulated and the waveform was observed.

The waveform helped verify that the reset operation occurs according to the clock.

### Waveform Result

![DFF Synchronous Reset Waveform](./dff_syncres%20waveform.png)

## Synthesis

The design was synthesized using Yosys.

The generated netlist and block diagram show how the synchronous reset logic is implemented in hardware.

### Netlist and Block Diagram

![DFF Synchronous Reset Netlist and Block Diagram](./dff_syncres%20netlist%20and%20blockdiagram.png)

## Result

This experiment helped me understand the difference between synchronous and asynchronous reset operations.

In synchronous reset, the output changes according to the reset condition only at the active clock edge.

## Files

- `dff_syncres waveform.png` - Simulation waveform
- `dff_syncres netlist and blockdiagram.png` - Netlist and block diagram

---

# 6. 2-Bit Multiplication

## What I designed

In this experiment, I worked with a multiplication circuit.

The RTL design performs multiplication between input values and produces the multiplication result at the output.

The purpose of this experiment was to understand how arithmetic operations written in Verilog are converted into hardware during synthesis.

## Synthesis

The multiplication design was synthesized using Yosys.

The generated netlist and block diagram were analyzed to understand the hardware implementation.

### Netlist and Block Diagram

![2-Bit Multiplication Netlist and Block Diagram](./mult_2%20netlist%20and%20blockdiagram.png)

## Result

This experiment helped me understand how a multiplication operation written in RTL is interpreted and synthesized into digital hardware.

## File

- `mult_2 netlist and blockdiagram.png` - Synthesized netlist and block diagram

---

# 7. 8-Bit Multiplication

## What I designed

In this experiment, I worked with another multiplication circuit having larger input width.

Increasing the number of input bits increases the complexity of the hardware required to perform multiplication.

The purpose of this experiment was to compare the synthesized hardware with the smaller multiplication design.

## Synthesis

The RTL was synthesized using Yosys.

The generated netlist and block diagram show the hardware required to implement the multiplication operation.

### Netlist and Block Diagram

![8-Bit Multiplication Netlist and Block Diagram](./mult_8%20netlist%20and%20blockdiagram.png)

## Result

This experiment helped me understand that the size and complexity of arithmetic hardware increase as the width of the input operands increases.

## File

- `mult_8 netlist and blockdiagram.png` - Synthesized netlist and block diagram

---

# 8. Multiple Module Design

## What I designed

In this experiment, I worked with a design containing multiple Verilog modules.

Large RTL designs are usually divided into smaller modules.

Each module performs a particular function, and the modules are connected together to form the complete design.

This approach makes RTL designs easier to understand, develop, test, and reuse.

## Synthesis

The multiple module design was synthesized using Yosys.

The resulting netlist and block diagram show how different modules are connected together.

### Netlist and Block Diagram

![Multiple Modules Netlist and Block Diagram](./multiple_modules%20netlist%20and%20blockdiagram.png)

## Result

This experiment helped me understand how multiple Verilog modules can be connected together and synthesized as a single design.

## File

- `multiple_modules netlist and blockdiagram.png` - Multiple module synthesis result

---

# 9. Hierarchical Synthesis

## What I designed

In hierarchical synthesis, the structure of the individual modules is maintained.

The submodules remain visible in the synthesized design instead of being merged completely into the top-level module.

This makes it easier to understand the relationship between the top module and its submodules.

## Synthesis

The design was synthesized while maintaining the module hierarchy.

Different synthesized netlists were observed to understand the hierarchical representation.

### Hierarchical Netlist 1

![Multiple Module Hierarchical Netlist 1](./multiple_module_hier%20netlist1.png)

### Hierarchical Netlist 2

![Multiple Module Hierarchical Netlist 2](./multiple_module_hier%20netlist2.png)

## Result

The hierarchical synthesis results show the module boundaries and connections between different modules.

This helped me understand how Yosys preserves the RTL module hierarchy during synthesis.

## Files

- `multiple_module_hier netlist1.png` - Hierarchical netlist result 1
- `multiple_module_hier netlist2.png` - Hierarchical netlist result 2

---

# 10. Flattened Synthesis

## What I designed

In flattened synthesis, the hierarchy between different modules is removed.

The logic from the submodules is combined into the top-level design.

As a result, the synthesized circuit is represented as a single flattened hardware structure.

## Synthesis

The multiple module design was flattened during synthesis.

Different netlist views were observed to understand how the design changes after flattening.

### Flattened Netlist 1

![Multiple Module Flat Netlist 1](./multiple_module_flat%20netlist1.png)

### Flattened Netlist 2

![Multiple Module Flat Netlist 2](./multiple_module_flat%20netlist2.png)

### Flattened Netlist 3

![Multiple Module Flat Netlist 3](./multiple_module_flat%20netlist3.png)

## Result

The flattened synthesis results show that the module hierarchy is removed and the internal logic is combined into a single design.

This experiment helped me understand the difference between hierarchical and flattened synthesis.

## Files

- `multiple_module_flat netlist1.png` - Flattened netlist result 1
- `multiple_module_flat netlist2.png` - Flattened netlist result 2
- `multiple_module_flat netlist3.png` - Flattened netlist result 3

---

# 11. Overall Learning

Through the Day 2 experiments, I understood the following:

- How sequential logic differs from combinational logic.
- How a D flip-flop stores data.
- How clock signals control sequential circuits.
- How asynchronous set works.
- How asynchronous reset works.
- How synchronous reset works.
- The difference between synchronous and asynchronous control signals.
- How simulation waveforms are used to verify RTL behavior.
- How multiplication operations are represented in RTL.
- How arithmetic RTL is converted into hardware.
- How input width affects the complexity of multiplication circuits.
- How multiple Verilog modules are connected.
- How module hierarchy is represented during synthesis.
- How hierarchical synthesis preserves module boundaries.
- How flattened synthesis removes module boundaries.
- How Yosys generates synthesized netlists.
- How synthesized block diagrams represent hardware structures.
- How RTL code is converted into actual digital logic.

---

# 12. Conclusion

Day 2 helped me understand sequential logic, D flip-flops, multiplication circuits, and multiple module synthesis.

I worked with D flip-flops having asynchronous set, asynchronous reset, and synchronous reset. By observing their waveforms and synthesized circuits, I understood how different reset and set conditions affect sequential logic.

The multiplication experiments helped me understand how arithmetic operations written in RTL are converted into hardware and how the size of the operands affects hardware complexity.

The multiple module experiments helped me understand how larger RTL designs can be divided into smaller modules.

By comparing hierarchical and flattened synthesis results, I understood how Yosys can either preserve module boundaries or combine the complete design into a single flattened hardware structure.

Overall, Day 2 improved my understanding of sequential RTL design, D flip-flops, arithmetic circuits, module hierarchy, simulation, synthesis, netlists, and hardware implementation.
