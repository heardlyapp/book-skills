# 4 — Anti-Patterns

> Source: *Quantum Computing for Everyone* by Chris Bernhardt.

## Common Errors

### 1. "Qubits Are Both 0 and 1 at the Same Time"

**The trap:** "A qubit is 0 AND 1 simultaneously — so a quantum computer checks all possibilities at once."

**Why it fails:** A qubit is not "both." It is a specific mathematical state α|0⟩ + β|1⟩ with well-defined coefficients. The popular description leads to the wrong intuition that quantum computers simply parallelize. Real quantum speedup requires interference — not just parallel evaluation. Without interference, quantum parallelism would be useless.

> **Case: Deutsch-Jozsa Algorithm (Chapter 8):** The first quantum algorithm to demonstrate a speedup. Deutsch-Jozsa determines whether a function is constant (same output for all inputs) or balanced (equal 0s and 1s) in ONE query — whereas classical computers need 2ⁿ⁻¹+1 queries. It does this not by "trying all inputs at once" but by using interference to cancel wrong answers and amplify the correct one.
> **Key takeaway**: Quantum advantage comes from interference, not parallelism. The cleverness is in how the algorithm is designed, not in how many states it can represent.

> **Case: The Three-Polarizer Paradox (Chapter 1):** Two crossed polarizers (0° and 90°) block all light. Adding a third at 45° between them lets light through. This is impossible classically — how can adding a filter make more light pass? The quantum explanation: the 45° filter changes the polarization state of the photons. This is a direct analogy to quantum measurement altering the state being measured.
> **Key takeaway**: If something seems paradoxical, the classical intuition is probably wrong. The three-polarizer paradox is the best intuition-builder for quantum measurement effects.

**The trap:** "Everything a classical computer can do, a quantum computer will do faster."

**Why it fails:** Quantum computers offer exponential speedup only for a small set of problems (factoring, search, simulation). For most computing tasks — word processing, databases, web servers, video streaming — there is no quantum advantage. The future is hybrid: classical computers running most tasks, with quantum co-processors for specific problems.

### 3. "Quantum Teleportation Teleports Matter"

**The trap:** "Quantum teleportation is like Star Trek — it teleports physical objects."

**Why it fails:** Quantum teleportation transfers the quantum STATE of a qubit, not the physical qubit itself. The original qubit is destroyed in the process. Teleportation also requires classical communication (two bits sent conventionally) — so it cannot happen faster than light.

### 4. "Entanglement Allows Faster-Than-Light Communication"

**The trap:** "Measuring one entangled qubit instantly affects the other — so we can communicate faster than light."

**Why it fails:** The measurement outcomes are random. Alice cannot choose what Bob will see. Bob cannot distinguish entangled correlations from random noise without classical information from Alice. No information is transmitted faster than light.

### 5. "Quantum Computers Are Just a Few Years Away"

**The trap:** "We'll have practical quantum computers by [current year + 5]."

**Why it fails:** Building a fault-tolerant quantum computer with millions of error-corrected qubits is an enormous engineering challenge. Current machines (2023-2025) have 100-1000 noisy physical qubits. Scaling to millions while controlling errors is likely a decade(s)-long effort. Quantum supremacy has been demonstrated for one narrow problem (Google, 2019) — but useful quantum advantage remains elusive.
