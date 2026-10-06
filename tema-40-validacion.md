# Tema 40 — Validación

> **Título oficial**: Herramientas de trabajo en grupo. Sistemas de videoconferencia. Acondicionamiento de salas y equipos.
>
> **Versión**: v1.0 — **Pendiente de validación por María, Ana y el IAM**
> **Fecha**: 2026-08-27

---

## 1. Cobertura del temario oficial

El enunciado oficial (BOAM 10.032, tema 40) enumera **tres materias**. Correspondencia con las secciones del contenido:

| Enunciado oficial | Sección | Estado |
|---|---|---|
| Herramientas de trabajo en grupo | §1 | ✅ Completo |
| Sistemas de videoconferencia | §2 | ✅ Completo |
| Acondicionamiento de salas y equipos | §3 | ✅ Completo |
| — Marco jurídico y aplicación en la Administración pública (**añadido**, no está en el enunciado ni en el esqueleto) | §4 | ✅ Completo · **se somete a validación** |

El **esqueleto de partida** se ha seguido **literalmente en §1, §2 y §3**: sus tres bloques de primer nivel son las tres primeras secciones, sus diez bloques de segundo nivel son los diez primeros epígrafes y sus veinte bloques de tercer nivel son los veinte subepígrafes, sin promover ni degradar ningún nivel. Es, con el T34 y el T37, el tercer tema de la serie cuyo esqueleto mapea sin ajuste a los tres niveles de numeración.

### 1.1. La sección §4 añadida: por qué, y qué pasa si se rechaza

Es la única desviación respecto del esqueleto y conviene explicarla y someterla expresamente a decisión.

**Por qué se ha añadido.** Por dos razones. La primera es de enfoque: en una convocatoria de una **Administración local**, la cuestión más relevante sobre videoconferencia **no es técnica sino jurídica** —cuándo puede un órgano colegiado municipal reunirse a distancia y qué hay que garantizar—, y **ningún otro tema del temario oficial la cubre**: el T39 trata el ENS y el ENI, y los T3 y T4 tratan la organización municipal, pero el régimen de las sesiones a distancia no aparece en ninguno. La segunda es de coherencia interna: las tres materias del enunciado convergen en un mismo punto, que es **una sesión administrativa válida celebrada a distancia**, y esa convergencia pedía una sección de cierre.

**Qué pasa si María, Ana o el IAM prefieren no incorporarla.** Su contenido se redistribuye sin pérdida: **§4.1** (sesiones a distancia) pasa a §2.4.1, **§4.2** (protección de datos y grabación) pasa a §1.3.1 y **§4.3** (adecuación al ENS) se reparte entre §1.3 y §3.2. La reestructuración es mecánica y no obliga a reescribir. **El diagrama D18 y las preguntas P53 a P60 del test seguirían siendo válidos** con la referencia de epígrafe actualizada.

## 2. Contenido teórico

- **4 secciones · 13 epígrafes · 20 subepígrafes** (numeración de tres niveles, `N.M.K`, coherente con el resto de la serie técnica).
- **~20.400 palabras** medidas con `wc -w`. Queda en la mitad alta de la serie, por detrás de T32 (≈25.000), T33 (≈24.500), T37 (≈23.000) y T34 (≈21.500), y por delante de T29 (≈21.200) y T30 (≈21.400). La extensión es proporcionada al enunciado: tres materias, una de ellas —el acondicionamiento— ajena a la informática y con normativa propia.
- **4 tipos de callout**: `[DATO CLAVE]`, `[EJERCICIO RESUELTO]`, `[EJEMPLO DE APLICACIÓN EN EL AYTO]` y `[RELACIÓN CON OTROS TEMAS]`.
- **Caso de referencia transversal**: el Ayuntamiento despliega una plataforma corporativa de trabajo en grupo y acondiciona el Salón de Sesiones de una Junta Municipal de Distrito más cinco salas de reunión. Atraviesa las cuatro secciones y enlaza con los tres casos prácticos.
- Cierre con un bloque de **«los diez datos que no se pueden fallar»**, no numerado, a modo de resumen memorístico de última hora.
- **Sin fragmentos de código.** Decisión deliberada, igual que en T26, T28, T29, T30, T32, T33, T34 y T37: el enunciado no menciona ningún lenguaje y lo memorizable son **numeraciones de RFC y de recomendaciones de la UIT, tasas binarias, umbrales de retardo, valores acústicos y lumínicos, fórmulas de dimensionamiento, plazos normativos y códigos del ENS**. Se han concentrado en tablas y en los diagramas D7, D8, D13, D14, D16, D17 y D18.
- **Sin nombres de producto**, con una excepción justificada: las **guías CCN-STIC de la serie 885**, que se citan porque son documentos oficiales españoles y porque su sola existencia es un dato examinable. Es el tema del temario en el que más tienta escribir marcas comerciales y el que más rápido envejece si se hace.

## 3. Fronteras con otros temas, declaradas de entrada

Este tema toca seis materias que el temario atribuye a otros temas. El reparto adoptado, explicitado en las «Convenciones» del propio contenido:

| Materia | Tema | Reparto adoptado |
|---|---|---|
| Paradigmas de computación distribuida y servicios en la nube (IaaS, PaaS, SaaS; nubes pública, privada e híbrida) | **T31** | Aquí solo como **decisión de despliegue** de una herramienta de trabajo en grupo, en unos párrafos de §1.1.1, no en una sección |
| Seguridad de los sistemas, criptografía y firma | **T32** | DTLS, SRTP, MLS y SFrame se citan **por lo que hacen**, no por cómo cifran |
| Comunicaciones, pila de protocolos y redes locales con su cableado | **T33, T34 y T37** | Aquí solo lo que el media en tiempo real exige de la red: **retardo, fluctuación, pérdida y marcado de prioridad** |
| Seguridad perimetral, acceso remoto y VPN | **T36** | Aquí solo la **travesía de NAT y de cortafuegos del media**, en §2.2.2 |
| Accesibilidad, diseño universal y usabilidad | **T25** | Aquí solo su aplicación a **una sala multimedia y a una plataforma de reunión**, en §3.3.1 |
| Principios del ENS y del ENI · gestión de incidencias | **T39 y T29** | Aquí, **las medidas concretas que recaen sobre este objeto** y el mantenimiento del parque de salas como caso particular de la gestión del servicio |

**Solapamiento residual asumido y por qué.** El punto de contacto más real es con el **T31**: el modelo de despliegue de una plataforma colaborativa es, por definición, una decisión de nube. Se ha resuelto **no explicando qué es SaaS** —eso es el T31— sino **qué implica elegirlo** para esta clase de servicio, con la frontera de responsabilidad y las medidas `op.nub.1` y `op.ext` como eje. Con el **T25** el solapamiento se concentra en los tres conceptos jurídicos de accesibilidad, que se han desarrollado aquí porque un opositor que estudie el T40 no puede quedarse sin saber qué es un ajuste razonable. **Se solicita al IAM que confirme este reparto**, en los mismos términos en que se pidió al generar el T30 y el T37.

## 4. Fuentes

- **Tier 1**: 38 referencias, organizadas en tres bloques (trabajo en grupo e identidad; videoconferencia; salas, accesibilidad y normativa española). Incluyen el bloque completo de RFC de WebRTC, las recomendaciones de la UIT-T de la familia H.3xx y de códecs, las normas ANSI/AVIXA, el CTE DB-HR, la UNE-EN 12464-1, la EN 301 549 y la normativa española de accesibilidad, órganos colegiados, ENS, ENI y protección de datos.
- **Tier 2**: 13 referencias (Ellis, Gibbs y Rein; Johansen; Shapiro y otros sobre CRDT; Tanenbaum y Kurose; guías CCN-STIC; Estrategia de nube híbrida; normas de medición acústica; criterios NC y NR; XMPP Standards Foundation; W3C; ITIL e ISO/IEC 20000-1).
- **Tier 3**: 3 referencias de contexto municipal.

### 4.1. Verificación contra fuente primaria, no de memoria

- **RFC**: descargado el **índice oficial del RFC Editor** (`https://www.rfc-editor.org/rfc-index.txt`) el 27 de agosto de 2026 y **grepeado uno a uno cada RFC citado**, comprobando fecha, estado y relaciones `Obsoletes` y `Obsoleted by`. Es el método que ya dio hallazgos en T35 y T36 y ha vuelto a darlos aquí (punto 4.2).
- **ENS**: extraído del **PDF consolidado del BOE** (`BOE-A-2022-7191`) con `pdftotext -layout`. De ahí proceden **literalmente** las medidas **`mp.if.1`, `mp.if.2`, `mp.if.3`** con sus tres requisitos, **`mp.eq.1`** con su refuerzo R1, **`mp.eq.4`** con su enumeración de dispositivos y sus dos refuerzos, **`mp.info.5`**, **`mp.s.1`** con sus siete requisitos y **`op.nub.1`** con sus cuatro exigencias, además de las tablas de aplicación por categoría de `op.ext`, `op.acc` y `op.exp`.
- **Ley 40/2015** (`BOE-A-2015-10566`): descargado el PDF del texto consolidado y extraído con `pdftotext -layout`. De ahí proceden literalmente los **apartados 1, 2, 3 y 5 del artículo 17**.
- **Ley 7/1985, LBRL** (`BOE-A-1985-5392`): igual procedimiento. De ahí procede literalmente el **artículo 46.3** completo, con sus dos párrafos.
- **TREBEP** (`BOE-A-2015-11719`): igual procedimiento. De ahí procede el **artículo 47 bis** con sus cinco apartados.
- **RD 193/2023** (`BOE-A-2023-7417`): igual procedimiento. De ahí procede la **disposición final sexta** con las cuatro fechas del calendario, y la exigencia de **bucles de inducción magnética** en los espacios escénicos de titularidad pública.
- **CTE, Documento Básico HR**: descargado el PDF oficial de `codigotecnico.org` y extraído con `pdftotext -layout`. De ahí proceden literalmente los **tres valores límite del apartado 2.2** y el umbral de **350 m³**.
- **ANSI/AVIXA V202.01 (DISCAS)**: extraídas del texto de la norma las **dos categorías de necesidad visual**, los **factores de agudeza 200 y 3438**, las **fórmulas de altura de imagen y de distancia del espectador más lejano** y el **cálculo del espectador más cercano** con sus límites de 30° y 60°. La **edición vigente** se ha verificado en el listado oficial de normas publicadas de AVIXA en agosto de 2026.
- **ITU-T H.323**: verificada en línea, en el propio sitio de la UIT, la **edición vigente y su fecha de aprobación**.

### 4.2. Seis datos que la verificación contra fuente primaria ha permitido afinar

Son la aportación diferencial de este tema frente a los temarios del mercado:

1. **La especificación vigente de SDP es la `RFC 8866`, de enero de 2021, que obsoletó la `RFC 4566`.** Prácticamente todos los materiales de oposición siguen citando la 4566. Verificado contra el índice del RFC Editor.
2. **JSEP es hoy la `RFC 9429`, de abril de 2024, que obsoletó la `RFC 8829`.** El bloque de WebRTC de enero de 2021 se cita como conjunto en todas partes sin advertir que una de sus piezas ya ha sido sustituida.
3. **La versión vigente de ITU-T H.323 es la 8, aprobada en marzo de 2022**, no la 7 de 2009 que citan casi todos los temarios.
4. **Existen dos normas de cifrado extremo a extremo para el trabajo colaborativo que ningún temario recoge**: **MLS** (`RFC 9420`, julio de 2023) para la mensajería de grupo y **SFrame** (`RFC 9605`, agosto de 2024) para el media en tiempo real. La segunda es la que resuelve el problema clásico de que una SFU siempre viera el contenido, y su ausencia deja cojo cualquier tratamiento de la videoconferencia multipunto.
5. **La medida `mp.eq.4` del ENS nombra literalmente los «dispositivos multimedia: proyectores, altavoces inteligentes»**, y **`mp.if.3` se titula «Acondicionamiento de los locales»**, que es literalmente la tercera materia del enunciado de este tema. Es la conexión más específica entre el ENS y el temario que se ha encontrado en toda la serie técnica, y no aparece en ningún material del mercado.
6. **El régimen de las sesiones a distancia de los órganos colegiados locales es el del artículo 46.3 de la LBRL, no el del artículo 17 de la Ley 40/2015**, y es **notablemente más restrictivo**: exige fuerza mayor, grave riesgo colectivo o catástrofe pública, y que los miembros se encuentren **en territorio español**. Los materiales que tratan la videoconferencia en la Administración citan casi siempre solo el régimen general, que es el que **no** se aplica a un Ayuntamiento.

### 4.3. Un dato que se declara con su incertidumbre

**La edición vigente de la norma DISCAS.** El **listado oficial de normas publicadas de AVIXA**, consultado en agosto de 2026 en dos páginas distintas del sitio, indica **ANSI/AVIXA V202.01:2026**; la ficha individual del producto, en cambio, sigue mostrando la edición **:2016**. Se ha optado por **declarar la edición vigente como :2026 y advertir de que la formulación reproducida procede del texto de la edición :2016**, que es la que se ha podido leer íntegra. **No se ha podido verificar si la revisión de 2026 modifica los factores de agudeza 200 y 3438 o las fórmulas.** Se anota como punto a revisar antes de cada convocatoria (punto 9.4).

## 5. Test (60 preguntas)

- **60 preguntas** de 3 opciones (A/B/C), formato oficial de la oposición, con penalización de **1/3** en el motor de corrección.
- **Distribución de la respuesta correcta: 20 A / 20 B / 20 C**, verificada por script. Aplicando la lección de T23, **la secuencia de las 60 letras se fijó antes de redactar una sola pregunta**, con 20 de cada una y sin tres letras iguales consecutivas, y se comprobó después que la secuencia obtenida coincidía **carácter a carácter** con la planificada. **No hizo falta ninguna corrección posterior.**
- **Cobertura por sección**, comprobada expresamente conforme a la lección del T36 —que el balanceo A/B/C no garantiza el reparto por materia—:

| Sección | Preguntas | Reparto A/B/C |
|---|---|---|
| §1 Herramientas de trabajo en grupo | **18** (P1-P18) | 6 A · 5 B · 7 C |
| §2 Sistemas de videoconferencia | **22** (P19-P40) | 7 A · 9 B · 6 C |
| §3 Acondicionamiento de salas y equipos | **12** (P41-P52) | 5 A · 3 B · 4 C |
| §4 Marco jurídico y aplicación en la Administración | **8** (P53-P60) | 2 A · 3 B · 3 C |

  Ninguna sección queda por debajo de 8 preguntas. El mayor peso de §2 es deliberado y defendible: es la materia con más contenido técnico cerrado.
- **Verificación automática**: 60 preguntas, 3 opciones únicas por pregunta, **coincidencia exacta entre el texto de la opción correcta y el de la solución** en las 60, y referencia a epígrafe y fuente en las 60.
- **Cinco preguntas de cálculo o de razonamiento cuantitativo** (P19 flujos de la malla, P20 cuello de botella de la subida, P44 volumen frente al umbral de 350 m³, P48 fórmula de DISCAS, P49 origen del factor 3438), pensadas para la parte práctica del examen.

## 6. Casos prácticos (3)

Los tres se sitúan en el Ayuntamiento de Madrid y comparten el supuesto de referencia del tema:

1. **Despliegue de la plataforma corporativa de trabajo en grupo** (§1): modelo de despliegue diferenciado por bloque de servicio con las medidas `op.nub.1` y `op.ext`, arquitectura de identidad con SAML, OpenID Connect y SCIM como respuesta a **1.400 cuentas huérfanas**, gobernanza frente a **3.000 carpetas compartidas sin caducidad**, política de conservación conciliando RGPD y archivo, y el riesgo de publicación de documentos colaborativos resuelto con `mp.info.5`.
2. **Sesión a distancia de una Junta Municipal de Distrito** (§2 y §4): descarte de la malla por cálculo (**702 flujos, 40 Mbit/s de subida**), arquitectura distinta por colectivo con la advertencia de que **retransmitir a 900 personas es difusión y no videoconferencia**, dimensionamiento del enlace con el **error de los ocho portátiles** deliberadamente sembrado en el enunciado, calidad de servicio, aplicación del **artículo 46.3 de la LBRL** frente al régimen general, y la caída de un miembro durante una votación tratada como **posible vicio de procedimiento**.
3. **Acondicionamiento del Salón de Sesiones y de las salas de reunión** (§3): diagnóstico de **cuatro quejas** que corresponden a cuatro fenómenos distintos —reverberación, eco, contraluz y tamaño de imagen—, aplicación del umbral de **350 m³** del DB-HR, **cálculo completo de DISCAS** con la conclusión de que la pantalla instalada solo cumple hasta 3,72 m de los 9,5 m reales, accesibilidad con sus tres normas y plazos vencidos, y plan de mantenimiento con su encaje en ITIL y en el ENS.

Cada caso suma **10 puntos** repartidos en cuatro cuestiones, con solución orientativa y tabla de criterios de evaluación.

## 7. Diagramas (18)

Los 18 diagramas son SVG inline, sin dependencias externas, con `role="img"` y `aria-label` descriptivo en español, y con las clases CSS sufijadas por número para evitar colisiones de estilo entre ellos.

**Los seis que hay que memorizar**, por orden de prioridad: **D7** (punto a punto, malla y servidor central, con las fórmulas y la tabla de crecimiento), **D8** (MCU frente a SFU fila a fila), **D12** (STUN, TURN e ICE con los tres tipos de candidato), **D14** (los cuatro umbrales de calidad y el marcado DSCP), **D16** (las cifras del DB-HR y de la UNE-EN 12464-1) y **D18** (los dos regímenes de la sesión a distancia y las medidas del ENS sobre la sala).

**Reglas de composición aplicadas desde el origen**, conforme a las lecciones acumuladas en la serie:

- Atribución `[Fuente: …]` a **12 px o más** del borde inferior del `viewBox` y a **12 px o más** del último elemento dibujado.
- **Ningún elemento mezcla `class` con el atributo de presentación `fill`**: cuando hace falta un color distinto del de la clase se usa `style="fill:…"`, porque en la cascada CSS **la clase gana al atributo**. Comprobado con `grep`: sin coincidencias.
- **Ninguna clase usada sin declarar**: comprobado por script sobre los 18 SVG.
- Revisión de **tildes también en mayúsculas** y en los `aria-label`, que es donde más se escapan.
- **Ninguna tabla markdown dentro de un callout** en el contenido, conforme a la lección de T34 y T35.

## 8. QA realizado

- **Validación XML de los 18 SVG antes de medir nada**, conforme a la lección del T32: un SVG mal formado pasa el recuento de elementos y el `getBBox` con un falso OK, porque el parser HTML es tolerante y el elemento roto mide `0×0`.
- **Render real** con Chrome headless y sonda `getBBox` sobre el `index.html` generado, forzando la clase activa en la pestaña de diagramas, con los **tres chequeos** de `_tools-qa/qa_svg.py`: desbordes del `viewBox`, colisiones entre textos y **texto solapado con un `<rect>` que no lo contiene**.
- **Revisión visual de las 18 capturas**, una a una, porque el QA programático no ve rótulos que no cuadran con lo que encabezan, flechas que apuntan a un hueco ni colores ilegibles por herencia de clase.
- **Integridad del test**: 60 preguntas, 3 opciones únicas por pregunta, coincidencia exacta entre el texto de la opción correcta y el de la solución, referencia presente en las 60. Distribución **20 A / 20 B / 20 C** y cobertura por sección comprobada.
- **Verificación aritmética de los ejercicios y de los casos**: los cálculos de flujos de la malla, de ancho de banda con margen, de volumen del recinto y de DISCAS se han recomprobado uno a uno.
- **Motor de test** probado sobre HTTP, no sobre `file://`, donde el `<script>` no se ejecuta en este entorno.
- **Asteriscos crudos y tablas markdown sin convertir**: recuento en el `index.html` tras excluir `<script>`, `<svg>`, `<style>` y `<pre><code>`. Ambos deben dar **0**.
- **Ortografía**: barrido con hunspell `es_ES`, con revisión manual por el alto número de falsos positivos propios de un tema técnico (nombres de norma, siglas inglesas, identificadores de medida del ENS).

## 9. Puntos que se someten a validación

1. **La sección §4 añadida.** Es la decisión de mayor calado del tema y la única desviación respecto del esqueleto. Se propone mantenerla por las razones del punto 1.1, y se indica cómo redistribuir su contenido si se prefiere no incorporarla.
2. **El reparto de fronteras con T31, T25, T32, T33, T34, T36, T37 y T39** descrito en el punto 3. Conviene fijarlo con el IAM, especialmente el solapamiento con el **T31** en materia de modelos de nube y con el **T25** en materia de accesibilidad.
3. **El nivel de detalle jurídico de §4.** Se ha desarrollado con amplitud porque es la parte diferencial y la que un examen de Administración local puede preguntar directamente. Si María o Ana consideran que un tema técnico no debe llevar tanta norma, la reducción natural es §4.2, dejando la protección de datos en el nivel de enumeración de deberes.
4. **La edición de la norma DISCAS**, según lo advertido en el punto 4.3. Debe reverificarse antes de cada convocatoria, y si se consigue el texto de la edición **:2026**, comprobar si los factores de agudeza **200** y **3438** siguen siendo los mismos.
5. **Los datos de actualidad de 2024 a 2026** —JSEP en la `RFC 9429`, SFrame en la `RFC 9605`, MLS en la `RFC 9420`, H.323 versión 8, la revisión **V4.1.1** de la EN 301 549 prevista para incorporar las WCAG 2.2—. Aportan valor frente a los temarios del mercado, pero **envejecen**: conviene revisarlos en cada convocatoria.
6. **La ausencia deliberada de nombres de producto.** Se somete a validación por si María o Ana consideran que, tratándose de un tema tan pegado a la práctica, conviene añadir un anexo con las plataformas de uso más extendido. La recomendación técnica es **no hacerlo en el cuerpo del tema**, porque es la parte que antes queda obsoleta, y en todo caso mantenerlo fuera del temario, en material de apoyo actualizable.
7. **La procedencia de los valores de la UNE-EN 12464-1:2022.** Es la única norma citada cuyos valores **no proceden del texto oficial**, por ser una norma de pago: se han tomado de reproducciones concordantes de su tabla para oficinas y salas de reuniones. Los cuatro valores —**500 lx, UGR ≤ 19, Uo ≥ 0,60 y Ra ≥ 80**— son ampliamente coincidentes entre fuentes, pero conviene contrastarlos con el ejemplar de la norma si el IAM dispone de él.
