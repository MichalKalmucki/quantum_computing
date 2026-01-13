Michał Kałmucki 151944

# Lab 1 Report: Introduction to Quantum Computing

## Overview
This lab introduces basic quantum operations and measurements using Qiskit. The experiments demonstrate single-qubit gates, superposition, and measurements in different Pauli bases.

## Task 1: Z-type Projection Measurement
Basic measurement of the |0⟩ state in the computational basis.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 1 Circuit](outputs/task1_z_measurement_circuit.png)

**Probabilities Diagram:**
![Task 1 Histogram](outputs/task1_z_measurement_histogram.png)

Q-sphere Representation:
Q-sphere visualization not available (seaborn library issue).

## Task 2: X Gate Operation
Application of the X (NOT) gate followed by measurement.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.x(qreg[0])
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 2 Circuit](outputs/task2_x_gate_circuit.png)

**Probabilities Diagram:**
![Task 2 Histogram](outputs/task2_x_gate_histogram.png)

**Q-sphere Representation:**
Q-sphere visualization not available.

## Task 3: Hadamard Gate (Superposition)
Creation of superposition state using the H gate.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.h(qreg[0])
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 3 Circuit](outputs/task3_h_gate_circuit.png)

**Probabilities Diagram:**
![Task 3 Histogram](outputs/task3_h_gate_histogram.png)

**Q-sphere Representation:**
Q-sphere visualization not available.

## Task 4: State Tomography - Measurements in Different Bases

### X Basis Measurement
Measurement in the X (σ₁) basis.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.ry(pi/2, qreg[0])
circuit.p(pi/2, qreg[0])
circuit.h(qreg[0])
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 4 X Basis Circuit](outputs/task4_x_basis_circuit.png)

**Probabilities Diagram:**
![Task 4 X Basis Histogram](outputs/task4_x_basis_histogram.png)

**Q-sphere Representation:**
Q-sphere visualization not available.

### Y Basis Measurement
Measurement in the Y (σ₂) basis.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.ry(pi/2, qreg[0])
circuit.p(pi/2, qreg[0])
circuit.sdg(qreg[0])
circuit.h(qreg[0])
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 4 Y Basis Circuit](outputs/task4_y_basis_circuit.png)

**Probabilities Diagram:**
![Task 4 Y Basis Histogram](outputs/task4_y_basis_histogram.png)

**Q-sphere Representation:**
Q-sphere visualization not available.

### Z Basis Measurement
Measurement in the Z (σ₃) basis.

**Code Snippet:**
```python
qreg = QuantumRegister(1, 'q')
creg = ClassicalRegister(1, 'c')
circuit = QuantumCircuit(qreg, creg)
circuit.ry(pi/2, qreg[0])
circuit.p(pi/2, qreg[0])
circuit.measure(qreg[0], creg[0])
```

**Quantum Circuit:** \
![Task 4 Z Basis Circuit](outputs/task4_z_basis_circuit.png)

**Probabilities Diagram:**
![Task 4 Z Basis Histogram](outputs/task4_z_basis_histogram.png)

**Q-sphere Representation:**
Q-sphere visualization not available.
