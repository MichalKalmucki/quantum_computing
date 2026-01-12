Michał Kałmucki 151944

# Project 1 Report: Quantum Measurements in Different Bases

## Overview
This project demonstrates basic quantum measurements and measurements in different Pauli bases (X, Y, Z) using Qiskit. The experiments show how quantum states behave under various measurement conditions.

## Task 1: Basic Measurement
Measuring the default state |0⟩ of a qubit.

**Code Snippet:**
```python
n = 4
nx = n
qx = QuantumRegister(nx)
cx = ClassicalRegister(nx)
circuit = QuantumCircuit(qx, cx)
circuit.measure(qx[0], cx[0])
```

**Results:**
![Task 1 Results](outputs/task1_basic_measurement_results.png)

## Task 2: X Gate Measurement
Applying an X gate before measurement.

**Code Snippet:**
```python
qreg = QuantumRegister(4, 'q')
creg_c = ClassicalRegister(4, 'c')
circuit = QuantumCircuit(qreg, creg_c)
circuit.x(qreg[0])
circuit.measure(qreg[0], creg_c[0])
```

**Results:**
![Task 2 Results](outputs/task2_x_gate_results.png)

## Task 3: H Gate Measurement
Applying a Hadamard gate before measurement.

**Code Snippet:**
```python
qreg = QuantumRegister(4, 'q')
creg_c = ClassicalRegister(3, 'c')
circuit = QuantumCircuit(qreg, creg_c)
circuit.h(qreg[0])
circuit.measure(qreg[0], creg_c[0])
```

**Results:**
![Task 3 Results](outputs/task3_h_gate_results.png)

## Task 4: Measurements in Different Bases

### X Basis Measurement
Preparing the state |+⟩ and measuring in X basis.

**Code Snippet:**
```python
qreg = QuantumRegister(4, 'q')
creg_c = ClassicalRegister(4, 'c')
circuit = QuantumCircuit(qreg, creg_c)
circuit.ry(pi / 2, qreg[0])
circuit.p(pi / 2, qreg[0])
circuit.h(qreg[0])
circuit.measure(qreg[0], creg_c[0])
```

**Results:**
![Task 4 X Basis Results](outputs/task4_x_basis_results.png)

### Y Basis Measurement
Preparing the state |i⟩ and measuring in Y basis.

**Code Snippet:**
```python
qreg = QuantumRegister(4, 'q')
creg_c = ClassicalRegister(4, 'c')
circuit = QuantumCircuit(qreg, creg_c)
circuit.ry(pi / 2, qreg[0])
circuit.p(pi / 2, qreg[0])
circuit.sdg(qreg[0])
circuit.h(qreg[0])
circuit.measure(qreg[0], creg_c[0])
```

**Results:**
![Task 4 Y Basis Results](outputs/task4_y_basis_results.png)

### Z Basis Measurement
Measuring in the computational (Z) basis.

**Code Snippet:**
```python
qreg = QuantumRegister(4, 'q')
creg_c = ClassicalRegister(4, 'c')
circuit = QuantumCircuit(qreg, creg_c)
circuit.ry(pi / 2, qreg[0])
circuit.p(pi / 2, qreg[0])
circuit.measure(qreg[0], creg_c[0])
```

**Results:**
![Task 4 Z Basis Results](outputs/task4_z_basis_results.png)

## Conclusion
These experiments demonstrate the principles of quantum measurement in different bases, showing how the preparation of quantum states affects measurement outcomes. The results are visualized through histograms showing both count distributions and probability distributions across multiple runs.