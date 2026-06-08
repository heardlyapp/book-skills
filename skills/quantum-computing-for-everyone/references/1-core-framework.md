# 1 — Core Framework

> Source: *Quantum Computing for Everyone* by Chris Bernhardt — Chapters 1-9.

## The Three Frameworks

### Framework A: Qubits, Superposition, and Measurement (Chapters 1, 3)

The qubit is the fundamental unit of quantum computing. Unlike a classical bit (0 or 1), a qubit exists in a superposition: α|0⟩ + β|1⟩, where |α|² + |β|² = 1. Measurement collapses this superposition to either |0⟩ (with probability |α|²) or |1⟩ (with probability |β|²). The act of measurement changes the qubit — you cannot "look" at a qubit without disturbing it.

> **Case: The Stern-Gerlach Experiment (Chapter 1):** Otto Stern and Walther Gerlach (1922) fired silver atoms through a magnetic field. Classical physics predicted a continuous spread. Instead, the atoms split into exactly two discrete beams, corresponding to spin up and spin down. This quantized outcome was the first experimental evidence of quantum spin — and the physical basis of the qubit. Measuring spin in different directions produces probabilistic results depending on the angle.

> **Case: Polarization Filters (Chapter 1, 3):** Bernhardt uses polarized light to demonstrate quantum behavior. Two polarized squares with the same orientation pass all light. Two with perpendicular orientations pass none. But three squares at 0°, 45°, and 90° produce a paradox: adding the middle filter (45°) allows light to pass through a system that previously blocked all light. This is a direct analogy to quantum measurement: the act of measuring at 45° changes the state of the photons.

### Framework B: Entanglement and Bell's Inequality (Chapters 4, 5)

Two qubits can be entangled: their combined state cannot be described as a product of individual states. The Bell state (|00⟩ + |11⟩)/√2 is the simplest example. Measuring the first qubit instantly determines the second, regardless of distance. Einstein called this "spooky action at a distance" and proposed hidden variable theories as an alternative.

> **Case: Bell's Inequality (Chapter 5):** John Bell (1964) proved mathematically that if local hidden variables existed, the measurement statistics must satisfy a specific inequality. Alain Aspect (1982) and later experiments showed that this inequality is violated — confirming that quantum mechanics is correct and local realism is false. Bernhardt walks through the math step by step, showing how Bell's inequality is derived and how experiments disprove it. For this work, Aspect, Clauser, and Zeilinger won the 2022 Nobel Prize in Physics.

### Framework C: Quantum Algorithms — Shor and Grover (Chapters 8, 9)

Quantum algorithms achieve speedup by exploiting superposition (computing with all possible inputs simultaneously), entanglement (correlations that classical bits cannot replicate), and interference (amplifying correct answers and canceling wrong ones). The two most important algorithms are Shor's (factoring) and Grover's (search).

> **Case: Shor's Algorithm (Chapter 9):** Peter Shor (1994) showed that a quantum computer could factor an N-bit number in O(N³) time — exponentially faster than the best classical algorithms (O(exp(N⅓))). Since RSA encryption relies on the difficulty of factoring large numbers, Shor's algorithm threatens all current public-key cryptography. A sufficiently large quantum computer could break RSA-2048 in hours.
