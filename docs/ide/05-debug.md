# Debug & Triage Guide
> **Note:** This guide covers debugging the generated application runtime, not the IDE.

This document exists to make failure visible.

## Common Failure Modes

### UI Feels Random
Likely causes:
- weak composition constraints
- missing deterministic anchors

### Repeated Stale Output
Likely causes:
- context decay not applied
- retrieval cache too aggressive

### Token Overruns
Likely causes:
- context graph not pruning
- over-verbose composition rationale

### Confident but Wrong
Likely causes:
- missing provenance
- no confidence penalty on weak sources

## Golden Signals

- intent confidence delta
- composition stability
- time-to-first-meaningful-action
- user correction rate

## Reproduction Protocol

To debug a run, capture:
- intent object
- context snapshot
- composition plan
- renderer version
- random seed (if any)

Replays must be possible.

## Triage Checklist

1. Is the intent object correct?
2. Is context current and relevant?
3. Did composition rules fire?
4. Did the renderer obey constraints?
5. Did memory update correctly?
