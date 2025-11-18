# Quantum Dice Simulator

# Author: Jenisha Baral

# Executive Summary

This project demonstrates how a quantum circuit can be used to simulate the rolling of a dice. The goal was to use the principles of quantum superposition and random measurement to generate the outcomes of dice, 1 to 6, with nearly uniform probability.

# Circuit Design

3-qubit quantum circuit was used, because 3 qubits can represent binary numbers from 0 to 7. Hadamard gates (H) were applied to all three qubits to create superposition, which means each qubit is in the state of 0 and 1 at the same time. Combining all three qubits, represents all number from 0 to 7 simultaneously.

The qubits were then measured into 3 classical bits, removing the superposition state into a specific binary output (000 to 111).

# Dice Mapping Logic

Because a dice only has 6 values, but 3 qubits produce 8 values, the following method was used:
If the measured binary number is 0 to 5, it directly maps to dice outcomes 1 to 6.
If the number is 6 or 7, it is invalid for a dice, so the code reruns the circuit until a number below 6 appears.
This ensures that every output is valid for dice.

# Simulation and Results

Using Qiskit’s AerSimulator, the circuit was executed 1000 times. Each execution represents one rolling of dice. 
A dictionary recorded the count of each outcome from 1 to 6.

The final results were displayed in a bar graph, which showed that the distribution is nearly uniform.
This confirms that the quantum superposition based method behaves like an ideal random dice generator.


# Conclusion

This project successfully shows how quantum randomness can be used for simple simulations.
Even though the circuit is small and easy to understand, it captures the core ideas of quantum superposition, measurement, and randomness, making it an excellent introductory example of quantum applications.
