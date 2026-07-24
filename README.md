# Ohana Platform

> **A modular infrastructure supervision platform built around observation, health monitoring and real-time visualization.**

---

## Overview

Ohana Platform is an open, modular platform designed to supervise infrastructure through standardized observations.

Rather than coupling data collection and visualization into a single application, Ohana separates responsibilities into independent components that communicate through well-defined interfaces.

This architecture provides:

* scalable supervision;
* modular plugins;
* declarative infrastructure;
* real-time dashboards;
* timeline-based history;
* clear separation between collection and visualization.

---

# Platform Architecture

```text
                    Infrastructure
                           │
                           ▼
                  Ohana-Agent
                           │
                 REST Observations
                           │
                           ▼
                  Ohana-Vision
                           │
                  Web Dashboard
                           │
                           ▼
                     Administrator
```

---

# Components

## Ohana-Agent

**Infrastructure observation engine**

Responsibilities:

* plugin execution;
* scheduler;
* capability monitoring;
* observation generation;
* observation export.

Repository

```text
https://github.com/<your-account>/Ohana-Agent
```

---

## Ohana-Vision

**Real-time supervision dashboard**

Responsibilities:

* observation ingestion;
* timeline engine;
* health computation;
* topology visualization;
* dashboard;
* WebSocket updates.

Repository

```text
https://github.com/<your-account>/Ohana-Vision
```

---

## Ohana-Platform

This repository.

Responsibilities:

* platform documentation;
* deployment guides;
* operational procedures;
* compatibility matrix;
* installation examples;
* future deployment assets.

---

## Ohana-House

Reference deployment of the platform.

This repository documents a real-world installation of Ohana within a home infrastructure and provides practical deployment examples.

---

# Documentation

The complete documentation is available in the `docs` directory.

| Document                  | Description                        |
| ------------------------- | ---------------------------------- |
| Architecture              | Global platform architecture       |
| Installer-Ohana-Platform | Complete installation guide        |
| Operations                | Production operation guide         |
| Troubleshooting           | Diagnostics and problem resolution |

---

# Getting Started

1. Install **Ohana-Agent**.
2. Install **Ohana-Vision**.
3. Configure the infrastructure.
4. Connect Agent to Vision.
5. Open the dashboard.

The complete procedure is described in:

```text
docs/Installer-Ohana-Platform.md
```

---

# Repository Structure

```text
Ohana-Platform/

docs/
examples/
scripts/

README.md
ROADMAP.md
CHANGELOG.md
```

---

# Version Compatibility

Platform releases define validated combinations of Ohana-Agent and Ohana-Vision.

| Platform | Agent  | Vision |
| -------- | ------ | ------ |
| 1.0      | 0.14.x | 0.1.x  |

---

# Roadmap

The platform roadmap is available in:

```text
ROADMAP.md
```

---

# Contributing

At this stage, the platform is primarily developed as the reference implementation of the Ohana ecosystem.

Contribution guidelines will be published in a future release.

---

# License

See the `LICENSE` file for licensing information.
