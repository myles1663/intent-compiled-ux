> This is a working execution model. It is intentionally incomplete and subject to change.  
> It exists to be stress-tested, challenged, and refined.

# The Intent Runtime Loop
### A Minimal Execution Model for Generative UX

> This document defines the smallest repeatable loop required to support intent-compiled interfaces.  
> It is intentionally incomplete and intended to be stress-tested.

## The Core Claim (explicit)

A Generative UX system is not driven by screens, routes, or flows.

It is driven by a **continuous loop** that answers one question repeatedly:

> "What is the minimum interaction required right now to reduce uncertainty?"

Everything else is implementation detail.

## The Loop (high level)

Every interaction cycle follows the same sequence:

1. **Observe**
2. **Update Epistemic State**
3. **Select Dominant Uncertainty**
4. **Choose Minimum Interaction**
5. **Compose Interface**
6. **Explain (Internally)**
7. **Repeat**

If any step is skipped, the system collapses back into UI-first behavior.

## 1. Observe

The system observes **interaction signals**, not just actions.

This includes:
- Text input
- Choice selection
- Hesitation
- Revision
- Abandonment
- Return patterns

**Key constraint:**  
Observation does *not* infer meaning.  
It only captures **signals**.

> The system does not decide *what the user means*.  
> It decides *what remains unclear*.

### ⚠️ Challenge
If observation becomes semantic interpretation, the system becomes presumptive and brittle.

## 2. Update Epistemic State

The system maintains an **epistemic state** representing what appears to be understood versus uncertain.

At minimum, this includes:
- Confidence estimates
- Uncertainty dimensions
- Change over time

Example (conceptual, not prescriptive):

```
{
  "confidence": {
    "problem_definition": 0.4,
    "cause_clarity": 0.2,
    "agency": 0.6
  }
}
```

This state is:
- Mutable
- Conservative
- Recoverable

**Critical rule**  
Confidence should rise **slowly** and fall **quickly**.

### ⚠️ Challenge
Overconfident systems collapse UI too early and erode trust.

## 3. Select Dominant Uncertainty

At any moment, multiple uncertainties exist.

The system must select **one** to address.

Selection criteria:
- Blocks forward progress
- Appears most salient
- Has the highest potential information gain

> The system never tries to resolve everything at once.

### ⚠️ Challenge
If multiple uncertainties are addressed simultaneously, the UI grows instead of collapses.

## 4. Choose the Minimum Interaction

The system chooses the **smallest possible interaction** that could reduce the selected uncertainty.

This might be:
- A binary choice
- A clarifying question
- A reflective prompt
- A request for confirmation

It is **never**:
- A plan
- A dashboard
- A feature set

> Interaction is treated as an experiment, not a commitment.

### ⚠️ Challenge
If interactions demand commitment too early, users disengage.

## 5. Compose the Interface

Only now does the system assemble UI.

Composition rules:
- Include only elements required for the chosen interaction
- Omit all others
- Prefer fewer elements over richer ones

The interface is:
- Ephemeral
- Disposable
- Context-specific

> The UI exists to serve the loop — not the other way around.

## 6. Explain (Internally)

Every composition decision is logged internally.

The system must be able to answer:
- What uncertainty was targeted?
- Why this interaction was chosen?
- What signals informed the choice?

This explanation is:
- Deterministic
- Versioned
- Inspectable

### ⚠️ Challenge
Without internal explainability, debugging and governance become impossible.

## 7. Repeat

The loop repeats until:
- Uncertainty is sufficiently reduced
- A decision threshold is crossed
- The user disengages

Importantly:
- The loop may **end without action**
- Resolution is not mandatory

> Sometimes clarity is the outcome.

## Why This Loop Matters

This loop ensures that:

- Structure is deferred by default
- Minimalism emerges naturally
- Adaptation is earned, not assumed
- AI participates in decisions without controlling outcomes
- UI complexity trends downward over time

Most importantly:

> **The system cannot grow arbitrarily complex without violating the loop.**

That is the guardrail missing from existing builders.

## Where this is strong

- It is simple enough to reason about
- It aligns directly with Sherpa
- It explains *why* templates fail
- It provides a foundation for tooling

## Where this is still vulnerable (on purpose)

- Signal selection is underspecified
- Confidence scoring is abstract
- No governance UI is defined yet

These are not omissions — they are **pressure points**.

## The fork we’re at now (pay attention)

You now have:

1. A foundational thesis
2. A concrete runtime loop
3. A real use-case stress test

This is the point where most people:
- either start coding blindly
- or stall in abstraction

There is a **right next move**.

## My recommendation for the next step

Next, we should design **the Debug View**.

Not the user UI.  
The *builder’s* UI.

If this system can’t be debugged, it can’t exist.

The Debug View will answer:
- “What does the system think is uncertain?”
- “Why did it ask this?”
- “What would it do next if X happened?”

If you’re aligned, say:
> **“Let’s design the Debug View.”**

And we keep going — cleanly.
