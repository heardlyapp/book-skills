# 3 — Techniques

> Source: *Quantum Computing for Everyone* by Chris Bernhardt.

## Practical Tools

### 1. The Qubit State Visualizer

A qubit α|0⟩ + β|1⟩ can be visualized on the Bloch sphere. The north pole is |0⟩. The south pole is |1⟩. Any point on the surface represents a valid superposition. The angles θ and φ determine the measurement probabilities and the relative phase. Hadamard gate = rotation to the equator.

> **Case: Hadamard Gate (Chapter 7):** The Hadamard gate H takes |0⟩ to (|0⟩+|1⟩)/√2 = a point on the equator of the Bloch sphere. This is a perfect superposition — 50% chance of measuring 0, 50% chance of measuring 1. Applying H again returns to |0⟩. H² = I.
> **Key takeaway**: The Hadamard gate is the most important single-qubit gate. It creates the uniform superposition that all quantum algorithms start with.

> **Case: The Fredkin Billiard-Ball Computer (Chapter 6):** Ed Fredkin designed a computer using only billiard balls colliding with each other and walls. The balls represent bits (present = 1, absent = 0). Collisions implement logical gates. This is a reversible, conservative computation model. Bernhardt includes it because it connects to Feynman's insight that led him to quantum computing: if classical reversible computation can be modeled with colliding balls, quantum versions would use wave-like behavior.
> **Key takeaway**: The billiard-ball computer is a beautiful bridge between classical and quantum computation. It shows that computation can be physical.

To create an entangled Bell state: (1) Apply Hadamard to the first qubit. (2) Apply CNOT with first qubit as control, second as target. Result: (|00⟩+|11⟩)/√2. This state is maximally entangled — measuring either qubit instantly determines the other.

### 3. The Quantum Teleportation Protocol

To teleport a qubit state from Alice to Bob: (1) Create a Bell pair between Alice and Bob. (2) Alice applies CNOT and Hadamard to her qubit and the unknown state. (3) Alice measures her two qubits, obtaining 2 classical bits. (4) Alice sends these 2 bits to Bob. (5) Bob applies the corresponding Pauli gates to his half of the Bell pair. Result: Bob's qubit now has the original state.

### 4. Grover's Algorithm in 4 Steps

(1) Prepare uniform superposition of all N states. (2) Apply the oracle (marks the correct answer by flipping its phase). (3) Apply the diffusion operator (amplitude amplification: reflects around the average). (4) Repeat steps 2-3 about √N times. Measurement yields the correct answer with high probability.

### 5. The BB84 Protocol in Steps

(1) Alice sends qubits randomly chosen from {|0⟩,|1⟩,|+⟩,|-⟩}. (2) Bob measures each qubit with randomly chosen basis. (3) Alice and Bob compare bases publicly, keeping only bits where bases matched. (4) They sacrifice some bits to check for eavesdropping. If error rate is low, the remaining bits form a secure key.
