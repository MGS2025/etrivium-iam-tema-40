# Tema 40 — Casos Prácticos

> **Título oficial**: Herramientas de trabajo en grupo. Sistemas de videoconferencia. Acondicionamiento de salas y equipos.
>
> **Formato**: 3 casos prácticos sobre supuestos reales del Ayuntamiento de Madrid. Cada caso suma **10 puntos**.
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

Los tres casos recorren el supuesto de referencia del tema (ver tema-40-contenido.md, «Convenciones»): el Ayuntamiento **despliega una plataforma corporativa de trabajo en grupo** y **acondiciona el Salón de Sesiones de una Junta Municipal de Distrito** más cinco salas de reunión pequeñas del mismo edificio. El **Caso 1** trabaja la **elección y el despliegue de la plataforma**: modelo, identidad, gobernanza de la información y encaje en el ENS y en el RGPD (§1). El **Caso 2**, el **diseño técnico y jurídico de una sesión a distancia**: arquitectura, protocolos, dimensionamiento y los requisitos que hacen válida la sesión (§2 y §4). Y el **Caso 3**, el **acondicionamiento de la sala**: diagnóstico de cuatro quejas, cálculo del tamaño de pantalla, accesibilidad y mantenimiento (§3).

---

## Caso 1 — Despliegue de la plataforma corporativa de trabajo en grupo

### Enunciado

El Instituto de Informática del Ayuntamiento de Madrid (IAM) debe implantar una **plataforma corporativa de trabajo en grupo** para el personal municipal. Datos de partida:

- Alcance: **aproximadamente 28.000 empleados** municipales, con **rotación y movilidad interna elevadas** entre áreas y distritos.
- Servicios que debe cubrir: **correo, mensajería, calendario, repositorio documental, edición colaborativa y reuniones**.
- El **teletrabajo** está implantado conforme al artículo 47 bis del TREBEP y afecta a una parte significativa de la plantilla.
- Coexisten **dos tipos de información** muy distintos: información **organizativa interna** (convocatorias, actas de coordinación, borradores) e información de **expedientes** con datos personales de vecinos.
- El sistema está categorizado como **MEDIA** en las dimensiones de confidencialidad, integridad, trazabilidad y autenticidad, y **ALTA** en disponibilidad para los servicios de atención a la ciudadanía.
- Colaboran habitualmente con la plataforma **empresas adjudicatarias** y **colegios profesionales** externos.
- Una auditoría interna previa detectó **1.400 cuentas activas de personas que ya no prestan servicio** y **más de 3.000 carpetas compartidas mediante enlaces abiertos sin caducidad**.

Se pide un informe técnico previo a la licitación.

### Cuestiones

**Cuestión 1 — Modelo de despliegue y frontera de responsabilidad (3 puntos).** Proponga el **modelo de despliegue** para cada uno de los cuatro bloques de servicio (correo y mensajería; calendario y reuniones; repositorio de expedientes; directorio de identidad), justificando cada elección. Explique el reparto de responsabilidades que resulta y **cite las medidas del ENS que se activan** por el hecho de contratar el servicio a un tercero, con su aplicación por categoría.

**Cuestión 2 — Identidad y las 1.400 cuentas huérfanas (3 puntos).** Diseñe la **arquitectura de identidad**: qué protocolo resuelve cada función, cómo se integra a los externos y, en particular, **qué mecanismo impide que vuelvan a aparecer cuentas huérfanas**. Indique las medidas del ENS aplicables.

**Cuestión 3 — Gobernanza de la información y las 3.000 carpetas abiertas (2 puntos).** Proponga los **controles** que corrigen el hallazgo de las carpetas compartidas y establezca una **política de conservación** diferenciada por tipo de contenido, conciliando las dos fuerzas normativas que operan en sentido contrario. Cite las medidas del ENS y los preceptos del RGPD aplicables.

**Cuestión 4 — Publicación de documentos y protección de datos (2 puntos).** El Ayuntamiento publicará en su portal de transparencia documentos elaborados de forma colaborativa en la plataforma. Identifique el **riesgo específico** que ese flujo introduce, la **medida del ENS** que lo aborda y las **obligaciones de protección de datos** derivadas de la contratación del servicio.

### Solución orientativa

- **C1**: (§1.1.1) El reparto razonable **no es un modelo único**, y se valora expresamente que el opositor no dé una respuesta uniforme:

| Bloque de servicio | Modelo propuesto | Justificación |
|---|---|---|
| **Correo y mensajería** | **SaaS** | Disponibilidad crítica, con picos, y se beneficia de la escala del proveedor. La información es sensible pero sobre todo organizativa |
| **Calendario y reuniones** | **SaaS** | Mismo razonamiento, con el añadido de que la interoperación externa (invitaciones, reuniones con otras Administraciones) es mucho más fácil desde la nube |
| **Repositorio de expedientes** | **Nube privada o instalación propia** | Pesan la **jurisdicción de los datos**, la medida `mp.info.1` y la **evaluación de impacto** del art. 35 del RGPD. Es el bloque donde el riesgo justifica el coste de operar |
| **Directorio de identidad** | **Interno**, federado hacia fuera | Debe ser la **fuente de la verdad**, para que una baja se ejecute en un solo sitio y se propague |

  El resultado es un modelo **híbrido**, que es exactamente lo que recomienda la **Estrategia de nube híbrida de las Administraciones públicas** de diciembre de 2022: el principio español **no es «nube primero» sino «nube híbrida primero»**, con **NubeSARA** como nube privada de referencia.

  **Frontera de responsabilidad.** Rige el modelo de **responsabilidad compartida**: el proveedor responde de la seguridad **del** servicio —plataforma parcheada, centro de datos, redundancia— y el Ayuntamiento, de la seguridad **en** el servicio: quién tiene cuenta, con qué permisos, con qué política de compartición externa y con qué conservación. Se valora que se señale que **los dos hallazgos de la auditoría son responsabilidad íntegra del cliente**, no del proveedor.

  **Medidas del ENS que se activan.** El fundamento es el **artículo 2.3 del RD 311/2022**, que extiende el ENS a los sistemas de los proveedores privados que prestan servicios al sector público. De ahí:

| Medida | Contenido | Aplicación en el supuesto (categoría MEDIA) |
|---|---|---|
| **`op.nub.1`** | Protección de servicios en la nube | Aplica **ya en BÁSICA**; en MEDIA, **+ R1** (servicios certificados). Sus cuatro exigencias: **pruebas de penetración, transparencia, cifrado y gestión de claves y jurisdicción de los datos** |
| **`op.ext.1`** | Contratación y acuerdos de nivel de servicio | Aplica en MEDIA. Es donde encaja el contrato del art. 28 del RGPD |
| **`op.ext.2`** | Gestión diaria | Aplica en MEDIA |
| **`op.ext.4`** | Interconexión de sistemas | Aplica en MEDIA (**+ R1 en ALTA**) |
| **`op.ext.3`** | Protección de la cadena de suministro | **No aplica**: solo en categoría ALTA |

  Se valora que se cite la existencia de las **guías CCN-STIC** que materializan todo esto —la serie **885**, con una guía específica para la herramienta de reuniones y trabajo en equipo, y la **CCN-STIC-823** sobre utilización de servicios en la nube—, y que se redacte la prescripción **sin marca**, conforme al **art. 126.6 de la LCSP**.

- **C2**: (§1.1.2) La arquitectura se articula en **tres protocolos con tres funciones distintas**, y la respuesta debe separarlas sin ambigüedad:

| Función | Protocolo | Papel en el supuesto |
|---|---|---|
| **Autenticar** | **SAML 2.0** (OASIS, 2005) u **OpenID Connect** sobre **OAuth 2.0** (`RFC 6749`), con testigo **JWT** (`RFC 7519`) | El empleado se autentica ante el **directorio municipal**; a la plataforma solo llega un **aserto o testigo firmado**. La contraseña nunca sale del Ayuntamiento |
| **Autorizar** | **OAuth 2.0** | Permisos delegados de aplicaciones que actúan en nombre del usuario. Por sí solo **no autentica** |
| **Aprovisionar** | **SCIM 2.0** (`RFC 7643` esquema, `RFC 7644` protocolo) | **Es la respuesta al hallazgo de las 1.400 cuentas huérfanas** |

  **El mecanismo que impide que reaparezcan** es **SCIM enlazado al sistema de personal como fuente autoritativa**: el alta, el cambio de destino y, sobre todo, **la baja** se propagan automáticamente a la plataforma. Se valora expresamente que se señale que **sin SCIM la baja depende de que alguien la recuerde**, y que con 28.000 empleados y alta rotación eso es una garantía inexistente. Complemento imprescindible: **asignar permisos a grupos y no a personas**, con la pertenencia al grupo determinada por el puesto, de modo que un cambio de destino reajuste los permisos solo y no se produzca **acumulación de privilegios**.

  **Los externos** no deben recibir cuentas municipales. Las dos vías correctas, por este orden: **federación con el proveedor de identidad de la empresa o colegio profesional**, o **acceso de invitado autenticado con segundo factor**. En ambos casos, con **fecha de caducidad**, **revisión periódica** y **etiqueta visible de externo** en la interfaz de la reunión.

  **Medidas del ENS**: `op.acc.5` (mecanismo de autenticación de **usuarios externos**), `op.acc.6` (**usuarios de la organización**) —ambas empujan al **segundo factor** en categoría MEDIA—, `op.acc.4` (**proceso de gestión de derechos de acceso**, aplicable en las tres categorías, que es el que exige la revisión) y `op.acc.3` (**segregación de funciones y tareas**, que **no aplica en BÁSICA** pero sí aquí).

- **C3**: (§1.3) **Controles frente a las carpetas abiertas**, en el orden en que hay que aplicarlos:

  1. **Cambiar el valor por omisión** de la compartición: que un enlace nazca **restringido a la organización**, y que abrirlo al exterior sea una acción deliberada y registrada.
  2. **Caducidad obligatoria** en toda compartición externa, con renovación expresa.
  3. **Etiquetado y clasificación** del contenido (`mp.info.2`, dimensión de confidencialidad, **no aplica en nivel BAJO** y sí aquí), del que cuelgan políticas automáticas.
  4. **Prevención de fugas de datos (DLP)** sobre patrones —DNI, cuenta bancaria, número de la Seguridad Social— combinados con la etiqueta y el contexto. Se valora que se advierta de que **una implantación que empieza bloqueando en lugar de avisando termina desactivada**, y que **el mayor vector de fuga es el accidental**, no el malicioso.
  5. **Campaña de revisión** de las 3.000 comparticiones existentes, con caducidad automática de las que nadie reclame.
  6. **Registro** de toda la actividad: `op.exp.8`, aplicable en las tres categorías, con **cuatro refuerzos en nivel MEDIO**.

  **Política de conservación.** Las dos fuerzas: el **RGPD empuja a borrar** —**minimización**, art. 5.1.c), y **limitación del plazo de conservación**, art. 5.1.e)— y la **normativa de archivo y la necesidad probatoria empujan a conservar**. Se concilian con **retención diferenciada por tipo de contenido** y **retención legal** como excepción que congela el borrado mientras dure un procedimiento:

| Contenido | Retención propuesta |
|---|---|
| Mensajería instantánea | **Corta** |
| Correo electrónico | **Media** |
| Documento incorporado a expediente | La que fije la **normativa de archivo** |
| Grabación de reunión de trabajo | **La más corta de todas**, con borrado automático |

  Se valora que se diga expresamente que **guardar todo para siempre no es prudencia: es un incumplimiento**.

- **C4**: (§1.3.1 y §4.2) **El riesgo específico** es que el documento elaborado de forma colaborativa **arrastra al portal el historial de quién escribió qué, los comentarios internos y los cambios rechazados**. Es un riesgo propio de la edición concurrente y no existe cuando el documento lo redacta una sola persona.

  **La medida del ENS** que lo aborda es **`mp.info.5`, «Limpieza de documentos»**: exige retirar «toda la información adicional contenida en **campos ocultos, metadatos, comentarios o revisiones anteriores**, salvo cuando dicha información sea pertinente para el receptor», y su texto subraya que **es especialmente relevante cuando el documento se difunde ampliamente, como al ofrecerlo al público en un servidor web**. Tiene dimensión de confidencialidad y **aplica en los tres niveles, incluido el BAJO**. Se valora que se proponga incorporar la limpieza **al propio flujo de publicación**, de forma automática, y no dejarla al cuidado de quien publica.

  **Obligaciones de protección de datos derivadas de la contratación**: el proveedor es **encargado del tratamiento** (**art. 28** del RGPD) y hace falta contrato con el contenido que el artículo exige; si trata datos fuera del Espacio Económico Europeo, hay que resolver la **base de la transferencia** (**arts. 44 a 49**), que es lo que `op.nub.1.2` llama **jurisdicción de los datos**; procede **evaluación de impacto** (**art. 35**) al menos para el bloque de expedientes; y hay que informar y fijar plazos conforme al **art. 13** y al **art. 5**. Se valora la mención de los **artículos 87 y 88 de la LOPDGDD** —intimidad en el uso de los dispositivos digitales y **desconexión digital**— por su incidencia sobre el registro de actividad y sobre la presencia publicada del empleado.

### Criterios de evaluación

| Cuestión | Puntos | Se valora |
|---|---|---|
| C1 | 3 | Que **no dé un modelo único** sino un reparto justificado por bloque · «nube híbrida primero» y no «nube primero» · responsabilidad compartida bien enunciada · **art. 2.3** del ENS como fundamento · `op.nub.1` con sus cuatro exigencias y `op.ext` con sus excepciones por categoría |
| C2 | 3 | Separar **autenticar, autorizar y aprovisionar** sin confundirlos · **SCIM como respuesta a las cuentas huérfanas** · permisos por grupo y no por persona · externos por federación o invitación con caducidad, nunca con cuenta municipal · `op.acc.3` a `op.acc.6` |
| C3 | 2 | Cambiar el valor por omisión antes que perseguir enlaces · caducidad obligatoria · advertencia sobre el DLP que bloquea de entrada · las **dos fuerzas** del RGPD y del archivo, y su conciliación por tipo de contenido · `op.exp.8` |
| C4 | 2 | Identificar el riesgo como **propio de la edición colaborativa** · citar **`mp.info.5`** con su contenido y su alcance en los tres niveles · automatizar la limpieza en el flujo de publicación · art. 28, arts. 44-49 y art. 35 del RGPD |

---

## Caso 2 — Sesión a distancia de una Junta Municipal de Distrito

### Enunciado

Por una **situación excepcional de grave riesgo colectivo** apreciada por el Concejal Presidente, la **Junta Municipal de un Distrito** debe celebrar su sesión ordinaria **a distancia**. Datos de partida:

- El órgano tiene **26 miembros** con derecho a voto, más **secretario** y **personal técnico de apoyo**.
- **18 miembros** se conectarán desde su domicilio o despacho, cada uno con su equipo. **8 miembros y el secretario** estarán presentes en el **Salón de Sesiones**, que dispone de **un único terminal de sala**.
- La sesión es **pública** y debe **retransmitirse a la ciudadanía**; se estima una audiencia de **hasta 900 personas**.
- El Salón de Sesiones conserva un **equipo de videoconferencia heredado basado en H.323**, que se usa para conectar con otras dependencias municipales.
- La plataforma corporativa es de **arquitectura SFU** y se accede por navegador.
- Cada participante remoto envía **720p a 1,5 Mbit/s** y **audio a 40 kbit/s**; recibe **un flujo destacado a 720p** y **hasta 8 flujos pequeños a 180p (0,2 Mbit/s)**, más el audio de los **3 locutores más activos**.
- El enlace del edificio de la Junta es de **100 Mbit/s simétricos**, compartido con el resto de la actividad de la sede.

Se pide un informe técnico y jurídico previo a la sesión.

### Cuestiones

**Cuestión 1 — Arquitectura y flujos (3 puntos).** Justifique por qué **no procede** una arquitectura en malla y calcule los flujos que generaría. Determine la **arquitectura adecuada** para cada uno de los tres colectivos —miembros remotos, sala y ciudadanía— y explique qué elemento hace falta para integrar el equipo heredado H.323, con su coste.

**Cuestión 2 — Dimensionamiento del enlace (3 puntos).** Calcule el **ancho de banda de subida y de bajada** que consume el Salón de Sesiones y valore si el enlace de 100 Mbit/s es suficiente. Identifique el **error de dimensionamiento más frecuente** en un supuesto como este y su corrección. Proponga la configuración de **calidad de servicio** con los umbrales y el marcado aplicables.

**Cuestión 3 — Régimen jurídico de la sesión (2 puntos).** Determine **qué norma rige** la celebración a distancia de esta sesión, qué requisitos impone y en qué se diferencia del régimen general. Indique además dónde se entienden adoptados los acuerdos.

**Cuestión 4 — Traducción técnica de los requisitos jurídicos y plan de respaldo (2 puntos).** Traduzca a **especificaciones concretas del sistema** los cinco requisitos del artículo 17.1 de la Ley 40/2015 y diseñe el **plan de respaldo**. Explique qué debe hacer el personal técnico si un miembro pierde la conexión durante una votación.

### Solución orientativa

- **C1**: (§2.1) **La malla queda descartada por cálculo**, no por criterio. Con **N = 27** puntos finales, cada uno sostendría `27 − 1 = 26` subidas y 26 bajadas, y el sistema, `27 × 26 = **702 flujos**`. La carga por participante sería `26 × 1,54 = **40 Mbit/s de subida**`, cifra fuera del alcance de cualquier conexión doméstica. Se valora que se explicite que **el crecimiento es cuadrático en el sistema y lineal en cada participante**, y que **la restricción que muerde primero es la subida**, porque en una conexión típica es muy inferior a la bajada.

  **Arquitectura por colectivo**, que es el punto que discrimina una respuesta buena:

| Colectivo | Arquitectura | Razón |
|---|---|---|
| **18 miembros remotos** | **SFU** | Conexiones muy dispares; cada uno compone su vista; coste de servidor bajo; **simulcast** (`RFC 8853`) adapta la calidad a cada receptor |
| **Sala (8 miembros + secretario)** | **Un único terminal de sala** conectado a la misma SFU | No son 9 participantes: **son uno**. Es la corrección del error de la C2 |
| **900 personas de la ciudadanía** | **Difusión**, no videoconferencia | No hay interacción: la restricción de retardo se relaja y la escalabilidad se resuelve con distribución escalonada o segmentos, con varios segundos de retardo |

  Se valora expresamente la distinción del tercer colectivo: **retransmitir un pleno no es una videoconferencia**, y tratarlo como tal es un error de diseño costoso.

  **Integración del equipo H.323 heredado.** Hace falta una **pasarela** que traduzca la señalización entre H.323 y el mundo SIP o WebRTC de la plataforma. Si además los códecs no coinciden, hará falta **transcodificación**, es decir, decodificar y recodificar el media, **con coste de cómputo, retardo y calidad**, porque cada recodificación degrada. Se valora la conclusión de fondo: **la arquitectura no la elige la moda, la elige el terminal más viejo que hay que admitir**; y la recomendación práctica de comprobar con antelación si el equipo heredado es realmente necesario en esta sesión, porque evitarlo ahorra la pasarela.

- **C2**: (§2.3.2) **Cálculo para el terminal de sala**:

  *Bajada.* Vídeo: `1,5 + (8 × 0,2) = 1,5 + 1,6 = 3,1 Mbit/s`. Audio de los tres locutores: `3 × 0,04 = 0,12 Mbit/s`. Subtotal `= 3,22 Mbit/s`. Con un **30 % de margen** por encabezados y ráfagas: `3,22 × 1,3 ≈ **4,2 Mbit/s**`.

  *Subida.* `1,5 + 0,04 = 1,54 Mbit/s`; con el 30 %: `≈ **2,0 Mbit/s**`.

  *Retransmisión a la ciudadanía.* Si se emite desde la sede, hay que **sumar el flujo de salida hacia la plataforma de difusión** —del orden de **3 a 6 Mbit/s** para 1080p—, no 900 veces ese valor: **la distribución a los 900 espectadores la hace la plataforma, no el edificio**. Se valora que se detecte este punto, porque el error inverso —multiplicar por la audiencia— es frecuente.

  *Valoración del enlace.* **100 Mbit/s simétricos son holgadamente suficientes** para unos 8 a 10 Mbit/s de necesidad total. Pero se valora que se diga que **la cifra no es lo que hay que contratar, sino lo que hay que reservar**, y que el riesgo real no es la capacidad sino **la competencia con el resto del tráfico de la sede**.

  **El error de dimensionamiento más frecuente**, y es el que el enunciado prepara deliberadamente: **suponer que los 8 miembros presentes en la sala se conectan cada uno con su portátil**. En ese caso la subida sería `8 × 1,54 × 1,3 ≈ **16 Mbit/s**` en lugar de 2, y aparecerían además **eco y acoplamiento** por tener ocho micrófonos y ocho altavoces abiertos en la misma habitación. **La corrección no es más ancho de banda: es un solo terminal de sala**, con el resto de los equipos con micrófono y altavoz apagados.

  **Calidad de servicio.** Umbrales aplicables: **retardo ≤ 150 ms** de boca a oreja (**UIT-T G.114**; hasta 400 ms tolerable, por encima inaceptable), **fluctuación < 30 ms** y **pérdida < 1 %**. Marcado conforme a la **`RFC 8837`**: **audio EF (46)**, **vídeo AF41 (34)** y datos en clases inferiores, con la regla de fondo de que **el audio se prioriza por encima del vídeo**. Se valora la cautela de que **el marcado solo sirve dentro del dominio administrativo propio**: fuera de la red municipal el DSCP se puede reescribir o ignorar, y allí lo que sostiene la sesión es la **adaptación del códec por control de congestión** (`RFC 8836`).

- **C3**: (§4.1) **La norma aplicable es el artículo 46.3 de la Ley 7/1985, reguladora de las Bases del Régimen Local**, no el artículo 17 de la Ley 40/2015. Es el error que el caso busca provocar, y distinguirlo es lo que vale los puntos.

| | **Art. 17 de la Ley 40/2015 (general)** | **Art. 46.3 de la LBRL (local, el aplicable)** |
|---|---|---|
| Carácter | La sesión a distancia es la **regla ordinaria**, salvo prohibición expresa del reglamento interno | **Excepcional** |
| Presupuesto habilitante | Ninguno | **Fuerza mayor, grave riesgo colectivo o catástrofe pública**, apreciados por el alcalde o presidente |
| Ubicación de los miembros | Sin restricción | **En territorio español** |
| Publicidad | No lo menciona | Debe garantizarse el **carácter público o secreto** de la sesión |
| Medios válidos | Correo electrónico, **audioconferencias** y videoconferencias | Audioconferencias, videoconferencias u otros sistemas que garanticen **seguridad tecnológica, efectiva participación política, validez del debate y de la votación** |

  En el supuesto **concurre el presupuesto habilitante** —grave riesgo colectivo apreciado por el Concejal Presidente—, de modo que la sesión **puede celebrarse a distancia**, siempre que los 18 miembros remotos se encuentren **en territorio español**, quede **acreditada su identidad** y se garantice el **carácter público** de la sesión, que en este caso se satisface con la retransmisión a la ciudadanía.

  **Dónde se entienden adoptados los acuerdos.** Conforme al **artículo 17.5 de la Ley 40/2015**, aplicable supletoriamente, **en el lugar donde tenga la sede el órgano colegiado** y, en su defecto, donde esté ubicada la presidencia. No en el domicilio de quienes votan.

- **C4**: (§4.1) **Traducción de los cinco requisitos**:

| Requisito del art. 17.1 | Especificación técnica |
|---|---|
| **Identidad** de los miembros | Acceso con **identidad federada** municipal y **segundo factor**; nombre mostrado **verificado y no editable** por el participante; **nunca** enlace anónimo. Refuerzo con vídeo activo durante la intervención |
| **Contenido** de las manifestaciones | **Audio inteligible** —lo que exige el acondicionamiento del Caso 3— y **grabación** o acta detallada, con transcripción como apoyo |
| **Momento** en que se producen | **Marca de tiempo** fiable en la grabación y **registro de conexiones y desconexiones**, que es lo que acredita **quién estaba presente en cada votación** |
| **Interactividad en tiempo real** | Retardo **dentro del umbral de la G.114** y **canal de petición de palabra**, para que ninguna intervención llegue fuera de turno |
| **Disponibilidad** de los medios durante la sesión | **Redundancia**: enlace de respaldo, **acceso telefónico**, equipo alternativo en sala y **comprobación previa protocolizada** |

  **Plan de respaldo**, que debe estar escrito antes de la sesión: (a) **número de acceso telefónico** publicado en la convocatoria —el artículo 17.1 admite expresamente la **audioconferencia**, de modo que quien entre por teléfono participa válidamente—; (b) **enlace de datos alternativo** en la sede, por ejemplo móvil; (c) **equipo de sala de reserva**; y (d) **comprobación previa** con prueba de audio bidireccional, de vídeo, de compartición de contenido, del enlace y de las credenciales, y verificación de la grabación.

  **Qué hacer si un miembro pierde la conexión durante una votación.** Es el punto de más valor de todo el caso. **No ha ocurrido una incidencia informática: ha ocurrido un posible vicio de procedimiento**, porque el requisito de **disponibilidad de los medios durante la sesión** ha dejado de cumplirse para ese miembro. La instrucción correcta al personal técnico es: **comunicarlo de inmediato a la secretaría del órgano**, que es quien decide si se suspende, se repite la votación o se hace constar en acta; **no** intentar resolverlo en silencio ni dejar que la votación se cierre. Se valora que se concluya que, por esta razón, **la comprobación previa y el respaldo telefónico no son buenas prácticas de mantenimiento sino medidas de garantía jurídica**.

### Criterios de evaluación

| Cuestión | Puntos | Se valora |
|---|---|---|
| C1 | 3 | Descartar la malla **por cálculo** (702 flujos, 40 Mbit/s de subida) y no por criterio · arquitectura **distinta por colectivo** · reconocer que **la retransmisión a 900 personas es difusión, no videoconferencia** · pasarela y, en su caso, transcodificación para el H.323, con su coste |
| C2 | 3 | Cálculo correcto de 4,2 Mbit/s de bajada y 2,0 de subida con el margen · no multiplicar la retransmisión por la audiencia · detectar el **error de los ocho portátiles** y corregirlo con **un solo terminal de sala** · umbrales de G.114, fluctuación y pérdida · marcado **EF y AF41** con la cautela del dominio propio |
| C3 | 2 | Aplicar el **art. 46.3 de la LBRL** y **no** el art. 17 de la Ley 40/2015 · los tres requisitos exclusivos del régimen local · verificar que concurre el presupuesto habilitante · el acuerdo se adopta **en la sede del órgano** |
| C4 | 2 | Traducir los **cinco** requisitos a especificaciones concretas · plan de respaldo con **acceso telefónico** como medio válido · y sobre todo: identificar la caída durante la votación como **posible vicio de procedimiento** y comunicarlo a la secretaría |

---

## Caso 3 — Acondicionamiento del Salón de Sesiones y de las salas de reunión

### Enunciado

Tras la sesión del Caso 2, la Junta de Distrito recibe **cuatro quejas** y encarga al IAM un informe de acondicionamiento del **Salón de Sesiones** y de las **cinco salas de reunión** del edificio. Datos de partida:

- El **Salón de Sesiones** mide **14 × 9 × 3,8 m** (**478,8 m³**), tiene **suelo de mármol**, **paredes lisas enfrentadas** y **techo de escayola continua**. Dispone de una **pantalla de 75 pulgadas** (altura de imagen **0,93 m**), instalada con el borde inferior a **1,10 m** del suelo. El asistente más alejado se sitúa a **9,5 m** de la pantalla.
- Las **cinco salas de reunión** son **despachos reconvertidos**, con suelo duro, paredes lisas enfrentadas, y la mesa colocada **con la ventana detrás** de quien preside.
- En cada sala de reunión, el equipo consiste en **un portátil en el centro de una mesa de doce plazas**.
- Las cuatro quejas recibidas:
  1. «Desde casa **no se entendía** lo que decían los que estaban en el salón; se oía como en una cueva».
  2. «Cuando yo hablaba, **me oía a mí mismo** un instante después».
  3. «Los concejales que estaban en la sala **salían como sombras**, no se les veía la cara».
  4. «**No se leía** lo que se proyectaba en la pantalla desde las últimas filas».
- Una vecina con discapacidad auditiva presentó además un **escrito solicitando** que las sesiones sean accesibles.

Se pide un informe técnico con diagnóstico, propuesta y plan de mantenimiento.

### Cuestiones

**Cuestión 1 — Diagnóstico de las cuatro quejas (3 puntos).** Identifique la **causa técnica** de cada una de las cuatro quejas, **sin confundir fenómenos distintos**, y proponga la corrección de cada una. Indique la norma aplicable donde exista.

**Cuestión 2 — Acondicionamiento acústico y lumínico del Salón de Sesiones (2 puntos).** Determine qué exige el **Documento Básico HR** del Código Técnico de la Edificación a un recinto de estas dimensiones y qué procede en consecuencia. Indique los valores de **iluminación** exigibles y las reglas específicas de una sala de videoconferencia.

**Cuestión 3 — Cálculo del tamaño de pantalla conforme a DISCAS (3 puntos).** Compruebe si la pantalla de 75 pulgadas cumple para **decisión básica** con un contenido cuyo elemento más pequeño tiene un **%EH del 2 %**. Calcule la **altura de imagen necesaria** y la **distancia máxima admisible** con la pantalla actual. Compruebe también el **espectador más cercano** y proponga alternativas si la pantalla necesaria no cabe.

**Cuestión 4 — Accesibilidad y mantenimiento (2 puntos).** Enumere las medidas de **accesibilidad** que procede adoptar y el **marco normativo** aplicable con sus plazos. Diseñe el **plan de mantenimiento** del parque de seis salas y su encaje con la gestión del servicio y con el ENS.

### Solución orientativa

- **C1**: (§3.1 y §3.2) Las cuatro quejas describen **cuatro fenómenos distintos**, y el mérito de la respuesta está en no mezclarlos:

| Queja | Fenómeno | Causa | Corrección |
|---|---|---|---|
| 1. «Como en una cueva» | **Reverberación** excesiva | Suelo de mármol, paredes lisas y techo continuo: superficies duras y reflectantes, sin absorción. El micrófono capta la sala entera y no solo la voz | **Acondicionamiento acústico**: techo absorbente, tratamiento de al menos una pared, moqueta o alfombra. Medición conforme a la **UNE-EN ISO 3382** |
| 2. «Me oía a mí mismo» | **Eco acústico** | Lo que sale por el altavoz vuelve a entrar por el micrófono y se reenvía al emisor con retardo | **Cancelación de eco acústico (AEC)**, exigida por la `RFC 7874` a todo punto final WebRTC. En sala grande, con **supresión de realimentación**, **compuertas de ruido** y **mezcla automática** |
| 3. «Salían como sombras» | **Contraluz** | La luz principal viene de detrás del sujeto y la cámara expone para el fondo | **Reorientar la mesa** para que la luz venga de frente; luz **difusa** y no directa. Es la corrección más barata de todas |
| 4. «No se leía la pantalla» | **Tamaño de imagen insuficiente** para la distancia | La pantalla no cumple los requisitos de la norma de tamaño de imagen para el espectador más lejano | Recalcular conforme a **DISCAS** (cuestión 3) |

  Se valora **explícitamente** que no se confundan los tres fenómenos acústicos: **reverberación** (cola sonora de la sala, problema de acondicionamiento), **eco** (retorno de la propia voz, problema de cancelación) y **acoplamiento** (pitido por realimentación, problema de ganancia). Y que se señale la **relación entre señal y ruido**: depende del cuadrado de la distancia, de modo que **acercar el micrófono a la mitad de distancia mejora unos 6 dB**, y por eso **el portátil solitario en el centro de una mesa de doce plazas es el peor montaje posible**. En las cinco salas pequeñas, la respuesta correcta es un **micrófono cercano o de haz conformado** y **techo absorbente**, no una cámara mejor.

- **C2**: (§3.1.1) El Salón mide **478,8 m³**, es decir, **por encima de los 350 m³**. En consecuencia, **el Documento Básico HR no fija un valor límite de tiempo de reverberación para este recinto**: procede un **estudio específico de acondicionamiento acústico**. Se valora que se sepa el umbral y que **no se aplique mecánicamente el valor de 0,7 s**.

  Para contexto y para las cinco salas pequeñas, que sí están por debajo del umbral, los valores del apartado 2.2 del **DB-HR** son: **0,7 s** en aula o sala de conferencias **vacía**, sin ocupación ni mobiliario; **0,5 s** en la misma **incluyendo el total de las butacas**; y **0,9 s** en restaurantes y comedores vacíos.

  Conviene añadir el criterio de **ruido de fondo**, que el CTE no fija pero que la práctica profesional sitúa en **NC-25 a NC-30**, del orden de **35 a 40 dBA**, y declararlo como criterio de diseño y no como exigencia reglamentaria. Y las tres **reglas geométricas**: evitar superficies paralelas duras enfrentadas —que es exactamente el defecto del Salón—, evitar plantas cuadradas exactas y evitar paredes cóncavas.

  **Iluminación.** Conforme a la **UNE-EN 12464-1:2022**, para oficinas y salas de reuniones y conferencias: **500 lx** de iluminancia mantenida, **UGR ≤ 19**, **Uo ≥ 0,60** y **Ra ≥ 80**, sobre el plano de trabajo a **0,85 m** del suelo. A ello se añaden las **tres reglas propias de una sala de vídeo**: (1) **luz de frente y no de detrás**; (2) **luz difusa y no puntual**; y (3) **iluminación zonificada y regulable**, porque la luz ambiente que cae sobre la pantalla **reduce la relación de contraste** —es el objeto de la norma **ANSI/AVIXA V201.01:2021**— y, si se apagan las luces para ver la proyección, **los participantes remotos dejan de ver a nadie**.

- **C3**: (§3.2.2) Aplicación de **DISCAS (ANSI/AVIXA V202.01)**, categoría de **decisión básica**, factor de agudeza **200**:

  *Altura de imagen necesaria para el espectador más lejano.*
  `IH = FV / (200 × %EH) = 9,5 / (200 × 0,02) = 9,5 / 4 = **2,375 m**`

  *Comprobación de la pantalla actual.* La pantalla de 75 pulgadas tiene **IH = 0,93 m**, muy por debajo de los 2,375 m necesarios. **No cumple.**

  *Distancia máxima admisible con la pantalla actual.*
  `FV = IH × %EH × 200 = 0,93 × 0,02 × 200 = **3,72 m**`

  Es decir, con la pantalla instalada **solo cumplen las primeras filas, hasta 3,72 m**, frente a los 9,5 m reales. **La queja 4 está técnicamente fundada.**

  *Espectador más cercano.* El desplazamiento vertical de la imagen respecto de la altura del ojo de un espectador sentado —tomada convencionalmente en torno a **1,10 m**— es aproximadamente `IO ≈ 0`, ya que el borde inferior está a 1,10 m. Con la pantalla actual: `CV = (IH + IO) × 1,732 = (0,93 + 0) × 1,732 ≈ **1,61 m**`. Ningún asiento está tan cerca, de modo que **por este lado no hay incumplimiento**. Debe comprobarse además la restricción horizontal: **ningún espectador a más de 60°** respecto de cualquier punto de la imagen, lo que en una sala de 14 m de ancho obliga a revisar los asientos de los extremos de las primeras filas.

  *Alternativas si una imagen de 2,375 m de altura no cabe.* Se valora que la respuesta **no sea resignarse**, sino ofrecer las tres salidas de la norma:

  1. **Aumentar el tamaño del contenido**, es decir, subir el **%EH**. Con un **%EH del 5 %** —tipografía grande de presentación—, `IH = 9,5 / (200 × 0,05) = **0,95 m**`: la pantalla actual, con 0,93 m, **se queda a dos centímetros y todavía no cumple**. Con un **%EH del 6 %**, `IH = 9,5 / 12 = **0,79 m**`, y entonces **sí cumple con margen**. La lección, que es el hallazgo del ejercicio: **el tamaño de letra de la presentación es una variable de diseño de la sala**, y una plantilla corporativa con tipografía grande puede ahorrar una obra.
  2. **Acercar al espectador más lejano**, reorganizando la disposición de los asientos.
  3. **Instalar una imagen mayor** —pared de LED o proyección— o **pantallas de refuerzo** intermedias para las filas traseras.

  Se valora la conclusión de fondo: **la pantalla que la norma exige suele ser bastante mayor que la que se instala por costumbre**, y la comprobación cuesta dos operaciones aritméticas.

- **C4**: (§3.3) **Accesibilidad.** El escrito de la vecina obliga a actuar, y el marco es triple:

| Norma | Contenido | Plazo |
|---|---|---|
| **RD 1112/2018** | Accesibilidad de sitios web y aplicaciones móviles del sector público conforme a la **EN 301 549** (versión citada en el DOUE: **V3.2.1**, de 2021; en España, **UNE-EN 301549:2022**), con **declaración de accesibilidad** y mecanismo de queja | Vigente |
| **RD 193/2023** | Condiciones básicas de accesibilidad de **los bienes y servicios a disposición del público** | **1 de enero de 2025** para los nuevos de titularidad pública; **1 de enero de 2026** para los ajustes razonables en los existentes públicos. **Ambos plazos ya han vencido** |
| **Ley 11/2023** | Transposición de la Directiva (UE) 2019/882 (Acta Europea de Accesibilidad) | Título I aplicable desde el **28 de junio de 2025** |

  **Medidas concretas**, separando plataforma y sala:

  - *En la plataforma*: **subtitulado** en directo y **transcripción**; **texto en tiempo real** durante la sesión, que WebRTC soporta con la **`RFC 8865`** sobre canales de datos; **compatibilidad con lectores de pantalla**; **manejo completo por teclado**; y contraste y tamaño de texto ajustables. Base normativa: **capítulo 6 de la EN 301 549**, sobre comunicación bidireccional de voz y vídeo en tiempo real.
  - *En la sala física*: **bucle de inducción magnética** señalizado —que el propio RD 193/2023 exige instalar en las salas de los espacios escénicos de titularidad pública—; **posiciones reservadas** con visión directa de la pantalla y del intérprete de lengua de signos; **acceso sin barreras** y espacio de maniobra; y **iluminación frontal suficiente sobre quien interviene**, que **no es un lujo**: sin ella no funcionan ni la lectura labial ni la interpretación en lengua de signos. Es, además, la misma corrección que resuelve la queja 3.

  Se valora que se distinga **diseño para todas las personas** —preventivo, para todos y desde el origen— de **ajuste razonable** —correctivo, individual y con el límite de la carga desproporcionada—, conforme al **RDL 1/2013**.

  **Plan de mantenimiento** de las seis salas:

  - **Inventario de configuración** de cada sala: qué equipos, con qué versión de firmware y desde cuándo. Es la base de todo lo demás y el ENS lo exige como **`op.exp.1`, inventario de activos**, aplicable en las tres categorías.
  - **Preventivo por calendario**: limpieza de ópticas, revisión de conectores, actualización de firmware y **prueba completa de cada sala** con periodicidad fijada.
  - **Predictivo mediante monitorización remota**: consola que ve el estado de las seis salas y **detecta el fallo antes que el usuario**, que es la ganancia principal y no la económica.
  - **Correctivo** con encaje en la gestión de servicio (**ITIL 4** y **UNE-ISO/IEC 20000-1**): **incidencias** —restaurar el servicio, que aquí significa **que la reunión se pueda celebrar**, aunque sea con solución provisional—, **problemas** —si tres salas fallan por lo mismo, no son tres incidencias sino un problema— y **peticiones**.
  - **Acuerdos de nivel de servicio referidos al calendario de reuniones y no al reloj**: una sala averiada a las nueve menos cuarto con sesión a las nueve es una urgencia; la misma avería un viernes por la tarde, no.
  - **Comprobación previa protocolizada** antes de toda sesión con valor jurídico, según lo visto en el Caso 2.
  - **Encaje en el ENS**: los equipos de sala son **`mp.eq.4`, otros dispositivos conectados a la red**, cuyo texto nombra literalmente los «**dispositivos multimedia: proyectores, altavoces inteligentes**»; deben tener configuración de seguridad adecuada, capacidad de **eliminar la información almacenada** y, en categoría MEDIA, **refuerzo R1** de productos certificados. El local está sujeto a **`mp.if.3`, acondicionamiento de los locales** —temperatura y humedad, amenazas del análisis de riesgos y **protección del cableado**—, y la red audiovisual, a **`mp.com.4`**, que exige **segmento separado** y cuyo refuerzo R1 nombra las VLAN.

### Criterios de evaluación

| Cuestión | Puntos | Se valora |
|---|---|---|
| C1 | 3 | **No confundir reverberación, eco y acoplamiento** · asignar a cada queja su fenómeno y su corrección · la relación señal-ruido y el cuadrado de la distancia · señalar el **portátil en el centro de la mesa** como el peor montaje posible |
| C2 | 2 | Calcular el volumen (**478,8 m³**) y concluir que **excede los 350 m³**, por lo que procede **estudio específico** y no el valor de 0,7 s · conocer los tres valores del DB-HR · **500 lx, UGR ≤ 19, Uo ≥ 0,60 y Ra ≥ 80** a 0,85 m · las tres reglas propias de una sala de vídeo |
| C3 | 3 | Aplicar correctamente `IH = FV / (200 × %EH)` y obtener **2,375 m** · concluir que la pantalla **no cumple** y calcular la distancia máxima real (**3,72 m**) · comprobar el espectador más cercano y la restricción de 60° · ofrecer las **tres alternativas**, incluida la de **subir el %EH** |
| C4 | 2 | Las **tres normas de accesibilidad con sus plazos**, advirtiendo de que ya han vencido · separar medidas de plataforma y de sala · **bucle de inducción** e **iluminación frontal** como requisito, no como mejora · inventario, preventivo, predictivo y correctivo · **`op.exp.1`, `mp.eq.4`, `mp.if.3` y `mp.com.4`** · acuerdos de nivel de servicio **referidos al calendario de reuniones** |
