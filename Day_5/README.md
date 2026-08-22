# Day 5 - Incomplete Conditional Logic and Case Statements

Day 5 focuses on understanding incomplete conditional
statements in RTL and how they affect simulation and
synthesis.

In this session, I worked with incomplete `if` statements
and incomplete case statements. The designs were simulated
using GTKWave and synthesized using Yosys to observe the
resulting waveforms and hardware representations.

These experiments helped me understand how incomplete
assignments can cause storage behavior and why complete
RTL descriptions are important for proper combinational
logic design.

---

# Index

1. [Objective](#1-objective)
2. [Incomplete If Statement](#2-incomplete-if-statement)
3. [Incomplete If Simulation](#3-incomplete-if-simulation)
4. [Incomplete If Synthesis](#4-incomplete-if-synthesis)
5. [Second Incomplete If Design](#5-second-incomplete-if-design)
6. [Second Incomplete If Simulation](#6-second-incomplete-if-simulation)
7. [Incomplete Case Statement](#7-incomplete-case-statement)
8. [Incomplete Case Simulation](#8-incomplete-case-simulation)
9. [Incomplete Case Synthesis](#9-incomplete-case-synthesis)
10. [Overall Learning](#10-overall-learning)
11. [Conclusion](#11-conclusion)

---

# 1. Objective

The main objective of Day 5 was to understand how incomplete
conditional statements are interpreted during RTL simulation
and synthesis.

The main concepts covered were:

- `if` statements in RTL
- Incomplete `if` conditions
- Incomplete assignments
- Case statements
- RTL simulation
- GTKWave waveform analysis
- Yosys synthesis
- Netlist generation
- Block diagram representation
- Latch inference
- Importance of complete RTL coding

---

# 2. Incomplete If Statement

## What I designed

In this experiment, I worked with an incomplete `if`
statement.

An incomplete `if` statement occurs when an output is
assigned only for a particular condition and no assignment
is provided for the other condition.

For example, if an output is assigned only when a condition
is true, the output may need to retain its previous value
when the condition is false.

## Purpose

The purpose of this experiment was to understand how
synthesis tools interpret incomplete conditional logic.

## Result

The design was synthesized using Yosys and the generated
hardware representation was examined.

![Incomplete If Netlist](incomp_if%20netlist%20and%20blockdiagram.png)

---

# 3. Incomplete If Simulation

## Simulation

The incomplete `if` design was simulated to observe the
behavior of the input and output signals.

GTKWave was used to view the generated waveform.

The waveform helps in understanding how the output behaves
when the condition changes.

![Incomplete If Waveform](incomp_if%20waveform.png)

## Result

The simulation showed the behavior of the output for the
different input conditions.

This helped me understand the importance of assigning the
output properly in conditional RTL.

---

# 4. Incomplete If Synthesis

## Synthesis

The RTL design was passed through Yosys for synthesis.

Yosys analyzed the incomplete conditional assignment and
generated the corresponding hardware representation.

The netlist and block diagram were examined to understand
the hardware inferred from the RTL.

![Incomplete If Netlist and Block Diagram](incomp_if%20netlist%20and%20blockdiagram.png)

## Result

This experiment demonstrated how incomplete RTL can lead to
storage behavior during synthesis.

---

# 5. Second Incomplete If Design

## What I designed

A second incomplete `if` example was used to further study
the effect of missing assignments.

The purpose was to compare another incomplete conditional
description with its simulation and synthesized result.

## Synthesis

The design was synthesized using Yosys and its resulting
netlist and block diagram were observed.

![Second Incomplete If Netlist](incomp%20if2%20netlist%20and%20blockdiagram.png)

## Result

This experiment provided another example of how RTL coding
style affects the hardware inferred during synthesis.

---

# 6. Second Incomplete If Simulation

## Simulation

The second incomplete `if` design was simulated using the
Verilog simulation flow.

GTKWave was used to observe the waveform and verify the
behavior of the design.

![Second Incomplete If Waveform](incomp%20if2%20waveform.png)

## Result

The waveform helped me understand how the output behaves
when an assignment is not provided for every condition.

---

# 7. Incomplete Case Statement

## What I designed

In this experiment, I worked with an incomplete case
statement.

A case statement is commonly used to describe different
input conditions in RTL.

When a case statement does not provide an output assignment
for every required condition, the output may retain its
previous value.

## Purpose

The purpose of this experiment was to understand the effect
of incomplete case assignments during simulation and
synthesis.

## Result

The design was processed using the RTL simulation and
synthesis flow.

---

# 8. Incomplete Case Simulation

## Simulation

The incomplete case design was simulated and its waveform
was observed using GTKWave.

The waveform shows the behavior of the output for the
different input conditions applied to the case statement.

![Incomplete Case Waveform](tb_incomp_case%20waveform.png)

## Result

The simulation helped me understand the behavior of the
output when some case conditions do not contain an explicit
assignment.

---

# 9. Incomplete Case Synthesis

## Synthesis

The incomplete case design was synthesized using Yosys.

The generated netlist and block diagram were examined to
understand the hardware inferred from the incomplete case
statement.

![Incomplete Case Netlist and Block Diagram](tb_incomp_case.netlist%20and%20blockdiagram.png)

## Result

The synthesis result demonstrated how the synthesis tool
interprets incomplete case logic.

This experiment showed why complete assignments are
important when designing combinational RTL.

---

# 10. Overall Learning

Through the experiments performed on Day 5, I understood
the following:

- How `if` statements are used in RTL.
- What an incomplete `if` statement means.
- How missing assignments affect RTL behavior.
- How incomplete conditional logic can infer storage.
- How case statements are used in digital design.
- How incomplete case statements affect synthesis.
- How GTKWave is used to observe simulation waveforms.
- How Yosys is used to synthesize RTL.
- How synthesized netlists represent the inferred hardware.
- How block diagrams help visualize synthesized logic.
- Why complete RTL descriptions are important.
- How proper RTL coding helps avoid unintended hardware.

---

# 11. Conclusion

Day 5 helped me understand the importance of complete
conditional logic in RTL design.

I worked with incomplete `if` statements and incomplete
case statements and examined their simulation waveforms
and synthesized netlists.

By comparing the RTL behavior with the synthesized
hardware representation, I understood how incomplete
assignments can affect the hardware inferred by synthesis
tools.

This session improved my understanding of RTL coding
practices and the relationship between RTL descriptions,
simulation results, and synthesized hardware.
