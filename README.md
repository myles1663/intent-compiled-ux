# Generative UX App IDE

This repository contains the **Generative UX App IDE**, a new kind of application builder where interfaces are generated at runtime from user intent instead of predefined screens and routes.

Unlike traditional UI frameworks, this IDE treats **intent** and **uncertainty** as first-class state. It compiles UI structures only after understanding what the user is trying to achieve, and produces explainable, deterministic interfaces backed by an instrumented runtime.

## What is in this repo?

- **IDE Specification** – The core design and architecture of the IDE lives in [`docs/ide`](docs/ide/00-vision.md). Start with the [Vision](docs/ide/00-vision.md) and [Runtime Loop](docs/ide/01-loop.md) documents to understand why and how this IDE works.
- **Architecture and Debugging** – See [`docs/ide/02-architecture.md`](docs/ide/02-architecture.md) for a breakdown of components and [`docs/ide/05-debug.md`](docs/ide/05-debug.md) for debugging guidance.
- **Examples** – Sample apps and runtime loop documents live under [`docs/examples`](docs/examples). These demonstrate what the IDE can compile, but they are not the IDE itself.

## Getting started

The IDE is in an early design phase. If you want to contribute or follow along:

1. Read the [Vision](docs/ide/00-vision.md) to understand the goals of Generative UX.
2. Review the [Runtime Loop](docs/ide/01-loop.md) and [Architecture Overview](docs/ide/02-architecture.md).
3. Explore [`docs/examples`](docs/examples) for concept app loop specs.
4. Join the discussion via issues or pull requests.

---

The original thesis on Generative UX lives in [`docs/examples/intent-compiled-interfaces.md`](docs/examples/intent-compiled-interfaces.md).
