# Techniques & Tools

> Source: *Lean Thinking* by James P. Womack & Daniel T. Jones, Parts II & III

## Core Lean Tools

### 1. Value Stream Mapping (VSM)

The essential diagnostic tool. Draw the current state of every step in the value stream for a product family. Then design the future state.

| Element | Current State | Future State (Lean) |
|---------|---------------|---------------------|
| Process steps | By department | By product sequence |
| Material flow | Batch & queue | Continuous / pull |
| Information flow | Push from forecasts | Pull from actual demand |
| Lead time | Weeks or months | Days or hours |
| Value-added ratio | 1–5% | 50%+ |

**How to do it:** Walk the actual process. Time every step. Count every inventory buffer. Map information flows. The process itself is the revelation.

> **Case: Pratt & Whitney** (Chapter 2): VSM revealed that P&W's jet engine value stream involved 14+ independent companies and 3+ months of lead time for a part with days of actual processing. The future-state map showed that co-locating processes and aligning schedules could cut 90% of the lead time.

### 2. Cellular Manufacturing

Instead of grouping machines by type (all grinders together, all presses together), arrange them in **U-shaped cells** in process sequence. Each cell produces a product family from start to finish.

- Reduces transport and waiting to zero
- Allows one operator to run multiple machines
- Exposes quality problems immediately (no buffer inventory)
- Cuts floor space by 30–50%

> **Case: Pratt & Whitney** (Chapter 3): P&W replaced a fully automated grinding system for turbine blades (costly, slow, inflexible) with a simple U-shaped cell designed by its own engineers. The cell cost a quarter of the old system, cut production costs in half, reduced throughput time by 99%, and slashed changeover time from hours to seconds.

### 3. SMED (Single-Minute Exchange of Die)

Reducing changeover/setup time to under 10 minutes is critical for small-lot production and continuous flow.

**Technique:**
- Separate internal setup (must stop machine) from external setup (can do while machine runs)
- Convert internal to external wherever possible
- Standardize and simplify remaining steps
- Practice changes until they are routine

### 4. 5S Workplace Organization

A foundational technique for visual control and waste elimination:

| S | Japanese | Meaning |
|---|----------|---------|
| 1 | Seiri | Sort — keep only what's needed |
| 2 | Seiton | Set in order — a place for everything |
| 3 | Seiso | Shine — clean and inspect |
| 4 | Seiketsu | Standardize — make it routine |
| 5 | Shitsuke | Sustain — maintain through discipline |

### 5. Kanban / Pull Signals

A simple visual system to signal upstream production:

- **Withdrawal kanban**: authorizes movement of parts from one stage to the next
- **Production kanban**: authorizes production of a specific quantity
- Rules: No cards → no production. Defects never go downstream. Level the schedule.

### 6. Andon

A visual signal (light, board, or display) that surfaces problems immediately. When an operator encounters an issue, they pull the andon cord — production stops or alerts, and help arrives. Creates **instant feedback** and prevents defects from flowing downstream.

> **Case: Toyota** (throughout): Toyota's andon system is the ultimate transparency tool. Any worker can stop the line. This forces immediate problem-solving instead of sweeping issues under the inventory rug.

## The Action Plan (Chapter 11)

Womack & Jones' practical 10-step plan for starting a lean transformation:

1. Find a **change agent** — a leader who owns the transformation
2. Get **lean knowledge** — learn from someone who has done it
3. Find a **crisis** to leverage — or create one
4. Map the **value streams** — ignore existing organizational structure
5. Start with something **quick and visible** — pick one product family
6. Create a **kaizen plan** — schedule the first kaikaku events
7. Set up **cells for flow** — reorganize immediately
8. Install **pull systems** — kanban for replenishment
9. **Extend** lean to suppliers and distributors
10. Create a **lean promotion office** to sustain and spread
