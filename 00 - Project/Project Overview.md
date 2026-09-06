# Community Frequency — Project Overview

## 1. Project

Community Frequency is an independent exploration, research, and feasibility project focused on resilient communications for places where conventional connectivity does not reliably reach.

The project is currently in **Phase 0 — Discovery & Feasibility**. The objective at this stage is not to deploy a finished network, but to understand the problem, test available approaches, document evidence, and determine whether a practical and sustainable communications architecture is possible.

## 2. The Question

The central question is:

> **How can communities maintain basic communications when cellular or Internet connectivity does not reach them or is not enough?**

This question deliberately comes before the technology.

A useful system may need to support simple, practical communications such as health or medical messages, emergency alerts, field check-ins, location information, logistics, coordination, or sensor and telemetry data. The actual requirements must be learned from the communities and environments involved.

## 3. Technology Is the Tool

Community Frequency is technology-neutral.

The project does not assume that Meshtastic, MeshCore, HF, satellite, cellular, or Internet connectivity is the answer by itself.

Instead, the project explores how different communications layers might complement one another.

### Potential layers

| Layer | Potential role |
|---|---|
| Low-power radio / mesh | Local or regional communications with limited infrastructure |
| Elevated repeaters | Extending coverage beyond a local area |
| HF radio | Long-distance communications where terrestrial infrastructure is unavailable |
| Satellite | Backhaul or communications for isolated locations |
| Cellular | Conventional connectivity where available |
| Internet | Backhaul, services, coordination, and broader connectivity |
| Sensors / telemetry | Moving environmental or operational information |

The eventual architecture will depend on evidence from the field.

## 4. Parallel Technology Tracks

Two low-power mesh technologies are currently being evaluated as parallel tracks:

- **Meshtastic**
- **MeshCore**

The project intentionally avoids treating either technology as the project's identity or predetermined solution.

The purpose is to understand each system on its own terms, document real-world behavior, identify strengths and limitations, and determine where each may or may not fit within a larger resilient communications architecture.

The Arizona field work has included direct-to-mobile testing, relayed communications, multi-hop behavior, repeater testing, route learning, and mobile/drive testing.

The evidence remains experimental and incomplete. A successful message does not automatically establish reliable coverage, and hop count does not represent physical distance.

## 5. Research Method

The project's working principle is:

> **Listen. Measure. Learn. Build.**

### Listen

Understand the communications problem from the perspective of the people and organizations experiencing it.

### Measure

Test what the environment and available technologies actually allow.

### Learn

Document successful tests, failures, limitations, uncertainties, and questions that require additional testing.

### Build

Only consider deployment when there is demonstrated need, appropriate community participation, technical evidence, and a sustainable path.

This approach is intentionally evidence-driven.

## 6. Field Experiments

Before considering remote deployment, Community Frequency has been conducting controlled field experiments in Arizona.

The public field record documents tests involving:

- direct communications
- relayed messages
- multi-hop behavior
- fixed and mobile nodes
- repeater behavior
- route/path learning
- signal observations
- mobile/drive testing
- comparisons between Meshtastic and MeshCore

The field record preserves observations separately from conclusions where possible.

It also records uncertainty. For example:

- RSSI and SNR observed at an intermediate node are not automatically end-to-end RF measurements.
- Hop count is not distance.
- Delivery of a message does not by itself prove that an entire route is understood.
- Path identifiers must be independently correlated before assigning them to a known repeater.

This discipline is important because the project is intended to produce evidence, not marketing claims.

## 7. Peru 2026

Peru is the first major field-assessment context for Community Frequency.

A planned **September 2026 feasibility mission** will focus on listening, observing, and learning directly about communications needs and local conditions.

The project is not approaching the mission with a predetermined deployment plan.

The assessment is intended to investigate:

- what communications are already available;
- where conventional connectivity is insufficient;
- how people currently communicate when cellular or Internet service is unavailable;
- what kinds of information actually need to move;
- environmental and geographic constraints;
- whether low-power communications could provide useful local or regional connectivity;
- how existing systems such as HF or satellite connectivity could complement local communications;
- technical and regulatory considerations;
- what would be required for a sustainable, community-oriented system.

The first objective is to understand the reality on the ground.

**We are not going to Peru with a predetermined solution. We are going to listen, measure, and learn.**

## 8. A Possible Architecture

One of the concepts being investigated is a layered architecture in which a community does not necessarily need direct access to the global Internet to gain useful local communications.

For example:

**Remote community → low-power mesh → elevated/solar repeater → connected location → HF / satellite / Internet**

This is a research concept, not a deployment recommendation.

Terrain, vegetation, moisture, antenna height, power availability, regulation, community needs, and the characteristics of each communications system will determine whether such an architecture is practical.

The project is particularly interested in whether one connected point can extend useful communications into surrounding areas without requiring conventional infrastructure at every location.

## 9. Community Ownership

Community Frequency is intended to explore technology **with communities, not simply for them**.

Technical capability alone does not make a communications system appropriate.

Any future deployment would need to consider:

- local needs and priorities;
- informed participation;
- local training and technical capacity;
- ownership and long-term maintenance;
- power availability;
- cultural context;
- privacy and safety;
- appropriate handling of sensitive information;
- regulatory requirements;
- financial sustainability.

The feasibility phase exists partly to determine whether these conditions can realistically be met.

## 10. Documentation and Transparency

The public repository is a curated publication layer derived from a private Master Vault.

The public record is intended to show the real development process:

**what was planned → what was tested → what happened → what was learned → what remains uncertain → what comes next**

Sensitive information is intentionally excluded from the public record. This includes credentials, security keys, private configurations, personal information, and sensitive location information where disclosure could create risk.

The project also preserves failed tests and limitations rather than presenting only successful results.

This is important because the project is still exploratory.

## 11. Current Status

**Phase 0 — Discovery & Feasibility**

Current priorities include:

1. Continue documenting and organizing the Arizona field experiments.
2. Continue evaluating Meshtastic and MeshCore without assuming either is the final platform.
3. Improve understanding of practical multi-hop and repeater behavior.
4. Prepare the Peru 2026 feasibility mission.
5. Investigate technical and regulatory requirements relevant to Peru.
6. Identify potential technical, community, research, and organizational collaborators.
7. Determine what evidence would be required before considering any real deployment.

## 12. What Success Looks Like

Success at this stage does not mean deploying a network.

A successful feasibility effort could produce a conclusion such as:

- a particular approach appears practical in a defined environment;
- several technologies can work together effectively;
- a proposed architecture is technically feasible but requires additional infrastructure;
- a technology is not appropriate for the environment;
- the communications problem requires a different solution;
- more field evidence is needed before a responsible decision can be made.

A finding that a technology **does not work** for a particular environment is still a valuable result.

## 13. How to Participate

Community Frequency is interested in connecting with people who can contribute:

- field experience;
- amateur-radio knowledge;
- HF and antenna expertise;
- low-power radio and mesh networking knowledge;
- satellite communications experience;
- solar/off-grid power expertise;
- emergency communications experience;
- engineering and research;
- remote deployment experience;
- community technology experience;
- relationships with organizations working in rural or Indigenous communities.

Financial and equipment support can also help fund the feasibility work.

## 14. The Guiding Principle

Community Frequency begins with a simple idea:

> **When the network ends, the community doesn't.**

The goal is not to force technology into a community.

The goal is to understand what people need to communicate, determine what the environment permits, and explore the most practical way to make that communication possible.

**Listen. Measure. Learn. Build.**


---

# Español

## 1. Proyecto

Community Frequency es un proyecto independiente de exploración, investigación y factibilidad enfocado en comunicaciones resilientes para lugares donde la conectividad convencional no llega de manera confiable.

El proyecto se encuentra actualmente en la **Fase 0 — Descubrimiento y Factibilidad**. El objetivo en esta etapa no es desplegar una red terminada, sino comprender el problema, probar diferentes enfoques, documentar evidencia y determinar si es posible una arquitectura de comunicaciones práctica y sostenible.

## 2. La Pregunta

La pregunta central es:

> **¿Cómo pueden las comunidades mantener comunicaciones básicas cuando la conectividad celular o de Internet no llega o no es suficiente?**

Esta pregunta viene deliberadamente antes que la tecnología.

Un sistema útil podría necesitar facilitar comunicaciones sencillas y prácticas, como mensajes de salud o médicos, alertas de emergencia, reportes de campo, información de ubicación, logística, coordinación o datos de sensores y telemetría. Los requisitos reales deben conocerse a partir de las comunidades y los entornos involucrados.

## 3. La Tecnología es la Herramienta

Community Frequency mantiene una posición neutral respecto de la tecnología.

El proyecto no asume que Meshtastic, MeshCore, HF, satélite, redes celulares o Internet sean por sí solos la respuesta.

En cambio, explora cómo diferentes capas de comunicación podrían complementarse.

### Capas potenciales

| Capa | Posible función |
|---|---|
| Radio de bajo consumo / mesh | Comunicaciones locales o regionales con infraestructura limitada |
| Repetidores elevados | Extender la cobertura más allá de un área local |
| Radio HF | Comunicaciones de larga distancia donde no existe infraestructura terrestre |
| Satélite | Enlace de retorno o comunicaciones para lugares aislados |
| Red celular | Conectividad convencional donde esté disponible |
| Internet | Enlace de retorno, servicios, coordinación y conectividad más amplia |
| Sensores / telemetría | Transmisión de información ambiental u operativa |

La arquitectura final dependerá de la evidencia obtenida en el campo.

## 4. Líneas Tecnológicas Paralelas

Actualmente se están evaluando dos tecnologías de redes mesh de bajo consumo como líneas paralelas:

- **Meshtastic**
- **MeshCore**

El proyecto evita deliberadamente tratar cualquiera de ellas como la identidad del proyecto o como una solución predeterminada.

El objetivo es comprender cada sistema en sus propios términos, documentar su comportamiento en condiciones reales, identificar fortalezas y limitaciones y determinar dónde podría o no encajar dentro de una arquitectura más amplia de comunicaciones resilientes.

El trabajo de campo en Arizona ha incluido pruebas de comunicación directa con dispositivos móviles, comunicaciones retransmitidas, comportamiento de múltiples saltos, pruebas de repetidores, aprendizaje de rutas y pruebas móviles/en vehículo.

La evidencia sigue siendo experimental e incompleta. Que un mensaje llegue correctamente no demuestra automáticamente que exista una cobertura confiable, y el número de saltos no representa distancia física.

## 5. Método de Investigación

El principio de trabajo del proyecto es:

> **Escuchar. Medir. Aprender. Construir.**

### Escuchar

Comprender el problema de comunicación desde la perspectiva de las personas y organizaciones que lo experimentan.

### Medir

Probar lo que realmente permiten el entorno y las tecnologías disponibles.

### Aprender

Documentar pruebas exitosas, fallas, limitaciones, incertidumbres y preguntas que requieren pruebas adicionales.

### Construir

Considerar un despliegue únicamente cuando exista una necesidad demostrada, participación comunitaria apropiada, evidencia técnica y un camino sostenible.

Este enfoque es deliberadamente basado en evidencia.

## 6. Experimentos de Campo

Antes de considerar un despliegue remoto, Community Frequency ha realizado experimentos de campo controlados en Arizona.

El registro público documenta pruebas relacionadas con:

- comunicaciones directas;
- mensajes retransmitidos;
- comportamiento de múltiples saltos;
- nodos fijos y móviles;
- comportamiento de repetidores;
- aprendizaje de rutas y caminos de comunicación;
- observaciones de señal;
- pruebas móviles/en vehículo;
- comparaciones entre Meshtastic y MeshCore.

El registro de campo conserva, cuando es posible, las observaciones separadas de las conclusiones.

También registra la incertidumbre. Por ejemplo:

- RSSI y SNR observados en un nodo intermedio no son automáticamente mediciones de RF de extremo a extremo.
- El número de saltos no representa distancia.
- La entrega de un mensaje no demuestra por sí sola que toda la ruta sea conocida.
- Los identificadores de ruta deben correlacionarse de manera independiente antes de asignarlos a un repetidor conocido.

Esta disciplina es importante porque el proyecto busca producir evidencia, no afirmaciones de marketing.

## 7. Perú 2026

Perú es el primer contexto importante de evaluación de campo de Community Frequency.

Una **misión de factibilidad prevista para septiembre de 2026** se enfocará en escuchar, observar y aprender directamente sobre las necesidades de comunicación y las condiciones locales.

El proyecto no está abordando la misión con un plan de despliegue predeterminado.

La evaluación busca investigar:

- qué comunicaciones ya están disponibles;
- dónde la conectividad convencional resulta insuficiente;
- cómo se comunican actualmente las personas cuando no existe servicio celular o de Internet;
- qué tipos de información necesitan realmente transmitir;
- las condiciones ambientales y geográficas;
- si las comunicaciones de bajo consumo podrían proporcionar conectividad local o regional útil;
- cómo sistemas existentes como HF o satélite podrían complementar las comunicaciones locales;
- consideraciones técnicas y regulatorias;
- qué sería necesario para mantener un sistema sostenible y orientado a la comunidad.

El primer objetivo es comprender la realidad sobre el terreno.

**No vamos a Perú con una solución predeterminada. Vamos a escuchar, medir y aprender.**

## 8. Una Posible Arquitectura

Uno de los conceptos que se está investigando es una arquitectura por capas en la que una comunidad no necesariamente necesita acceso directo a Internet global para obtener comunicaciones locales útiles.

Por ejemplo:

**Comunidad remota → mesh de bajo consumo → repetidor elevado/solar → ubicación conectada → HF / satélite / Internet**

Este es un concepto de investigación, no una recomendación de despliegue.

El terreno, la vegetación, la humedad, la altura de las antenas, la disponibilidad de energía, la regulación, las necesidades de la comunidad y las características de cada sistema de comunicación determinarán si una arquitectura de este tipo resulta práctica.

El proyecto está particularmente interesado en saber si un único punto conectado puede extender comunicaciones útiles hacia áreas cercanas sin requerir infraestructura convencional en cada ubicación.

## 9. Participación y Propiedad Comunitaria

Community Frequency busca explorar tecnología **con las comunidades, no simplemente para ellas**.

La capacidad técnica por sí sola no hace que un sistema de comunicaciones sea apropiado.

Cualquier despliegue futuro tendría que considerar:

- necesidades y prioridades locales;
- participación informada;
- capacitación y capacidad técnica local;
- propiedad y mantenimiento a largo plazo;
- disponibilidad de energía;
- contexto cultural;
- privacidad y seguridad;
- manejo adecuado de información sensible;
- requisitos regulatorios;
- sostenibilidad financiera.

La fase de factibilidad existe, en parte, para determinar si estas condiciones pueden cumplirse de manera realista.

## 10. Documentación y Transparencia

El repositorio público es una capa de publicación seleccionada a partir de un Master Vault privado.

El registro público busca mostrar el proceso real de desarrollo:

**qué se planeó → qué se probó → qué ocurrió → qué se aprendió → qué sigue siendo incierto → qué viene después**

La información sensible se excluye deliberadamente del registro público. Esto incluye credenciales, claves de seguridad, configuraciones privadas, información personal y datos de ubicación sensibles cuando su divulgación pueda representar un riesgo.

El proyecto también conserva las pruebas fallidas y las limitaciones, en lugar de presentar únicamente los resultados exitosos.

Esto es importante porque el proyecto sigue siendo exploratorio.

## 11. Estado Actual

**Fase 0 — Descubrimiento y Factibilidad**

Las prioridades actuales incluyen:

1. Continuar documentando y organizando los experimentos de campo realizados en Arizona.
2. Continuar evaluando Meshtastic y MeshCore sin asumir que cualquiera de ellos será la plataforma final.
3. Mejorar la comprensión del comportamiento práctico de múltiples saltos y repetidores.
4. Preparar la misión de factibilidad en Perú 2026.
5. Investigar los requisitos técnicos y regulatorios relevantes para Perú.
6. Identificar posibles colaboradores técnicos, comunitarios, de investigación y organizacionales.
7. Determinar qué evidencia sería necesaria antes de considerar cualquier despliegue real.

## 12. Qué Significa Tener Éxito

El éxito en esta etapa no significa desplegar una red.

Un esfuerzo de factibilidad exitoso podría producir una conclusión como:

- un enfoque determinado parece práctico en un entorno definido;
- varias tecnologías pueden trabajar juntas de manera efectiva;
- una arquitectura propuesta es técnicamente viable, pero requiere infraestructura adicional;
- una tecnología no es apropiada para el entorno;
- el problema de comunicación requiere una solución diferente;
- se necesita más evidencia de campo antes de tomar una decisión responsable.

Descubrir que una tecnología **no funciona** para un entorno determinado también es un resultado valioso.

## 13. Cómo Participar

Community Frequency busca conectarse con personas que puedan aportar:

- experiencia de campo;
- conocimientos de radioafición;
- experiencia con HF y antenas;
- conocimientos de radio de bajo consumo y redes mesh;
- experiencia en comunicaciones satelitales;
- conocimientos de energía solar y sistemas fuera de la red;
- experiencia en comunicaciones de emergencia;
- ingeniería e investigación;
- experiencia en despliegues remotos;
- experiencia con tecnología comunitaria;
- relaciones con organizaciones que trabajan con comunidades rurales o indígenas.

El apoyo financiero y las donaciones de equipos también pueden ayudar a financiar el trabajo de factibilidad.

## 14. El Principio Rector

Community Frequency parte de una idea sencilla:

> **Cuando termina la red, la comunidad no desaparece.**

El objetivo no es imponer tecnología a una comunidad.

El objetivo es comprender qué necesitan comunicar las personas, determinar qué permite el entorno y explorar la forma más práctica de hacer posible esa comunicación.

**Escuchar. Medir. Aprender. Construir.**
