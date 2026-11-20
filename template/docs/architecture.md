# Architecture

Defines the system's components, data flows, dependencies, boundaries, and deployment.

## Overview

<!-- Agent: Summarize the system, its main parts, and how they interact in two to four sentences. -->

## Components

| Name        | Responsibility             | Location             |
| ----------- | -------------------------- | -------------------- |
| [COMPONENT] | [COMPONENT_RESPONSIBILITY] | [COMPONENT_LOCATION] |

## Data Flows

<!-- Agent: Describe each flow in one bullet with its trigger, path, storage, and output. -->

- [DATA_FLOW]

## External Dependencies

| Dependency            | Purpose              | Owner              |
| --------------------- | -------------------- | ------------------ |
| [EXTERNAL_DEPENDENCY] | [DEPENDENCY_PURPOSE] | [DEPENDENCY_OWNER] |

## Boundaries and Invariants

<!-- Agent: List trust boundaries and rules that must stay true regardless of code changes. -->

- [INVARIANT]

## Deployment

Target: [DEPLOYMENT_TARGET]

<!-- Human: Add environments, release steps, and rollback. -->

## Diagram

<!-- Agent: Replace the nodes and edges with real components. -->

```mermaid
flowchart LR
    Client --> Server
    Server --> DB
```

## Key Decisions

Every architecture decision has an ADR in [adr/](adr/).
