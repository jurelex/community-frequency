# Technology Tracks / Líneas Tecnológicas

## English
Community Frequency is technology-neutral. Low-power mesh is being evaluated as one component of a broader resilient communications architecture.

Following the September 7, 2026 platform decision, **Meshtastic is the primary platform focus**. MeshCore remains a preserved research track, but active testing is paused.

| Technology | Current role |
|---|---|
| Meshtastic | **Primary platform** — mobile/community mesh, telemetry, GPS, field participation, fixed infrastructure, and deployment research |
| MeshCore | **Paused research track** — preserved documentation and experimental infrastructure; may be revisited if specifically justified |
| HF | Long-range backhaul and communications where appropriate |
| Satellite / Internet | Connected backhaul and remote-area connectivity |
| Cellular | Existing connectivity where available |

### Meshtastic

Meshtastic is the primary platform under evaluation for mobile operation, telemetry/GPS, community participation, fixed infrastructure, field deployments, Raspberry Pi integration, and data collection/monitoring.

### MeshCore

MeshCore testing is paused. Existing research remains documented, including Companion, Repeater, Advert, Contact, Path, Direct, Flood, ACK/Delivered, Path Hash, path learning, repeater-confirmed delivery, and multi-hop behavior.

These observations remain part of the project's experimental record and are not treated as a deployment recommendation.

### Current platform hypothesis

The current working direction is that Meshtastic is the better operational fit for the present Community Frequency objectives, particularly where maintainability, field serviceability, documentation, trainability, and long-term operational simplicity matter alongside technical capability.

This is a current platform decision for the project, not a claim that MeshCore is technically incapable or unsuitable for every use case. Future reconsideration remains possible if a specific requirement justifies it.

### Conceptual architecture

COMMUNITY FREQUENCY → MESHTASTIC → mobile nodes / fixed nodes / field deployments → Raspberry Pi monitoring, data, and services

A broader resilient communications architecture may also incorporate HF, satellite, Internet, cellular, elevated repeaters, and other appropriate technologies as evidence from the field warrants.

The architecture remains subject to field validation and is not a blanket deployment recommendation.

---

## Español
Community Frequency mantiene una postura tecnológicamente neutral. Las redes mesh de bajo consumo se están evaluando como un componente de una arquitectura más amplia de comunicaciones resilientes.

Después de la decisión de plataforma del 7 de septiembre de 2026, **Meshtastic es el enfoque principal del proyecto**. MeshCore permanece como una línea de investigación preservada, pero las pruebas activas están pausadas.

| Tecnología | Función actual |
|---|---|
| Meshtastic | **Plataforma principal** — mesh móvil/comunitaria, telemetría, GPS, participación en campo, infraestructura fija e investigación de despliegue |
| MeshCore | **Línea de investigación pausada** — documentación e infraestructura experimental preservadas; podrá reconsiderarse si existe una justificación específica |
| HF | Comunicaciones y backhaul de largo alcance cuando corresponda |
| Satélite / Internet | Backhaul conectado y conectividad en zonas remotas |
| Celular | Conectividad existente donde esté disponible |

### Meshtastic

Meshtastic es la plataforma principal bajo evaluación para operación móvil, telemetría/GPS, participación comunitaria, infraestructura fija, despliegues de campo, integración con Raspberry Pi y recopilación/monitoreo de datos.

### MeshCore

Las pruebas con MeshCore están pausadas. La investigación existente permanece documentada, incluyendo Companion, Repeater, Advert, Contact, Path, Direct, Flood, ACK/Delivered, Path Hash, aprendizaje de rutas, entregas confirmadas por repetidores y comportamiento de múltiples saltos.

Estas observaciones permanecen como parte del registro experimental del proyecto y no se consideran una recomendación de despliegue.

### Hipótesis actual de plataforma

La dirección actual de trabajo es que Meshtastic representa un mejor ajuste operativo para los objetivos actuales de Community Frequency, especialmente cuando la mantenibilidad, la facilidad de servicio en campo, la documentación, la capacitación y la simplicidad operativa a largo plazo importan tanto como la capacidad técnica.

Esta es una decisión de plataforma para la etapa actual del proyecto, no una afirmación de que MeshCore sea técnicamente incapaz o inadecuado para todos los casos de uso. Sigue siendo posible reconsiderarlo si un requisito específico lo justifica.

### Arquitectura conceptual

COMMUNITY FREQUENCY → MESHTASTIC → nodos móviles / nodos fijos / despliegues de campo → Raspberry Pi para monitoreo, datos y servicios

Una arquitectura más amplia de comunicaciones resilientes también podría incorporar HF, satélite, Internet, redes celulares, repetidores elevados y otras tecnologías apropiadas cuando la evidencia de campo lo justifique.

La arquitectura continúa sujeta a validación en campo y no constituye una recomendación general de despliegue.
