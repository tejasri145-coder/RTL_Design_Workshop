# Day 3 - RTL Optimization and Sequential Logic

Day 3 was mainly focused on understanding sequential circuits
and observing how synthesis tools simplify RTL designs.

During this session, I worked with D flip-flops, constant
logic, counters, and different combinational logic examples.

The designs were simulated and then synthesized using Yosys
to understand how the RTL description is transformed into
hardware-level logic.

---

# Index

1. [Objective](#1-objective)
2. [DFF Constant 1](#2-dff-constant-1)
3. [DFF Constant 2](#3-dff-constant-2)
4. [DFF Constant 3](#4-dff-constant-3)
5. [Good Counter](#5-good-counter)
6. [Optimization Check](#6-optimization-check)
7. [Optimization Check 2](#7-optimization-check-2)
8. [Optimization Check 3](#8-optimization-check-3)
9. [Optimization Check 4](#9-optimization-check-4)
10. [Overall Learning](#10-overall-learning)
11. [Conclusion](#11-conclusion)

---

# 1. Objective

The main objective of Day 3 was to understand the behavior
of sequential logic and the optimization performed by Yosys
during the synthesis process.

The major concepts covered were:

- D flip-flop operation
- Clock and reset signals
- Constant value handling
- RTL optimization
- Counter-based sequential logic
- Combinational logic optimization
- RTL simulation
- Waveform analysis
- Yosys synthesis
- Gate-level representation

---

# 2. DFF Constant 1

## What I designed

In this experiment, I studied a D flip-flop with a constant
value applied to its data path.

The circuit mainly deals with a clock signal, reset condition,
and the output of the flip-flop.

The purpose was to understand how a fixed input affects the
behavior of a sequential circuit.

## Simulation

The design was simulated and the waveform was examined to
observe the changes in the clock, reset, and output signals.

### Waveform Result

![DFF Constant Waveform](./dff%20const%20waveform.png)

## Synthesis

After simulation, the design was synthesized using Yosys.

Yosys analyzes the RTL and identifies portions of the design
that have fixed values. Such logic can be simplified during
the synthesis process.

## Observation

This experiment helped me understand that a constant signal
can reduce the amount of logic required in a synthesized
design.

---

# 3. DFF Constant 2

## What I designed

The second D flip-flop experiment was used to study another
case involving constant logic.

The design contains sequential behavior controlled by the
clock and reset signals.

The main purpose was to observe how the synthesis tool
handles a fixed value inside a sequential circuit.

## Synthesis

The RTL design was processed using Yosys.

Yosys examined the logic and generated a hardware
representation after performing its optimization steps.

### Result

![DFF Constant 2](./dff%20const2.png)

## Observation

The synthesized result demonstrates how constant values can
allow the synthesis tool to simplify the original RTL design.

---

# 4. DFF Constant 3

## What I designed

This experiment was another example of a D flip-flop with
constant behavior.

It was used to understand how sequential RTL is represented
after synthesis and how unnecessary logic can be eliminated.

## Synthesis

The design was passed through the Yosys synthesis flow.

The resulting hardware representation shows the simplified
logic obtained from the RTL description.

### Result

![DFF Constant 3](./dff%20const3.png)

## Observation

This experiment showed that synthesis tools can recognize
fixed-value logic and produce a simpler hardware structure
while maintaining the required functionality.

---

# 5. Good Counter

## What I designed

In this experiment, I worked with a counter based on
sequential logic.

A counter changes its state according to clock transitions.
The reset signal is used to initialize the circuit.

The important signals are:

- Clock
- Reset
- Counter output

## Simulation and Synthesis

The counter was analyzed through the RTL simulation and
synthesis flow.

The synthesized design gives a hardware-level view of how
the counter is constructed using sequential elements.

### Counter Netlist and Block Diagram

![Good Counter Netlist and Block Diagram](./good%20counter%20netlist%20and%20blockdiagram.png)

> **Note:** If the actual filename contains a different ending,
> replace the filename above with the exact GitHub filename.

## Observation

The counter experiment helped me understand how sequential
elements can be combined to create a circuit whose state
changes with every clock event.

---

# 6. Optimization Check

## What I designed

This experiment was performed to study the optimization of
a simple combinational RTL expression.

The design contains basic logic operations that can be
simplified during synthesis.

## Synthesis

Yosys processed the RTL and applied optimization techniques
before generating the final hardware representation.

### Netlist and Block Diagram

![Optimization Check Netlist and Block Diagram](./opt%20check%20netlist%20and%20blockdiagram.png)

> **Note:** Replace the filename above with the exact filename
> shown in GitHub if its ending is different.

## Observation

The experiment demonstrates that synthesis tools analyze
the complete logic instead of directly converting every RTL
statement into an individual gate.

---

# 7. Optimization Check 2

## What I designed

This experiment used another combinational logic expression
to observe how Yosys performs optimization.

The objective was to understand how the original RTL can be
converted into a simpler hardware implementation.

## Synthesis

Yosys analyzed the Boolean logic and generated an optimized
representation of the circuit.

### Netlist and Block Diagram

![Optimization Check 2](./opt%20check2%20netlist%20and%20blockdiagram.png)

> **Note:** Check the exact filename in GitHub and replace the
> path if required.

## Observation

The result shows that Boolean logic can often be represented
using fewer or simpler hardware elements after synthesis.

---

# 8. Optimization Check 3

## What I designed

This experiment was another example used to study
combinational logic optimization.

The RTL was passed through the synthesis flow to observe
the resulting hardware structure.

## Synthesis

Yosys performed its optimization passes and generated the
corresponding gate-level representation.

### Netlist and Block Diagram

![Optimization Check 3](./opt%20check3%20netlist%20and%20blockdiagram.png)

> **Note:** Replace the image path with the exact filename
> from the GitHub folder if necessary.

## Observation

This experiment helped me understand how different RTL
expressions can be simplified during synthesis.

---

# 9. Optimization Check 4

## What I designed

This experiment was performed to study another example of
logic optimization.

The design was synthesized to observe how Yosys converts
the RTL description into an optimized hardware structure.

## Synthesis

The synthesis tool analyzed the logic and removed
unnecessary operations wherever possible.

### Netlist and Block Diagram

![Optimization Check 4](./opt%20check4%20netlist%20and%20blockdiagram.png)

> **Note:** Replace the image path with the exact filename
> from the GitHub folder if necessary.

## Observation

The result helped me understand that synthesis optimization
can reduce unnecessary hardware while keeping the required
logic behavior unchanged.

---

# 10. Overall Learning

Through the Day 3 experiments, I learned:

- How D flip-flops are used in sequential circuits.
- How clock signals control sequential logic.
- How reset signals initialize a circuit.
- How constant values affect sequential designs.
- How Yosys identifies constant logic.
- How unnecessary logic can be removed during synthesis.
- How counters are built using sequential elements.
- How combinational logic can be optimized.
- How simulation helps verify RTL functionality.
- How synthesis produces a gate-level representation.
- How RTL descriptions are related to the final hardware.

---

# 11. Conclusion

Day 3 gave me practical knowledge about sequential logic
and RTL optimization.

I worked with D flip-flops, constant-value designs, a
counter, and several logic optimization examples.

The experiments helped me understand the complete flow from
RTL description to simulation and finally to synthesized
hardware.

By observing the synthesized results, I understood how Yosys
can simplify RTL logic and generate an efficient hardware
implementation while preserving the intended functionality.
