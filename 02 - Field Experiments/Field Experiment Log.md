# Field Experiment Log

## Purpose

This document records selected field experiments suitable for public release from the Community Frequency Master Vault. Sensitive packet logs, precise coordinates, credentials, private network details, and other operational information are excluded.

## Meshtastic Track

### September 2, 2026 — Fixed-Base / Mobile Connectivity Test

**Devices:** Y1BH fixed home/base node; Y1BM mobile GPS-capable node; Raspberry Pi logging system.

**Objective:** Determine whether the fixed node could reliably observe mobile-node traffic while the mobile node moved through the local area, while recording RSSI, SNR, and hop information.

A direct message was received with approximately **-44 dBm RSSI, +11.25 dB SNR, and 0 hops**, providing a strong local direct-link measurement.

During movement, the logger recorded both direct and relayed traffic. Examples included:

| Observation | RSSI | SNR | Hops |
|---|---:|---:|---:|
| Mobile position report | -100 dBm | +4.5 dB | 2 |
| Mobile position report | -121 dBm | -10.75 dB | 1 |
| Mobile position report | -102 dBm | +4.25 dB | 2 |
| Mobile position report | -100 dBm | +7.25 dB | 1 |

These observations demonstrate continued reception beyond the direct local link.

**RF interpretation:** For a relayed packet, RSSI/SNR recorded by the fixed node describe reception into that fixed node, not complete end-to-end RF conditions. A 0-hop packet is directly useful as a mobile-to-fixed measurement; multi-hop packets provide useful hop/path information but should not be described as the mobile node's end-to-end signal strength.

### September 4, 2026 — Mobile Drive / AZ Mesh Test

A later drive produced additional observations. One channel test was received at approximately **-120 dBm, -11.75 dB SNR, 1 hop**. A direct message associated with a mountain-side test was received at approximately **-120 dBm, -11.25 dB SNR, 3 hops**.

The recorded test sequence included an `azmsh: 1/3 successful` result and a maximum observed path of approximately three hops.

Additional messages showed varying hop counts, including both 0-hop and 2-hop reception.

**Preliminary interpretation:** Message delivery and received RF conditions varied substantially with location. These observations are not sufficient to define a coverage boundary.

## MeshCore Track

### September 2026 — Local Companion-to-Companion Test

**Experimental topology:**

- WY1B — fixed MeshCore repeater
- WY1B-MC1 — fixed/home companion
- WY1B-MC2 — mobile companion

**Confirmed repeater test configuration:** 908.205 MHz, 62.5 kHz bandwidth, SF9, CR8, repeater mode enabled.

These are experimental configuration values, not a universal deployment recommendation.

### MC1 ↔ MC2 Path Learning

The first companion-to-companion message failed while the contact/path was shown as Flood.

A later sequence produced:

1. `Testing direct message` — failed while path was Flood.
2. `Testing after flood` — Delivered.
3. MC2 replied `Test back` — Delivered.
4. The contact subsequently showed `Path: Direct`.

**Observation:** A usable direct path was learned after initial discovery/flood behavior.

### MC2 Mobile / Drive Testing

MC2 was used for drive/coverage testing. Tests produced a mixture of Delivered and Failed messages depending on location.

After movement, MC2 was observed with a one-hop path to MC1, strongly suggesting repeater-mediated routing. The exact intermediate repeater should not be claimed unless the path/hash is independently correlated.

**Observation:** Mobility appears to expose learned-path staleness or recovery behavior and is therefore a useful stress-test condition.

### MC2 GPS / Power Observations

MC2 initially reported `0.0/0.0` for GPS until GPS was enabled. After GPS was enabled and the device was powered from the vehicle, valid positions were successfully transmitted.

MC2 also experienced a brief shutdown while showing approximately 30% battery, but remained powered from vehicle USB. The exact cause was not established; a low-voltage or power-management issue remains a hypothesis.

### September 5, 2026 — MeshCore #test Repeater Confirmation

MC2 sent a `#test` message. The application reported **Heard 1 Repeat**.

The View Path display showed:

- MC2 — sent the message
- WY1B Repeater — Hop 1 — repeated the message
- MC2 — received the message
- Path: 1 hop

This is direct evidence that WY1B repeated that particular channel packet.

The application also displayed two known repeaters; this was interpreted as known contacts, not evidence that both repeaters handled the packet.

### September 5, 2026 — Wider AZCOREMSH Testing

An AZCOREMSH public test produced an acknowledgement containing SNR/RSSI information and a three-hop path.

A separate MC2 `#testing` experiment reported six repeats and a six-hop route:

`06 → 85 → 49 → 02 → a5 → 95`

The identity of every path identifier has not yet been established. In particular, `06` has not yet been independently correlated with WY1B.

**Interpretation:** The result demonstrates that the wider AZCOREMSH infrastructure can provide long multi-hop connectivity, but does not yet establish every repeater identity or route stability.

## Cross-Technology Observations

Meshtastic and MeshCore are being evaluated as different systems rather than as simple replacements for one another.

**Meshtastic observations include:** direct versus relayed reception, RSSI/SNR, hop counts, mobile coverage observations, position reporting, and network traffic logging.

**MeshCore observations include:** repeater-centered infrastructure, learned paths, flood discovery, direct path learning, mobility-related path changes, repeater confirmation through View Path, and multi-hop testing.

No conclusion has been made that one system is universally superior.

## Experimental Limitations

Current results are not formal RF coverage maps or statistically complete performance studies.

Limitations include limited test runs, changing locations and environmental conditions, incomplete knowledge of the wider network, incomplete path-identifier correlation, third-party traffic, and lack of repeated measurements at every test point.

## Next Testing Priorities

Future tests should emphasize reproducibility:

1. Fixed radio configuration
2. Fixed antenna configuration
3. Defined test route or test points
4. Repeated measurements
5. Unique test messages
6. Delivery success/failure
7. RSSI
8. SNR
9. Hop count
10. Independently verified repeater identity
11. Timestamp
12. Environmental conditions
13. Power state
14. Private GPS position with only appropriate geographic precision published

The goal is to move from interesting observations toward repeatable evidence.

## Evidence Classification

- **Confirmed observation** — directly demonstrated by the recorded experiment.
- **Measured value** — recorded by the test system.
- **Strong interpretation** — supported by multiple observations but open to further testing.
- **Hypothesis** — plausible explanation requiring additional evidence.
- **Unknown** — insufficient evidence to determine the answer.
