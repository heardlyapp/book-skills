# Reference: System Design

## Overview
Conceptual integrity and the second-system effect are Brooks's most important contributions to system design.

## Case: Conceptual Integrity
A system must have a single, coherent vision. This is conceptual integrity. It is more important than having many innovative features. The architect (or small architectural group) must make all design decisions. The implementers must follow the design faithfully. Brooks argues that the best systems (IBM System/360 architecture, the original Macintosh) were designed by small groups with tight control.

## Case: The Second-System Effect
The second system a designer builds is the most dangerous. The designer tries to include everything they could not fit into the first system. They want to incorporate all the new techniques they have learned. The result is over-engineered, feature-bloated, and too complex. Brooks's advice: consciously restrain the second-system tendency.

## Case: The Architect Role
The architect must be independent of the implementation team. The architect designs what the system should do; the implementer decides how to do it. This separation is essential for conceptual integrity. The architect must have authority over design decisions, even when they conflict with implementation convenience.

## Case: The Pilot Project
Brooks recommends building a pilot (prototype) system first. This system is intended to be thrown away. The second system — the one that learns from the pilot — will be the production system. But guard against the second-system effect: keep it simple.

## Case: OS/360 Architecture
The IBM System/360 architecture was a triumph of conceptual integrity. A single architectural specification defined how all models of the family would work. This consistency was more important than including every possible feature.
