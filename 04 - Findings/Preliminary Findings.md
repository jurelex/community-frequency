# Preliminary Findings

These findings are preliminary and are expected to change as additional controlled testing is performed.

## 1. Fixed infrastructure matters

Both technology tracks reinforce the importance of fixed infrastructure when extending communications into areas where conventional connectivity is limited. Elevation, antenna placement, and infrastructure location should be treated as major experimental variables.

## 2. Mobility exposes different network behaviors

Meshtastic testing showed changing hop counts and RF conditions as the mobile node moved.

MeshCore testing showed that learned paths can become less useful after movement and that new paths may subsequently be learned.

Mobility is therefore an important test condition rather than simply a use case to be assumed.

## 3. Multi-hop connectivity is observable, but path interpretation matters

Both environments have demonstrated multi-hop traffic.

Hop count alone does not identify the complete physical route. For MeshCore, path identifiers still need to be correlated with known repeater identities before a complete route can be claimed.

For Meshtastic, RSSI/SNR recorded at a receiving fixed node should not be treated as an end-to-end signal measurement when a packet was relayed.

## 4. Repeater behavior can be demonstrated directly

The MeshCore `#test` experiment provided direct evidence that the local WY1B repeater repeated a particular packet.

Future experiments should distinguish between delivery confirmation, observed repetition, known path, and inferred path.

## 5. The technologies should not be reduced to a winner-takes-all comparison

Current evidence does not support a conclusion that Meshtastic or MeshCore is universally superior. A comparative, requirement-driven evaluation remains more appropriate.

## 6. The Peru question remains open

The Arizona experiments are preparation for a future feasibility assessment. They do not establish that either technology will work in a rainforest environment.

The Peru assessment must separately investigate vegetation, terrain, moisture, elevation opportunities, power availability, existing communications systems, community requirements, maintenance capacity, regulatory requirements, and appropriate backhaul options.

The purpose of the Peru mission is discovery and evidence gathering, not confirmation of a predetermined technology choice.
