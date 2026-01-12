Michał Kałmucki 151944

# Quantum Computing Lab 2 Report

## 1. Circuit Plots (Tasks 1-7)

### Bell State Circuits (Tasks 1-4)

#### Phi+ Circuit
![Phi+ Circuit](outputs/Phi+_circuit.png)

#### Phi- Circuit
![Phi- Circuit](outputs/Phi-_circuit.png)

#### Psi+ Circuit
![Psi+ Circuit](outputs/Psi+_circuit.png)

#### Psi- Circuit
![Psi- Circuit](outputs/Psi-_circuit.png)

### Measurement Circuits (Tasks 5-7)

#### Phi+ XX Measurement
![Phi+ XX Circuit](outputs/Phi+_XX_circuit.png)

#### Phi+ YY Measurement
![Phi+ YY Circuit](outputs/Phi+_YY_circuit.png)

#### Phi+ XZ Measurement
![Phi+ XZ Circuit](outputs/Phi+_XZ_circuit.png)

#### Phi- XX Measurement
![Phi- XX Circuit](outputs/Phi-_XX_circuit.png)

#### Phi- YY Measurement
![Phi- YY Circuit](outputs/Phi-_YY_circuit.png)

#### Phi- XZ Measurement
![Phi- XZ Circuit](outputs/Phi-_XZ_circuit.png)

#### Psi+ XX Measurement
![Psi+ XX Circuit](outputs/Psi+_XX_circuit.png)

#### Psi+ YY Measurement
![Psi+ YY Circuit](outputs/Psi+_YY_circuit.png)

#### Psi+ XZ Measurement
![Psi+ XZ Circuit](outputs/Psi+_XZ_circuit.png)

#### Psi- XX Measurement
![Psi- XX Circuit](outputs/Psi-_XX_circuit.png)

#### Psi- YY Measurement
![Psi- YY Circuit](outputs/Psi-_YY_circuit.png)

#### Psi- XZ Measurement
![Psi- XZ Circuit](outputs/Psi-_XZ_circuit.png)

## 2. Results Plots (Tasks 1-7)

### Bell State Results (Tasks 1-4)

#### Phi+ Histogram
![Phi+ Histogram](outputs/Phi+_histogram.png)

#### Phi- Histogram
![Phi- Histogram](outputs/Phi-_histogram.png)

#### Psi+ Histogram
![Psi+ Histogram](outputs/Psi+_histogram.png)

#### Psi- Histogram
![Psi- Histogram](outputs/Psi-_histogram.png)

### Measurement Results (Tasks 5-7)

#### Phi+ XX Histogram
![Phi+ XX Histogram](outputs/Phi+_XX_histogram.png)

#### Phi+ YY Histogram
![Phi+ YY Histogram](outputs/Phi+_YY_histogram.png)

#### Phi+ XZ Histogram
![Phi+ XZ Histogram](outputs/Phi+_XZ_histogram.png)

#### Phi- XX Histogram
![Phi- XX Histogram](outputs/Phi-_XX_histogram.png)

#### Phi- YY Histogram
![Phi- YY Histogram](outputs/Phi-_YY_histogram.png)

#### Phi- XZ Histogram
![Phi- XZ Histogram](outputs/Phi-_XZ_histogram.png)

#### Psi+ XX Histogram
![Psi+ XX Histogram](outputs/Psi+_XX_histogram.png)

#### Psi+ YY Histogram
![Psi+ YY Histogram](outputs/Psi+_YY_histogram.png)

#### Psi+ XZ Histogram
![Psi+ XZ Histogram](outputs/Psi+_XZ_histogram.png)

#### Psi- XX Histogram
![Psi- XX Histogram](outputs/Psi-_XX_histogram.png)

#### Psi- YY Histogram
![Psi- YY Histogram](outputs/Psi-_YY_histogram.png)

#### Psi- XZ Histogram
![Psi- XZ Histogram](outputs/Psi-_XZ_histogram.png)

## 3. Mathematical Calculations (Tasks 2-4)

### Matrix Form (Task 2: Phi-)
**Matrices used:**

$$ H = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}, \quad Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}, \quad I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} $$

$$ H \otimes I = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 0 & 1 & 0 \\ 0 & 1 & 0 & 1 \\ 1 & 0 & -1 & 0 \\ 0 & 1 & 0 & -1 \end{pmatrix} $$

$$ Z \otimes I = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1 \end{pmatrix} $$

$$ CX = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix} $$

**Derivation:**

Starting from the initial state:
$$ |00\rangle = \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix} $$

Apply H ⊗ I:
$$ (H \otimes I) |00\rangle = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 0 & 1 & 0 \\ 0 & 1 & 0 & 1 \\ 1 & 0 & -1 & 0 \\ 0 & 1 & 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} $$

Apply Z ⊗ I:
$$ (Z \otimes I) \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \end{pmatrix} $$

Apply CNOT (CX):
$$ \text{CX} \cdot \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 0 \\ 0 \\ -1 \end{pmatrix} $$

Final state:
$$ |\Phi^-\rangle = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ 0 \\ 0 \\ -\frac{1}{\sqrt{2}} \end{pmatrix} $$

### Operator Form (Task 3: Psi+)
**Derivation:**

Starting from |00⟩.

Apply H ⊗ I:
$$ (H \otimes I) |00\rangle = \frac{1}{\sqrt{2}} (|00\rangle + |10\rangle) $$

Apply CX:
$$ \text{CX} \cdot \frac{1}{\sqrt{2}} (|00\rangle + |10\rangle) = \frac{1}{\sqrt{2}} (|00\rangle + |11\rangle) $$

Apply I ⊗ X:
$$ (I \otimes X) \cdot \frac{1}{\sqrt{2}} (|00\rangle + |11\rangle) = \frac{1}{\sqrt{2}} (|01\rangle + |10\rangle) $$

Final state:
$$ |\Psi^+\rangle = \begin{pmatrix} 0 \\ \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} \\ 0 \end{pmatrix} $$

### Operator Form (Task 4: Psi-)
**Derivation:**

Starting from |00⟩.

Apply H ⊗ I:
$$ (H \otimes I) |00\rangle = \frac{1}{\sqrt{2}} (|00\rangle + |10\rangle) $$

Apply Z ⊗ I:
$$ (Z \otimes I) \cdot \frac{1}{\sqrt{2}} (|00\rangle + |10\rangle) = \frac{1}{\sqrt{2}} (|00\rangle - |10\rangle) $$

Apply CX:
$$ \text{CX} \cdot \frac{1}{\sqrt{2}} (|00\rangle - |10\rangle) = \frac{1}{\sqrt{2}} (|00\rangle - |11\rangle) $$

Apply I ⊗ X:
$$ (I \otimes X) \cdot \frac{1}{\sqrt{2}} (|00\rangle - |11\rangle) = \frac{1}{\sqrt{2}} (|01\rangle - |10\rangle) $$

Final state:
$$ |\Psi^-\rangle = \begin{pmatrix} 0 \\ \frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}} \\ 0 \end{pmatrix} $$