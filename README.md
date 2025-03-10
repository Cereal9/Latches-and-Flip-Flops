# Lab 5: Latches and Flip-Flops


### Introduction
In this lab, we explore the fundamental concepts of latches and flip-flops, which are essential components in digital logic design. Latches and flip-flops are bistable devices used for storing binary information and play a crucial role in sequential circuits. The objectives of this lab include designing, simulating, and implementing a D latch and a D flip-flop with an asynchronous clear.

---

## Objectives
The goals of this lab are as follows:
- To design, analyze, and simulate a D latch.
- To design, analyze, and simulate a D latch with asynchronous active-low clear.
- To simulate, analyze, and implement a rising-edge D flip-flop with asynchronous active-high clear.

---

## Part 1: Design, Simulation, and Verification of a D Latch with Clear

### 1.1 Theory
A **D latch** is a level-sensitive device that transfers input data (D) to the output (Q) when the enable signal (G) is high. The latch holds its previous state when G is low. In this experiment, an additional asynchronous active-high clear signal is introduced, which resets the latch regardless of the enable signal.

### 1.2 Procedure
1. Create a new Quartus project.
2. Develop a VHDL file named `D_Latch.vhd`.
3. Construct a truth table for the D latch with the following properties:
   - The next output Q+ follows input D when G = 1.
   - The output retains its state when G = 0.
   - An active-high clear (Clr) asynchronously resets the output.
4. Generate a Karnaugh map to derive the Boolean expression for Q+.
5. Implement the circuit using logic gates.
6. Simulate the circuit using a waveform testbench and verify the expected output behavior.
7. Capture a screenshot of the simulation.

### 1.3 Observations and Results
- The latch correctly stored and transferred data as expected.
- The asynchronous clear successfully reset the output regardless of the enable signal.
- The Karnaugh map simplifications matched the expected logic circuit implementation.

### 1.4 Conclusion
The designed D latch functioned correctly as a data storage element, demonstrating the importance of enable signals and asynchronous resets in sequential circuits. 

---

## Part 2: Design, Simulation, Verification, and Implementation of a D Flip-Flop with Asynchronous Clear

### 2.1 Theory
A **D flip-flop** is an edge-triggered device that stores and transfers data on a clock signal's rising or falling edge. Unlike latches, which are level-sensitive, flip-flops change state only during clock transitions, making them ideal for synchronous circuits. The design in this lab uses a **master-slave configuration**, which consists of two D latches.

### 2.2 Procedure
1. Develop a VHDL file named `D_FlipFlop.vhd`.
2. Construct the D flip-flop using two D latches in a master/slave arrangement.
3. Define at least four expected behavioral statements:
   - When the clock transitions from low to high, data is transferred from input D to output Q.
   - When the clock is low, Q retains its previous state.
   - An active-high asynchronous clear resets the output.
   - The flip-flop does not change state when the clock is stable.
4. Implement the design in VHDL (`D_FlipFlop` entity).
5. Simulate and verify that the flip-flop behaves according to the defined behavioral statements.
6. Capture a screenshot of the simulation.
7. Implement the design on an FPGA, mapping:
   - **Q** → LED
   - **D** → Switch
   - **Clock** → Switch
   - **Clr** → Switch
8. Verify the FPGA implementation against the simulated results.
9. Demonstrate functionality to the instructor or record a short video explaining the operation.

### 2.3 Observations and Results
- The D flip-flop successfully stored and transferred data on the rising clock edge.
- The asynchronous clear functioned independently of the clock.
- The master-slave configuration ensured proper synchronization of data transfer.
- The FPGA implementation matched the simulated results, confirming the correct functionality of the circuit.

### 2.4 Conclusion
The experiment demonstrated the difference between latches and flip-flops, emphasizing the importance of clock signals in sequential circuits. The successful FPGA implementation validated the theoretical design, reinforcing the practical applications of D flip-flops in memory storage and data synchronization.

---

## Summary and Final Thoughts
This lab provided hands-on experience in designing, simulating, and implementing digital storage elements. The comparison between latches and flip-flops highlighted their distinct functionalities, showing how flip-flops are crucial in synchronous circuit design. The simulation results aligned with theoretical expectations, and the FPGA implementation successfully demonstrated real-world applicability.

Future improvements could include:
- Extending the design to include JK or T flip-flops.
- Implementing synchronous reset and preset features.
- Testing the design under varying clock frequencies for performance analysis.

### Files in Repository
- `D_Latch.vhd` – VHDL code for the D latch
- `D_FlipFlop.vhd` – VHDL code for the D flip-flop
- Simulation screenshots (to be added)


---

