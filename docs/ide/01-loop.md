# IDE Runtime Loop
> **Note:** This loop describes the behavior of the **generated application at runtime**, not the IDE.


This document defines the **canonical runtime loop** of the Generative UX App IDE.

This loop governs how intent becomes interface — repeatedly, safely, and explainably.

---

## High-Level Loop

1. Intent Capture
2. Context Construction
3. Composition Planning
4. Deterministic Rendering
5. Runtime Instrumentation
6. Memory & Confidence Update
7. Next Question Generation

---

## 1. Intent Capture

Input:
- explicit user statements
- interaction signals
- hesitation, revision, abandonment

Output:
- typed Intent Object
- confidence score
- unresolved variables

---

## 2. Context Construction

Inputs:
- intent object
- prior sessions
- external data (optional)

Output:
- Context Graph
  - sources
  - timestamps
  - confidence weights
  - decay rules

---

## 3. Composition Planning

The system generates a **UI Composition Plan**, not UI code.

Includes:
- required blocks
- ordering
- dependencies
- justification for each element

This plan is inspectable.

---

## 4. Deterministic Rendering

A constrained renderer turns the plan into UI.

Rules:
- no hallucinated components
- no free-form layout
- only approved primitives

Same plan → same UI.

---

## 5. Runtime Instrumentation

The runtime captures:
- interactions
- dwell time
- corrections
- abandonments

These are signals, not analytics vanity metrics.

---

## 6. Memory & Confidence Update

Updates:
- intent confidence
- context relevance
- block usefulness

Old assumptions decay.

---

## 7. Next Question Generation

The system decides:
- what uncertainty remains
- what question would reduce it most

Then the loop repeats.
