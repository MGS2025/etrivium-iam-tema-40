# Tema 40 — Índice

> **Título oficial**: Herramientas de trabajo en grupo. Sistemas de videoconferencia. Acondicionamiento de salas y equipos.
>
> **Bloque**: Parte II — Técnico (Temas 11-40)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

---

## Estructura del tema

1. **Herramientas de trabajo en grupo**
   1.1. Arquitectura y modelos de despliegue
   1.1.1. Modelos de servicio en la nube, locales e híbridos
   1.1.2. Gestión de identidades y control de acceso federado
   1.2. Funcionalidades clave de los entornos colaborativos
   1.2.1. Comunicación e intercambio de información síncrono y asíncrono
   1.2.2. Gestión documental y edición concurrente
   1.2.3. Planificación, gestión de tareas y flujos de trabajo
   1.3. Seguridad y gobernanza del espacio de trabajo
   1.3.1. Prevención de fugas de datos y políticas de conservación
   1.3.2. Auditoría de actividad y gestión de permisos

2. **Sistemas de videoconferencia**
   2.1. Arquitecturas y principios de videoconferencia
   2.1.1. Modelos de comunicación punto a punto y multipunto
   2.1.2. Infraestructura central de conmutación: MCU y SFU
   2.2. Protocolos y transporte multimedia
   2.2.1. Protocolos de señalización H.323 y SIP
   2.2.2. El estándar WebRTC y la comunicación en tiempo real
   2.3. Códecs y calidad de servicio
   2.3.1. Códecs de compresión de audio y vídeo
   2.3.2. Calidad de servicio y gestión de ancho de banda
   2.4. Interoperabilidad e integración
   2.4.1. Integración con plataformas de trabajo en grupo
   2.4.2. Interoperabilidad entre sistemas y entornos heterogéneos

3. **Acondicionamiento de salas y equipos**
   3.1. Diseño ambiental y acondicionamiento de salas
   3.1.1. Acústica, insonorización y acondicionamiento lumínico
   3.2. Equipamiento audiovisual e infraestructura
   3.2.1. Dispositivos de captura y reproducción de audio y vídeo
   3.2.2. Visualización, cableado y electrónica de red
   3.3. Accesibilidad y mantenimiento de instalaciones
   3.3.1. Accesibilidad universal en salas multimedia
   3.3.2. Mantenimiento preventivo y gestión de incidencias

4. **Marco jurídico y aplicación en la Administración pública**
   4.1. Las sesiones a distancia de los órganos colegiados
   4.2. Protección de datos y grabación de reuniones
   4.3. Adecuación al Esquema Nacional de Seguridad

---

## Conceptos clave para memorizar

| Concepto | Dato clave |
|---|---|
| **Qué es una herramienta de trabajo en grupo** | Software que da soporte a un **grupo de personas que persiguen un objetivo común y comparten un entorno**. La disciplina que lo estudia es el **CSCW** (*Computer-Supported Cooperative Work*, término acuñado por **Grief y Cashman en 1984**) y el producto se llama **groupware**. Se descompone en **tres funciones, las 3C**: **comunicación**, **coordinación** y **colaboración** |
| **La matriz de Johansen** | Clasifica el groupware por **dos ejes: el tiempo y el lugar**. Mismo tiempo y mismo lugar: **interacción cara a cara** (sala de reuniones, pizarra). Mismo tiempo y distinto lugar: **interacción síncrona distribuida** (videoconferencia, mensajería, edición simultánea). Distinto tiempo y mismo lugar: **interacción asíncrona** (turnos, tablón). Distinto tiempo y distinto lugar: **interacción asíncrona distribuida** (correo, foro, gestor documental, flujo de trabajo). **Es el esquema de clasificación que más se pregunta** |
| **Los tres modelos de despliegue** | **SaaS** (el proveedor opera todo; la organización solo configura), **local** o *on-premise* (la organización opera todo) e **híbrido**. En España el principio rector de las AAPP **no es «nube primero» sino «nube híbrida primero»**, según la **Estrategia de nube híbrida de las Administraciones públicas** (diciembre de 2022) |
| **El precepto que extiende el ENS al proveedor** | **Artículo 2.3 del RD 311/2022**: el ENS se aplica también a **los sistemas de los proveedores privados** cuando prestan servicios o soluciones a las entidades del sector público. La medida específica es **`op.nub.1`** (protección de servicios en la nube), con **`op.ext.1` a `op.ext.4`** para los recursos externos |
| **Identidad federada: los tres protocolos** | **SAML 2.0** (OASIS, 2005; asertos XML; el clásico de la federación en AAPP) · **OpenID Connect** (capa de identidad sobre **OAuth 2.0**, `RFC 6749`, con **JWT**, `RFC 7519`) · **SCIM 2.0** (`RFC 7643` esquema y `RFC 7644` protocolo) para **aprovisionar y desaprovisionar cuentas**. **OAuth 2.0 autoriza, no autentica**: quien autentica es OIDC |
| **Edición concurrente: las tres soluciones** | **Bloqueo** (*check-out*: un solo escritor, cero conflictos, cero simultaneidad) · **Transformación operacional (OT)**, con **servidor central que reordena las operaciones** · **CRDT** (*tipo de datos replicado sin conflictos*), que **converge sin servidor central** y es la base de la edición colaborativa moderna y de los modos sin conexión |
| **Punto a punto, malla, MCU y SFU** | Con **N** participantes: la **malla** exige a cada uno **N−1 subidas y N−1 bajadas** (crece con el cuadrado y **no escala por encima de 4-6**). La **MCU** *mezcla y transcodifica*: **1 subida y 1 bajada** por participante, mucha CPU en el servidor y **una sola composición para todos**. La **SFU** *reenvía sin decodificar*: **1 subida y N−1 bajadas**, poca CPU, **maquetación libre en cada cliente** y **simulcast** para adaptarse a cada receptor. **La SFU es la arquitectura dominante hoy** |
| **H.323 frente a SIP** | **H.323** (**UIT-T**, versión vigente **8, de marzo de 2022**): arquitectura de **terminal, pasarela (*gateway*), controlador de acceso (*gatekeeper*) y unidad de control multipunto (MCU)**, codificación **binaria ASN.1/PER**, señalización **H.225.0** y control **H.245**. **SIP** (**IETF**, `RFC 3261`, 2002): **texto**, inspirado en HTTP, describe la sesión con **SDP** (**`RFC 8866`, que obsoletó a la `RFC 4566`**) mediante el modelo **oferta/respuesta** (`RFC 3264`). **Ninguno de los dos transporta media**: eso lo hace **RTP** (`RFC 3550`) |
| **WebRTC** | Conjunto de normas **W3C** (API de JavaScript) e **IETF** (protocolos), publicado como **bloque de RFC en enero de 2021**: `RFC 8825` visión general, `8826` y `8827` seguridad, `8834` RTP, `8835` transportes, `8831` canales de datos, `8837` marcado **DSCP**. **JSEP** es hoy la **`RFC 9429`** (abril de 2024), que **obsoletó a la `RFC 8829`**. **No define señalización**: la deja a la aplicación. **El cifrado es obligatorio**: **DTLS-SRTP** (`RFC 5764` y `RFC 3711`) |
| **Códecs obligatorios en WebRTC** | **Audio** (`RFC 7874`): **Opus** (`RFC 6716`) y **G.711**. **Vídeo** (`RFC 7742`): **VP8** (`RFC 6386`) **y H.264 Constrained Baseline** — los **dos**, para garantizar que dos navegadores cualesquiera se entiendan |
| **Ancho de banda de vídeo, orden de magnitud** | **H.264/AVC**: **360p ≈ 0,5 Mbit/s · 720p ≈ 1,5 Mbit/s · 1080p ≈ 3 Mbit/s**. **H.265/HEVC** y **AV1** dan la misma calidad con **≈ la mitad**; **H.266/VVC** (**publicada el 6 de julio de 2020**), con **un 40-50 % menos que HEVC**. El **audio** es despreciable en comparación: **Opus, de 6 a 510 kbit/s**, y **32 kbit/s ya es voz excelente** |
| **Presupuesto de retardo** | La **UIT-T G.114** fija el objetivo en **≤ 150 ms** de boca a oreja para una conversación cómoda; **entre 150 y 400 ms** es aceptable con reservas; **por encima de 400 ms**, inaceptable. **Fluctuación (*jitter*) por debajo de 30 ms** y **pérdida de paquetes por debajo del 1 %** |
| **Marcado DSCP para tiempo real** | `RFC 8837`: **audio EF (46)**, **vídeo AF41 (34)** en flujo de alta prioridad, y **datos** en clases inferiores. El principio que hay que saber: **el audio se prioriza por encima del vídeo**, porque una reunión sin vídeo funciona y sin audio no |
| **Travesía de NAT** | **STUN** (`RFC 8489`) descubre la dirección pública: es **barato** y no lleva tráfico. **TURN** (`RFC 8656`) **retransmite todo el media** cuando no hay camino directo: es **caro** y hay que dimensionarlo. **ICE** (`RFC 8445`) es el **algoritmo que prueba los candidatos y elige el mejor camino** |
| **Tiempo de reverberación exigible** | **CTE, Documento Básico HR** (RD 1371/2007): en **aulas y salas de conferencias vacías** de volumen **menor que 350 m³**, **T ≤ 0,7 s**; **incluyendo el total de las butacas**, **T ≤ 0,5 s**; en restaurantes y comedores vacíos, **T ≤ 0,9 s**. Por encima de **350 m³** la sala exige **estudio específico** |
| **Iluminación de una sala de reuniones** | **UNE-EN 12464-1:2022**: **500 lx** de iluminancia mantenida, **UGR ≤ 19** (deslumbramiento), **Uo ≥ 0,60** (uniformidad) y **Ra ≥ 80** (reproducción cromática), medidos sobre el **plano de trabajo a 0,85 m** |
| **DISCAS: el tamaño de la pantalla** | **ANSI/AVIXA V202.01** (edición vigente **:2026**; formulación de la edición **:2016**). Dos categorías: **decisión básica (BDM)** y **decisión analítica (ADM)**. **BDM**: `IH = FV / (200 × %EH)`, con **factor de agudeza 200**. **ADM**: `IH = (IR × FV) / 3438`, con **factor de agudeza 3438** (los minutos de arco que hay en un radián). **Espectador más cercano**: `CV = (IH + IO) × 1,732`, y **ningún espectador a más de 60° respecto de cualquier punto de la imagen** |
| **Accesibilidad de la sala y de la plataforma** | **EN 301 549** (versión armonizada citada en el DOUE: **V3.2.1, de marzo de 2021**; en España, **UNE-EN 301549:2022**), aplicable por el **RD 1112/2018** a los sitios y aplicaciones del sector público. **RD 193/2023**, exigible en bienes y servicios **nuevos de titularidad pública desde el 1 de enero de 2025** y en los existentes susceptibles de ajuste razonable **antes del 1 de enero de 2026**. **Ley 11/2023** (transposición de la Directiva (UE) 2019/882), cuyo **título I es aplicable desde el 28 de junio de 2025** |
| **Sesiones a distancia: los dos regímenes** | **Art. 17.1 de la Ley 40/2015** (régimen **general**): los órganos colegiados pueden reunirse a distancia **como regla ordinaria**, siempre que se asegure **la identidad, el contenido de las manifestaciones, el momento en que se producen, la interactividad e intercomunicación en tiempo real y la disponibilidad de los medios durante la sesión**; el **apartado 5** sitúa el acuerdo **en la sede del órgano**. **Art. 46.3 de la Ley 7/1985 (LBRL)** (régimen **local, más estricto**): solo ante **fuerza mayor, grave riesgo colectivo o catástrofe pública**, con los miembros **en territorio español** y garantizando el **carácter público o secreto** de la sesión |
| **Las medidas del ENS que tocan este tema** | **`mp.if.3`** *acondicionamiento de los locales* (temperatura y humedad, amenazas del análisis de riesgos y **protección del cableado**), **`mp.if.1`** áreas separadas y **`mp.if.2`** identificación de las personas · **`mp.eq.4`** *otros dispositivos conectados a la red*, que **nombra expresamente los «dispositivos multimedia: proyectores, altavoces inteligentes»** · **`mp.eq.1`** puesto de trabajo despejado · **`mp.s.1`** correo electrónico y **`mp.s.2`** servicios web · **`mp.info.5`** **limpieza de documentos** (metadatos, campos ocultos, comentarios y revisiones anteriores) · **`mp.com.2`** y **`mp.com.3`** · **`op.exp.8`** registro de la actividad · **`op.nub.1`** y **`op.ext.1-4`** |
| **Cifrado extremo a extremo de la colaboración** | **MLS** (*Messaging Layer Security*, **`RFC 9420`, julio de 2023**) para la **mensajería de grupo**, y **SFrame** (*Secure Frame*, **`RFC 9605`, agosto de 2024**) para el **media en tiempo real**. Son las dos piezas que permiten que **ni siquiera la SFU vea el contenido**, y **prácticamente ningún temario del mercado las recoge** |
