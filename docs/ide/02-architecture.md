# IDE Architecture Overview
> **Note:** All components described here live inside the generated application runtime, not the IDE.

This IDE is composed of **explicit subsystems** with hard boundaries.

---

## Core Components

### Intent Engine
- parses signals
- emits intent objects
- tracks uncertainty

### Context Graph Builder
- aggregates knowledge
- tracks provenance
- applies decay

### Composition Engine
- selects UI primitives
- assembles structure
- emits rationale

### Renderer
- deterministic
- constrained
- explainable

### Runtime Monitor
- collects signals
- feeds memory

### Memory System
- relevance-based recall
- decay over time
- no global context stuffing

---

## Design Constraints

- Every decision must be explainable
- Every output must be reproducible
- No hidden state
- No silent overrides

---

## Non-Goals

- Fully autonomous agents
- Opaque reasoning
- Template-based UI masquerading as generative
