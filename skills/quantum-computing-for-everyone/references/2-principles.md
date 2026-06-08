# 2 — Key Principles

> Source: *Quantum Computing for Everyone* by Chris Bernhardt.

## The 7 Principles

### 1. A Qubit Is a Unit Vector in Complex 2-Space

The precise mathematical definition: a qubit is a unit vector in ℂ², written as α|0⟩ + β|1⟩ where |α|² + |β|² = 1. Measurement yields |0⟩ or |1⟩ probabilistically. The superposition is not "both at once" — it's a well-defined mathematical state with measurable properties.

> **Case: Quantum Key Distribution (Chapter 3):** The BB84 protocol (Bennett and Brassard, 1984) uses qubits to generate a shared secret key between two parties. Any eavesdropper's measurement inevitably disturbs the qubits, revealing their presence. BB84 is provably secure — a property impossible with classical key distribution.

### 2. Measurement Destroys Superposition

Once you measure a qubit, it collapses to a classical bit. You cannot "observe" a quantum computation without disrupting it. This is why quantum algorithms are designed so that the correct answer emerges with high probability — you don't need to measure intermediate states.

### 3. Entanglement Is Correlation Without Communication

Measuring one entangled qubit determines the other. But this cannot transmit information faster than light — the outcomes are correlated but random until compared. Quantum teleportation uses entanglement plus classical communication to transfer a qubit state. No faster-than-light communication is possible.

### 4. Quantum Gates Are Unitary Matrices

All quantum operations are reversible (unitary). The Hadamard gate creates superposition. The CNOT gate entangles. The Pauli gates (X, Y, Z) act like rotations. Unlike classical AND/OR gates (which lose information), quantum gates preserve information.

### 5. Quantum Speedup Requires Specific Structure

Most problems have no quantum advantage. Speedup comes from exploiting mathematical structure: periodicity (Shor), amplitude amplification (Grover), or evaluating functions in superposition (Deutsch-Jozsa). Random brute-force problems gain nothing.

### 6. Quantum Computing Is Not Hardware-Dependent

> **Case: The No-Cloning Theorem (Chapter 7):** You cannot copy an unknown quantum state. This is a mathematical theorem, not an engineering limitation. It has profound implications: quantum error correction requires specialized codes, and quantum key distribution is secure because eavesdroppers cannot copy qubits.

### 7. Post-Quantum Cryptography Is Being Developed

NIST has selected new encryption standards resistant to quantum attacks (lattice-based, hash-based). The transition will take a decade or more, but it is already underway.
