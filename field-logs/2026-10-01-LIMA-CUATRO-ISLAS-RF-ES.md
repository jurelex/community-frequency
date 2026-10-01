# Community Frequency — Perú 2026
## 2026-10-01 — Lima: cuatro islas de RF y una realidad de infraestructura

### Estado actual del despliegue

El despliegue de campo en Perú ya pasó de la etapa de banco y configuración a pruebas reales en sitios fijos en Lima y la costa sur.

Hasta ahora:

- Se han desplegado **dos de las tres estaciones G3** previstas para infraestructura fija.
- También se han desplegado **dos nodos solares**.
- San Borja cuenta con una estación de observación remota basada en Raspberry Pi 4, MeshMonitor y Tailscale.
- El G3 de San Borja está conectado directamente al Pi por USB mediante un puente serial de Meshtastic, evitando depender de la dirección DHCP local del G3.
- Se instaló un nodo en Miraflores aproximadamente a la altura de un séptimo piso.
- Punta Negra y Punta Hermosa tienen nodos ubicados por encima del nivel de calle.
- La conectividad MQTT con el ecosistema MeshPeru está funcionando y permite observar otros nodos.

A pesar de ello, los despliegues realizados hasta ahora han producido **cuatro islas prácticas de RF**, en lugar de una sola malla conectada.

### San Borja

San Borja es actualmente el sitio mejor instrumentado, porque la estación puede administrarse de manera remota y MeshMonitor mantiene un registro persistente de la actividad.

La expectativa era que al menos uno de los nodos conocidos de MeshPeru, descubierto a través de MQTT y aparentemente lo suficientemente cercano geográficamente a San Borja, también pudiera ser escuchado directamente por RF.

Eso todavía no ha ocurrido.

Por lo tanto, la diferencia entre visibilidad por MQTT y visibilidad por RF se ha vuelto fundamental. Ver un nodo en MeshPeru mediante MQTT no demuestra que el radio de San Borja pueda escucharlo directamente por LoRa. La posición publicada también puede ser aproximada o antigua, y siguen siendo desconocidos factores como la altura de la antena, ubicación interior, atenuación del edificio, frecuencia de transmisión o el gateway real que está reportando el nodo.

Por ahora, San Borja tiene buena observabilidad y acceso remoto, pero prácticamente no se ha detectado una malla RF útil alrededor del sitio.

### Miraflores

Se ha colocado un nodo aproximadamente a la altura de un séptimo piso en Miraflores.

A pesar de esa elevación, el nodo todavía no ha aparecido como se esperaba en las observaciones de campo.

A diferencia de San Borja, en este momento no existe una buena vía de administración remota para esa instalación, lo que hace el diagnóstico mucho más lento.

Este resultado refuerza una lección importante: estar varios pisos por encima de la calle no garantiza una buena exposición de RF. Un departamento en un séptimo piso y una instalación en la azotea son entornos muy distintos desde el punto de vista de propagación.

### Punta Negra ↔ Punta Hermosa

La separación en línea recta entre los sitios sanitizados de Punta Negra y Punta Hermosa es aproximadamente **5,4 km**.

Inicialmente, esa distancia parecía bastante razonable para LoRa. El nodo de Punta Negra se encuentra aproximadamente a la altura de un segundo piso y el de Punta Hermosa aproximadamente a la altura de un cuarto piso, por lo que ninguno está al nivel del suelo.

Sin embargo, no se ha establecido contacto RF.

La inspección física del trayecto indica que existe una colina o cresta que bloquea la línea de vista directa entre ambos sitios.

Esto cambia considerablemente la interpretación. La distancia por sí sola probablemente no sea el factor limitante. La obstrucción del terreno y la falta de despeje de la zona de Fresnel son explicaciones mucho más probables.

Cambiar a un preset LoRa más lento puede proporcionar algo más de margen de enlace, pero probablemente no compensará una obstrucción significativa de terreno. Para este trayecto, la altura o un relay en una ubicación estratégica serían más importantes que el cambio de preset.

### Cuatro islas de RF

En este momento, el despliegue del área de Lima se describe mejor como **cuatro celdas o islas de RF separadas**.

Algunos nodos pueden verse dentro de sus áreas locales, pero todavía no se ha demostrado un camino de RF útil que conecte los principales sitios de despliegue.

La única visibilidad práctica entre estas islas es, por ahora, a través de **MQTT/Internet**.

Esta distinción debe mantenerse explícita en los resultados:

> **Conectividad MQTT no es conectividad de malla RF.**

### La infraestructura se está convirtiendo en el experimento

Uno de los hallazgos más importantes del viaje hasta ahora es que la disponibilidad de equipos no es actualmente la principal limitación.

Community Frequency todavía cuenta con radios portátiles, un nodo solar, equipo Elecrow, baterías, controladores y herramientas de prueba.

El recurso difícil de conseguir es **acceso a elevación útil**.

Las ubicaciones potencialmente buenas para relays suelen ser:

- azoteas,
- pisos altos,
- colinas o crestas,
- torres,
- edificios institucionales,
- u otras propiedades que no están bajo control de Community Frequency.

El acceso a esos lugares es difícil, temporal o simplemente no está disponible.

Esto está ralentizando las pruebas porque el problema de red requiere cada vez más infraestructura en lugares donde no es posible dejar un radio fácilmente.

### Implicancias de costo y arquitectura

Una posible solución sería mover los nodos fijos desde departamentos hacia las azoteas.

Sin embargo, eso crea otro problema.

Si el nodo RF útil tiene que vivir en la azotea, pero los usuarios se encuentran varios pisos más abajo dentro de edificios de concreto armado, puede ser necesario instalar infraestructura adicional para conectar el radio de la azotea con los usuarios o dispositivos dentro del edificio.

En lugar de:

`un nodo LoRa económico por ubicación`

la arquitectura práctica podría terminar siendo:

`usuarios interiores → nodo de acceso del edificio → nodo de infraestructura en azotea → malla regional`

Eso incrementa:

- cantidad de hardware,
- complejidad de instalación,
- requerimientos de energía,
- mantenimiento,
- permisos del sitio,
- necesidades de red,
- y costo total de despliegue.

Esto es especialmente importante para Community Frequency porque una red destinada a comunidades rurales o con poca infraestructura no puede asumir acceso irrestricto a azoteas ni torres instaladas profesionalmente en cada sitio.

### Hallazgo preliminar

La expectativa inicial era que varios nodos LoRa correctamente configurados y distribuidos alrededor de Lima pudieran empezar a formar una malla útil de manera relativamente orgánica.

La evidencia inicial de campo no respalda esa suposición.

Lima está comportándose más bien como un conjunto de **celdas de RF definidas por terreno, edificios, ubicación de antenas y acceso limitado a puntos altos**.

La lección preliminar es:

> **Los radios económicos y la energía solar, por sí solos, no son suficientes para crear una malla regional resiliente. El acceso a ubicaciones estratégicamente elevadas puede ser uno de los componentes más importantes de la arquitectura de red.**

Esto no debe interpretarse como un fracaso del experimento.

Es precisamente el tipo de restricción que resulta difícil descubrir únicamente en el laboratorio.

### Próxima etapa de campo

El siguiente paso es regresar hacia Lima central.

Se llevará y monitoreará un nodo móvil durante el trayecto para observar si alguno de los nodos desplegados de Community Frequency o de MeshPeru se vuelve alcanzable por RF.

Las expectativas de que este recorrido, por sí solo, conecte las islas actuales son bajas, pero cualquier contacto será valioso.

Para cada contacto relevante se intentará conservar:

- ubicación aproximada,
- hora,
- nodo origen,
- RSSI,
- SNR,
- número de saltos,
- recepción directa o retransmitida,
- y especialmente la **procedencia RF versus MQTT**.

El nodo solar y el equipo Elecrow que todavía están disponibles pueden ser más valiosos como **sondas temporales de elevación** que como instalaciones permanentes.

En vez de intentar inmediatamente dejar otro radio fijo, el objetivo puede ser encontrar ubicaciones desde las cuales se puedan escuchar simultáneamente dos islas de RF que actualmente están aisladas.

### Estado

**ACTIVO / INCOMPLETO**

Resultado actual:

**2 radios G3 de infraestructura desplegados + 2 nodos solares desplegados → aproximadamente 4 islas de RF, sin un puente RF demostrado entre los sitios principales.**

MQTT sigue siendo, por ahora, la única vía confirmada de conectividad entre esas islas.

El problema de campo ha cambiado: ya no se trata principalmente de configurar radios, sino de identificar y conseguir acceso a la infraestructura física necesaria para colocar esos radios donde la propagación realmente funcione.
