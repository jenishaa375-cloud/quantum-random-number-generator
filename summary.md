# Quantum Dice Simulator — Executive Summary

# Author: Jenisha Baral
# Project: Simulating a Dice Roll Using Quantum Superposition

# Executive Summary

This project demonstrates how a simple quantum circuit can be used to simulate the rolling of a dice. The goal was to use the principles of quantum superposition and random measurement to
generate outcomes from 1 to 6 with nearly uniform probability.

# Circuit Design

I used a 3-qubit quantum circuit, because 3 qubits can represent binary numbers from 0 to 7.

Hadamard gates (H) were applied to all three qubits.

This creates superposition, meaning each qubit is in state 0 and 1 at the same time.

Combined, the three qubits represent all numbers from 0 to 7 simultaneously.

The qubits were then measured into 3 classical bits, collapsing the quantum state into a specific binary output (000 to 111).

# Dice Mapping Logic

Because a dice only has 6 values, but 3 qubits produce 8 values, I used the following method:

If the measured binary number is 0 to 5, it directly maps to dice outcomes 1 to 6.

If the number is 6 or 7, it is invalid for a dice, so the code reruns the circuit until a number below 6 appears.

This ensures that every dice output is generated from a valid quantum measurement.

# Simulation and Results

Using Qiskit’s AerSimulator, the circuit was executed 1000 times, each representing one roll of the dice.

A dictionary recorded the count of each outcome from 1 to 6.

The final results were displayed in a bar graph, showing that the distribution is nearly uniform.
This confirms that the quantum superposition–based method behaves like an ideal random dice generator.


# Conclusion

This project successfully shows how quantum randomness can be used for simple simulations.
Even though the circuit is small and easy to understand, it captures the core ideas of quantum computation—superposition, measurement, and randomness—making it an excellent introductory example of quantum applications.
