# MeshCore Testing Restarted — New Infrastructure Structure

**Project:** Community Frequency  
**Date:** September 8, 2026  
**Status:** Decision / Testing Restarted

## 1. Decision

Community Frequency is restarting active MeshCore testing after pausing the initial round of experiments.

The first round gave us a good understanding of MeshCore paths, flooding, direct messaging, repeaters, and Room Servers, but the original setup was too focused on individual device testing. We are now restructuring the test network so we can evaluate MeshCore as an actual small-scale infrastructure deployment.

## 2. New Test Structure

```text
HOME
├── WY1B — Seeed Studio Solar Pro
│   └── Fixed solar repeater
│
└── WY1B-Room — T114
    └── Room Server
PROPERTY
└── WY1B-2 — Seeed Studio Solar Pro
    └── Fixed solar repeater
COMPANIONS
├── WY1B-MC1 — Heltec V4
├── WY1B-MC2 — Heltec V4
└── WY1B-MC3 — Heltec V4
```

The infrastructure roles are intentionally separated:

- **WY1B / WY1B-2:** dedicated solar repeaters
- **WY1B-Room:** dedicated Room Server
- **MC1 / MC2 / MC3:** portable/user companions

The Room Server will now become an important part of field experiments rather than simply a separate feature being tested.

## 3. Field Test Objectives

The new test structure will allow us to compare:

1. **Direct messaging** — Can one specific node reach another?
2. **Channel/flood testing** — How does traffic propagate through the mesh?
3. **Room messaging** — Can a field node reliably reach a known infrastructure service?
4. **Room store-and-forward** — Can the Room retain a message while a client is offline and deliver it when the client reconnects?
5. **Multi-repeater paths** — Can a field node reach the home Room Server through the property and home repeaters?
6. **Coverage and reliability** — How do these services behave as MC2 moves away from the infrastructure?

## 4. Research Objective

The goal is no longer simply to demonstrate that MeshCore can send messages.

We want to collect repeatable field data and determine how well this architecture could support the Community Frequency concept of reliable, maintainable community communications.

The testing will therefore focus on infrastructure behavior, service availability, path behavior, coverage, reliability, and operational maintenance rather than individual device capabilities alone.

## 5. Platform Status

MeshCore remains an experimental platform for Community Frequency.

The restart of testing does **not** change the project's current primary-platform decision. Meshtastic remains the primary platform focus for Community Frequency. MeshCore is being maintained as an active experimental research track so that its infrastructure model can be evaluated more realistically.

We are not assuming MeshCore is the answer. The field results will help determine where it fits, where it does not fit, and what operational lessons can be carried forward.

## 6. Historical Context

This testing phase follows the initial MeshCore experiments, which examined paths, flooding, direct messaging, repeaters, Room Servers, tracing, diagnostics, and network behavior.

The earlier testing was valuable but was heavily oriented toward individual device behavior. The new architecture is intended to test a small infrastructure model with clearly separated repeater, service, and user-node roles.

**Testing is officially restarted with this architecture.**
