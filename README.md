# Aether

> 🚧 Early development

Aether is a **high-throughput, distributed, fault-tolerant workflow execution engine being built in Go**.

The project explores how workflow systems should be designed, implemented, verified, and operated when the system has to remain correct and useful despite concurrency, failures, retries, restarts, partial progress, and changing load.

This repository is intentionally public from the beginning.

There is no production implementation yet. The system is being built incrementally, with requirements, design decisions, invariants, experiments, benchmarks, and failure investigations documented alongside the implementation.

---

## Why Aether?

Workflow execution looks straightforward until the system has to answer questions such as:

* What does it mean for a workflow step to have actually completed?
* What happens when a worker crashes halfway through execution?
* How should retries behave when the original attempt may still have succeeded?
* How is workflow state made durable?
* What happens when multiple workers attempt to make progress concurrently?
* How should the system behave when dependencies are slow or unavailable?
* Which guarantees should the system provide, and what trade-offs are required to provide them?
* How do we know the system is correct rather than merely appearing to work in normal conditions?

Aether exists to explore these questions through a real implementation rather than treating distributed-systems design as a collection of diagrams and terminology.

---

## Engineering Focus

Aether is primarily an exploration of:

* distributed workflow execution
* concurrency and coordination
* durable state
* failure detection and recovery
* retries and recovery semantics
* correctness and invariants
* observability
* performance and throughput
* operational behavior under failure

The goal is not to maximize the number of technologies involved.

The goal is to understand the system deeply enough to make explicit decisions about its behavior, prove or test important assumptions, and understand the consequences of those decisions.

---

## Development Approach

Aether is being developed incrementally.

The development process is intentionally treated as part of the project.

The repository will document the progression from:

```text
Requirements
    ↓
System model
    ↓
Execution semantics
    ↓
Invariants
    ↓
Architecture decisions
    ↓
Implementation
    ↓
Verification
    ↓
Failure experiments
    ↓
Benchmarks
    ↓
Operational refinement
```

Important engineering decisions will be recorded rather than hidden behind the final implementation.

This includes decisions about correctness guarantees, failure handling, concurrency, persistence, recovery, performance, and operational trade-offs.

---

## Current Status

Aether is currently in the **requirements and design stage**.

The repository is public before implementation begins so that the engineering process can be observed as the system evolves.

Current state:

* Project defined
* Scope being established
* Requirements being developed
* System behavior and guarantees being explored
* Implementation not yet started

As the project progresses, this README will evolve to reflect the actual state of the system.

---

## Public by Design

The repository is intentionally public from the start.

The objective is not to present a polished system without showing how it came to exist.

Instead, the project will make the engineering process visible:

* why a requirement exists
* why a design was chosen
* what alternatives were considered
* which invariants must hold
* what failed during implementation
* what experiments revealed
* how performance changes over time
* which trade-offs remain unresolved

The final implementation is only one part of the project.

The reasoning behind the implementation is equally important.

---

## Technology

### Primary language

**Go**

Go is being used as the primary implementation language while exploring the runtime, concurrency, networking, persistence, and operational characteristics required by the system.

### Areas of exploration

Depending on the requirements established during the project, the implementation may involve:

* concurrent workers
* persistent workflow state
* asynchronous messaging
* scheduling and coordination
* retry and recovery mechanisms
* observability
* performance testing

Specific technologies will be introduced only when they solve an identified system requirement.

---

## What Aether Is Not

Aether is not currently presented as a production-ready workflow platform.

It is also not intended to be a collection of disconnected demonstrations of distributed-systems techniques.

The project is being developed as one coherent system, where individual mechanisms exist because the workflow engine requires them.

---

## Roadmap

The roadmap will evolve as requirements become clearer.

The broad progression is expected to be:

```text
1. Business and system requirements
2. Execution model and correctness guarantees
3. Core workflow representation
4. Local execution
5. Durable state
6. Failure and recovery semantics
7. Distributed execution
8. Concurrency and coordination
9. Observability
10. Performance and load evaluation
11. Failure experiments
12. Hardening and operational refinement
```

The order and scope of these stages may change as the system reveals new constraints.

That change is part of the engineering process rather than something the project is trying to hide.

---

## Documentation

As development progresses, the repository will contain documentation covering areas such as:

* requirements
* system behavior
* architecture
* ADRs
* invariants
* execution semantics
* failure scenarios
* verification strategy
* benchmarks
* operational considerations

Documentation will be added as the corresponding decisions are actually made.

---

## Project Philosophy

Aether is being built around a simple principle:

> **Understand the system before optimizing the implementation.**

A working implementation is not enough.

The project should be able to explain:

* what guarantees it provides
* why those guarantees exist
* what happens when components fail
* what assumptions the system relies on
* where those guarantees stop
* how the system behaves under load
* how those claims were verified

The intent is to build a system that can be reasoned about, tested under failure, and measured under load—not merely one that works on the happy path.

---

## Status

**Early development — requirements and design phase**

This repository will change substantially as implementation begins.
