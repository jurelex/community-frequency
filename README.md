# Community Frequency

## Resilient communications for places where conventional connectivity does not reach

Community Frequency is an exploratory field-research project focused on community-owned, low-power communication systems and their role within resilient communications infrastructure.

The project is investigating how technologies such as low-power mesh networks can complement existing communications systems — including HF radio, satellite, cellular, and Internet connectivity — particularly in remote and underserved environments.

This repository is the **public project record**.

It documents research, experiments, field observations, technical decisions, failures, lessons learned, and the development of the project over time.

> **This is not a finished solution.**
>
> The project is deliberately evidence-driven: **listen, measure, learn, and build.**

---

## Current Status

**Phase 0 — Discovery & Feasibility**

The project is currently focused on understanding the technical, operational, environmental, community, and regulatory requirements for resilient communications in remote environments.

A major near-term activity is the planned **Peru 2026 feasibility mission**, which will be used to gather information, evaluate existing communications practices, conduct controlled technical testing where appropriate, and identify requirements for future field work.

No deployment conclusions have been made yet.

---

## What We Are Investigating

The central question is:

> **How can community-owned, low-power communications extend the reach and usefulness of existing communications infrastructure in places where conventional connectivity does not reach?**

Areas of investigation include:

- Low-power mesh networking
- Store-and-forward communications
- Remote and intermittent connectivity
- Solar-powered communications infrastructure
- Elevated repeater infrastructure
- HF radio and other backhaul systems
- Satellite and Internet connectivity
- Environmental and terrain constraints
- Community ownership and local technical capacity
- Emergency and health communications
- Field logistics and coordination
- Regulatory and spectrum considerations
- Practical deployment and maintenance requirements

The goal is not to replace existing infrastructure.

The goal is to understand whether low-power local networks can **extend the value of the connectivity that already exists**.

---

## Technology Tracks

Community Frequency is intentionally technology-neutral.

Two low-power mesh technologies are currently being evaluated as parallel research tracks:

- **Meshtastic**
- **MeshCore**

They are being studied independently rather than assuming that either technology will become the project's permanent platform.

The project may ultimately use one technology, multiple technologies, or a different architecture entirely.

Technology selection will follow evidence from testing and field requirements.

See:

- [`01 - Research/Technology Tracks.md`](01%20-%20Research/Technology%20Tracks.md)

---

## Research Approach

The project follows a practical field-research cycle:

**Observe → Hypothesize → Test → Measure → Document → Reassess**

Testing is intended to distinguish between:

- What is known
- What has been observed
- What has been measured
- What is suspected
- What has not yet been tested

Failures and unexpected results are considered valuable research data.

A result that disproves an assumption is still a useful result.

See:

- [`00 - Project/Methodology.md`](00%20-%20Project/Methodology.md)

---

## Peru 2026

The planned Peru 2026 mission is currently a **discovery and feasibility effort**, not a deployment project.

The assessment is intended to help answer questions such as:

- What communications systems are already being used?
- Where are the actual connectivity gaps?
- What environmental conditions affect low-power radio performance?
- What infrastructure already exists?
- Where could low-power mesh communications provide useful additional coverage?
- What technical skills and resources are available locally?
- What community ownership models could be appropriate?
- What regulatory requirements apply?
- What would a sustainable deployment and maintenance model require?

The findings will determine whether additional field testing or future deployment work is justified.

See:

- [`03 - Peru 2026/Peru Assessment.md`](03%20-%20Peru%202026/Peru%20Assessment.md)

---

## Field Experiments

Field experiments are used to evaluate real-world behavior rather than relying solely on theoretical or laboratory assumptions.

Experiments may examine:

- Range
- Elevation
- Terrain
- Vegetation
- Antenna configuration
- Node placement
- Message delivery
- Hop behavior
- Store-and-forward behavior
- Power requirements
- Environmental conditions
- Operational usability

Results are documented as they become available.

See:

- [`02 - Field Experiments/Field Experiment Log.md`](02%20-%20Field%20Experiments/Field%20Experiment%20Log.md)

---

## Preliminary Findings

The project maintains a separate record of observations and findings so that conclusions can evolve as additional evidence becomes available.

Early observations should not be interpreted as final deployment recommendations.

See:

- [`04 - Findings/Preliminary Findings.md`](04%20-%20Findings/Preliminary%20Findings.md)

---

## Why Publish the Work?

The project is being developed openly so that supporters, researchers, engineers, radio operators, community organizations, and other potential collaborators can see what is actually being tested.

Public documentation makes it possible to see:

- What we planned to test
- What we actually tested
- What worked
- What failed
- What changed
- What remains unknown
- Why decisions were made
- How conclusions develop over time

The objective is not to present a predetermined answer.

It is to document the process of finding the answer.

---

## Public / Private Documentation

The GitHub repository is the project's **public publication layer**.

Detailed research and operational information is maintained separately in a private Master Vault.

Sensitive information intentionally excluded from the public repository may include:

- Raw packet logs
- Sensitive geographic coordinates
- Private network configurations
- Credentials and keys
- Personal information
- Private organizational information
- Sensitive partner or community information
- Other information that could create security or privacy risks

The public record is therefore curated for transparency without exposing information that should remain private.

---

## Funding Transparency

Community Frequency is currently being developed as an independent project.

Project-specific funding and equipment information is documented publicly as the project develops.

See:

- [`06 - Funding Transparency/Project Funding.md`](06%20-%20Funding%20Transparency/Project%20Funding.md)
- [`06 - Funding Transparency/Equipment.md`](06%20-%20Funding%20Transparency/Equipment.md)

---

## Project Timeline

The project timeline records major decisions, experiments, milestones, and changes in direction.

See:

- [`05 - Project History/Timeline.md`](05%20-%20Project%20History/Timeline.md)

---

## Contributing

Technical discussion and constructive criticism are welcome.

Particularly useful contributions include:

- Field-testing experience
- Meshtastic experience
- MeshCore experience
- RF engineering knowledge
- Antenna and propagation analysis
- Power-system experience
- Remote-network deployment experience
- HF or satellite integration experience
- Experience operating communications systems in remote environments
- Knowledge of community-owned technology models
- Peru or Latin American regulatory knowledge
- Suggestions for reproducible testing methodologies

If you have experience that could help answer a specific research question, please open an issue or start a discussion.

**The most useful contribution is evidence.**

If you disagree with an assumption or conclusion, showing how it can be tested is especially valuable.

---

## Current Questions

The project is intentionally maintaining unanswered questions.

Among them:

1. How well do low-power mesh networks perform in the environmental conditions encountered in remote communities?
2. How much does elevation improve practical coverage?
3. What network architectures are sustainable with limited power and intermittent infrastructure?
4. How can mesh networks complement HF, satellite, or Internet backhaul?
5. Which technical characteristics matter most for community-scale deployments?
6. What maintenance and training requirements are realistic?
7. What regulatory requirements must be addressed before field deployment?
8. Which technology or combination of technologies best fits the actual requirements?

These questions will change as evidence accumulates.

---

## Repository Structure

```text
00 - Project/
    Project Status
    Project Transparency
    Methodology

01 - Research/
    Technology Tracks

02 - Field Experiments/
    Field Experiment Log

03 - Peru 2026/
    Peru Assessment

04 - Findings/
    Preliminary Findings

05 - Project History/
    Timeline

06 - Funding Transparency/
    Project Funding
    Equipment

07 - Media/
    Publication guidance
