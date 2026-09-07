---
title: "MeshCore Testing Paused — Meshtastic-First Platform Decision"
project: "Community Frequency"
date: 2026-09-07
status: "Decision / Testing Paused"
---

# MeshCore Testing Paused — Meshtastic-First Platform Decision

**Date:** September 7, 2026  
**Status:** Decision — MeshCore testing paused

## 1. Decision

Community Frequency is pausing active MeshCore testing and returning to a Meshtastic-first platform strategy.

MeshCore remains documented as a research experiment and may be revisited in the future, but it will no longer be treated as the primary operational platform.

> **Community Frequency will focus its primary hardware, field testing, infrastructure, and deployment research on Meshtastic.**

## 2. Why

Hands-on MeshCore testing demonstrated useful capabilities, including repeater networking, path discovery, direct versus flood communication, tracing, diagnostics, long multi-hop paths, and network observation.

However, the practical maintenance experience exposed too much operational friction for the project’s intended model. Firmware management, USB access, companion/repeater administration, remote-management behavior, and general maintenance created more complexity than we want in a community deployment platform.

The project goal is not simply to build an interesting technical network. It is to develop a communications platform that can eventually be deployed and maintained without excessive specialist intervention.

## 3. Operational requirement

A central Community Frequency principle is:

> **Deploy it, have it work, and don’t need to babysit it.**

Technology will therefore be evaluated not only by capability, but also by reliability, maintainability, availability, field serviceability, documentation, trainability, and long-term operational simplicity.

## 4. What MeshCore accomplished

The MeshCore experiment was not a failure.

It answered important questions through real-world testing that could not have been answered through documentation alone.

The project gained practical experience with:

- Companion devices.
- Repeaters.
- Advertisements and contacts.
- Path hashes.
- Flood and direct routing.
- Path learning.
- Repeater traces.
- Ping and trace behavior.
- Public-channel testing.
- Application-layer diagnostics.
- Analyzer concepts.
- Repeater statistics.
- Remote administration.
- Real-world coverage and path behavior.

The experiment established an important architectural lesson:

> **A platform can be technically capable and still be the wrong operational fit for a particular project.**

## 5. Meshtastic becomes the primary platform

The working Community Frequency architecture is now:

```text
COMMUNITY FREQUENCY
        │
        ▼
    MESHTASTIC
        │
 ┌──────┼──────────┐
 ▼      ▼          ▼
Mobile  Fixed     Field
nodes   nodes     deployments
        │
        ▼
 Raspberry Pi
 monitoring / data / services
```

Meshtastic will be the primary focus for:

- Commercial hardware evaluation.
- Peru hardware evaluation.
- Field deployments.
- Mobile/community nodes.
- Fixed infrastructure.
- Raspberry Pi integration.
- Data collection and monitoring.
- Community Frequency reference configurations.

## 6. MeshCore status

MeshCore is paused, not rejected.

| Area | Status |
|---|---|
| Testing | **Paused** |
| Operational platform | No |
| Documentation | Retained |
| Research value | Retained |
| Future reconsideration | Possible |

The existing MeshCore work remains part of the project history and research documentation.

No additional MeshCore testing is planned unless a specific future requirement justifies resuming it.

## 7. Existing MeshCore hardware

The existing MeshCore hardware and configurations should not be unnecessarily modified.

The WY1B MeshCore repeater and related equipment can remain documented as experimental infrastructure.

This preserves the ability to reproduce or review the experiment later without allowing it to consume ongoing project effort.

## 8. What happens next

The project will concentrate on Meshtastic.

Immediate priorities:

1. Evaluate commercially available Meshtastic-compatible hardware.
2. Select the most practical Community Frequency field device.
3. Continue Peru MTC/homologation research.
4. Validate the Peru operating configuration.
5. Develop repeatable field-test procedures.
6. Continue Raspberry Pi monitoring and data collection.
7. Document successful Meshtastic deployments.
8. Develop the Community Frequency deployment model around a low-maintenance architecture.

## 9. Lessons learned

### Technical capability is not enough

A platform can have excellent features and still be a poor operational fit.

### Maintenance is part of the architecture

Firmware updates, configuration, recovery, administration, and troubleshooting are part of the system itself.

### Field deployments need simplicity

The more specialized knowledge required to maintain a deployed node, the harder it becomes to scale a community project.

### Experiments have value even when they are paused

The MeshCore work produced practical knowledge and helped establish a better-informed platform decision.

## 10. Current platform decision

| Area | Decision |
|---|---|
| Primary platform | **Meshtastic** |
| Secondary/research platform | MeshCore |
| Active MeshCore testing | **Paused** |
| Meshtastic hardware evaluation | **Continue** |
| Peru hardware research | **Continue** |
| Peru MTC research | **Continue** |
| Raspberry Pi infrastructure | **Continue** |
| Existing MeshCore documentation | **Preserve** |

## 11. Project principle

> **The best technology is not necessarily the technology with the most features. It is the technology that can reliably solve the problem and be maintained by the people who actually have to use it.**

For the current stage of Community Frequency, Meshtastic is the better fit for that objective.

---

## Historical note

This decision follows an extended hands-on evaluation of MeshCore infrastructure, including companion-to-repeater-to-companion communication, path discovery, tracing, public-channel tests, repeater status monitoring, remote administration, field driving tests, and network behavior research.

The observations and results from that work remain part of the Community Frequency project record.
