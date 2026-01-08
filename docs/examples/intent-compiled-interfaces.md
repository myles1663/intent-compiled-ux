# Intent-Compiled Interfaces

> This is a working thesis. It is intentionally incomplete and subject to change. It exists to attract critique, not consensus.

### A Foundational Position on Generative UX




---

## Preamble

Software is entering a phase where behavior is no longer fully deterministic, user intent is no longer stable, and the “correct” interface cannot always be known in advance.

Despite this shift, most application builders — including those labeled “AI first” — remain grounded in interaction models designed for static systems. AI is treated as an assistant layered onto predetermined screens, rather than as a participant in deciding *what the interface should be at all*.

This document argues that a growing class of applications cannot be expressed cleanly within that model.


Not because current tools are poorly executed — but because they are built on assumptions that no longer hold.

## Execution Model

This repository also defines a minimal execution model for Generative UX systems.  
See: [The Intent Runtime Loop](docs/intent-runtime-loop.md)

---

## 1. The Fracture

Modern application builders assume that the primary unit of experience is a **screen**: a predefined composition of components, connected by routes, rendered consistently across users and sessions.

This approach works when:

* User intent is stable
* Outcomes are known in advance
* The system’s role is to execute predefined workflows

It begins to fail in a specific and increasingly common class of applications:  
**systems where intent is fluid, credibility must be earned, and the correct experience emerges through interaction rather than execution.**

In these systems, the problem is not that structure is impossible — it is that **the information required to choose the right structure does not exist at build time**.

Yet current tools still require builders to:

* Commit to layouts early
* Encode interaction paths statically
* Treat AI as a content generator inside predetermined containers

When builders attempt to create adaptive experiences within these constraints, the result is predictable:

* Exploding conditional logic
* Template sprawl
* Interfaces that grow more complex as the system learns more

Instead of collapsing as understanding increases, the UI accumulates features.

This is not a failure of discipline.  
It is a consequence of tooling that assumes interfaces must exist *before* interaction begins.

---

## 2. The Reframe: From Screens to Responsive Intent

Traditional application design treats the interface as the primary artifact and the user as a navigator of that artifact.

Generative UX inverts this relationship.

In intent driven systems, the system’s primary responsibility is not to present functionality, but to **reduce user uncertainty and increase confidence toward a decision or understanding**.

Users in these systems do not move linearly through flows. They probe, test assumptions, hesitate, validate, and reassess. Two users with the same role may require entirely different experiences to reach the same outcome.

This is especially evident in credibility driven domains.  
For example, two CFOs evaluating the same product may share a title but differ radically in:

* Risk tolerance
* Prior experience
* Internal constraints
* Trust thresholds

Template based systems treat these users as variants of the same persona.  
Intent driven systems treat them as **distinct epistemic states**.

In a Generative UX model:

* The system observes how a user engages
* Infers what they appear uncertain about
* Assembles an experience that responds to *that uncertainty*, not to a static persona definition

The interface becomes a **runtime artifact** — assembled to serve the current intent, reshaped as confidence changes, and collapsed as understanding solidifies.

Minimalism, in this model, is not a stylistic goal.  
It is a *byproduct of certainty*.

When the system understands the user, it naturally says less.

---

## 3. Why Existing Builders Cannot Simply Evolve

It is tempting to believe that current app builders could support Generative UX through incremental additions: smarter templates, AI assisted layouts, or more powerful conditional rendering.

In practice, these approaches fail because existing builders are architected around assumptions that are incompatible with intent driven systems.

**First, structure is committed too early.**  
Most builders require screens, routes, and component trees to exist prior to interaction. Conditional rendering can hide elements, but the underlying structure remains pre committed.

Generative UX requires the opposite:  
**structure must be chosen after context emerges, not assumed beforehand.**

Retrofitting deferral into early‑commit systems leads to:

* Fragile logic
* Poor debuggability
* Experiences that feel adaptive but behave inconsistently

**Second, state models are UI centric rather than epistemic.**  
Existing tools track application state and interface state, but do not model:

* User confidence
* Uncertainty
* Trust accumulation
* Information redundancy

Without these as first‑class state, systems can only decide what to add — not what to remove.

As a result, AI features tend to increase verbosity rather than clarity.

**Third, AI is positioned as a helper rather than a decision participant.**  
In most builders, AI generates content within fixed containers. It does not decide:

* Which interaction is necessary
* Which information is redundant
* Which interface elements should not exist at all

Generative behavior is layered on top of static foundations that were never designed to adapt.

**Finally, explainability degrades as adaptivity increases.**  
As conditional logic grows, it becomes increasingly difficult to answer a fundamental question:

> “Why did the system show this to this user at this moment?”

In intent driven systems, this question is not optional.  
If behavior cannot be explained deterministically, trust collapses — especially in high‑stakes domains.

These limitations are not missing features.  
They are consequences of foundational design choices.

Incremental evolution reinforces the assumptions that Generative UX requires us to abandon.

---

## 4. The Non Negotiables

The following are not preferences.  
They are requirements for any system that claims to support Generative UX.

---

### 4.1 Deferred Structure Is Mandatory

Interface structure must be deferrable until runtime, selected based on observed context rather than predefined flows.

This does not imply the absence of structure.  
It implies **structure is chosen, not assumed**.

The system must be able to:

* Assemble interfaces from intent rather than routes
* Omit entire interaction patterns when unnecessary
* Recompose as confidence increases

Any builder that requires screens or layouts to exist prior to interaction will eventually collapse into conditional complexity.

---

### 4.2 Confidence and Uncertainty Are First Class State

The system must explicitly model:

* What the user appears confident about
* What remains uncertain
* How that uncertainty changes over time

This epistemic state must be:

* Queryable by composition logic
* Addressable by the runtime
* Explainable after the fact

Without it, the system has no principled way to decide what to compress, remove, or replace with evidence.

Generative UX is not about showing more information.  
It is about showing **only what is still necessary**.

---

### 4.3 Composition Must Be Deterministic and Explainable

AI may participate in composition, but system behavior must always be traceable.

The system must be able to answer:

> “Why did this experience take this shape for this user at this moment?”

This requires:

* Clear boundaries between probabilistic inference and deterministic rules
* Traceable decision paths
* Versioned behavior over time

If behavior cannot be explained, it cannot be trusted.  
If it cannot be trusted, it will not be adopted.

---

### 4.4 Adaptation Must Earn Trust

Generative UX must bias toward clarity before personalization.

Early interactions should:

* Favor predictable structure
* Minimize surprise
* Establish system intent

Only as trust is earned should the system:

* Increase adaptivity
* Reduce visible structure
* Collapse interaction surfaces

Personalization without trust feels chaotic.  
Minimalism without understanding feels incomplete.

---

### 4.5 The UI Is a Runtime Artifact

In intent driven systems, the UI is not designed once and shipped.

It is:

* Assembled
* Evaluated
* Collapsed
* Reassembled

The builder’s role is not to design screens, but to define:

* Intent boundaries
* Constraint systems
* Acceptable behaviors

Any platform that treats UI as a static asset — even a dynamically filled one — cannot fully support this model.

---

### 4.6 Minimalism Is an Outcome, Not a Goal

Minimal interfaces should emerge naturally as the system gains confidence in the user’s understanding.

If the system remains verbose, it is not a design failure — it is a signal that uncertainty remains.

Minimalism becomes a diagnostic indicator, not an aesthetic target.

---

## 5. The Invitation

This document is not a product announcement, a hiring pitch, or a roadmap.

It is a working position.

The goal is to explore whether a new class of application builder — one designed around intent, uncertainty, and deferred structure — is not only possible, but necessary.

This work is early, unpolished, and intentionally constrained.

It is for builders who are less interested in shipping faster — and more interested in building systems that **could not exist before**.

---
