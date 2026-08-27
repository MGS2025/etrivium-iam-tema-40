# Tema 40 — Changelog

> **Título oficial**: Herramientas de trabajo en grupo. Sistemas de videoconferencia. Acondicionamiento de salas y equipos.

---

## v1.0 — 2026-08-27 — Primera versión

Generación completa del tema desde el esqueleto oficial `Test_Prompting/temas agosto/40.md`, siguiendo el patrón de la serie técnica (plantilla de referencia: **T37**). **Con este tema se cierra el temario oficial: T1 a T40 completo.**

### Alcance de la v1.0

| Entregable | Cantidad |
|---|---|
| Contenido teórico | 4 secciones · 13 epígrafes · 20 subepígrafes · **~20.400 palabras** |
| Diagramas SVG inline | **18** |
| Banco de test | **60 preguntas** A/B/C, balanceadas **20/20/20** |
| Casos prácticos | **3**, de 10 puntos cada uno |
| Fuentes | 38 Tier 1 · 13 Tier 2 · 3 Tier 3 |
| Pestañas del `index.html` | 8 (Inicio, Contenido, Índice, Diagramas, Test, Casos, Validación, Fuentes) |

### Decisiones de generación

1. **Estructura fiel al esqueleto en §1, §2 y §3, con una sección §4 añadida.** Los tres bloques `##` del esqueleto son las tres primeras secciones, sus diez `###` son los diez primeros epígrafes y sus veinte `####` son los veinte subepígrafes, **sin promover ni degradar ningún nivel**. Es el tercer tema de la serie que mapea sin ajuste, tras T34 y T37. La **§4, «Marco jurídico y aplicación en la Administración pública», no está en el esqueleto** y se ha añadido de forma expresa y declarada, por dos razones: en una convocatoria de Administración local, la pregunta sobre videoconferencia con más probabilidad de aparecer **no es técnica sino jurídica**, y **ningún otro tema del temario la cubre**; y porque las tres materias del enunciado convergen en una **sesión administrativa válida celebrada a distancia**. El punto 1.1 del documento de validación explica cómo redistribuir su contenido si el IAM prefiere no incorporarla.

2. **Las tres materias tratadas como tres capas del mismo problema, no como tres bloques inconexos.** Es la decisión editorial que da unidad al tema: el enunciado encadena un software, un sistema de comunicación y una obra civil, y lo que los une es que **describen el mismo objeto visto desde tres distancias**. De ahí el principio que ordena §3 y que se enuncia explícitamente: **la calidad percibida de una reunión a distancia la determina casi siempre la sala, no la red**.

3. **RFC verificados uno a uno contra el índice oficial del RFC Editor**, descargado el 27 de agosto de 2026. El método, ya rentable en T35 y T36, ha dado aquí **dos hallazgos de primer orden**: **la especificación vigente de SDP es la `RFC 8866`, de enero de 2021, que obsoletó la `RFC 4566`** —que es la que citan prácticamente todos los temarios del mercado—, y **JSEP es hoy la `RFC 9429`, de abril de 2024, que obsoletó la `RFC 8829`**, pieza del bloque WebRTC de 2021 que todo el mundo sigue citando como vigente.

4. **Dos normas de cifrado extremo a extremo incorporadas al tema y ausentes en el mercado.** **MLS** (`RFC 9420`, julio de 2023) para la mensajería de grupo y **SFrame** (`RFC 9605`, agosto de 2024) para el media en tiempo real. La segunda es la que resuelve el problema clásico de que una SFU siempre viera el contenido, y sin ella el tratamiento de la videoconferencia multipunto queda incompleto: permite explicar por qué una SFU **sí** puede ser extremo a extremo y una MCU **no**.

5. **La versión vigente de H.323 corregida.** Verificado en el sitio de la UIT que es la **versión 8, aprobada en marzo de 2022**, y no la 7 de 2009 que dan por buena las fuentes secundarias.

6. **La conexión más específica entre el ENS y el enunciado de un tema encontrada en toda la serie.** Extraído del PDF consolidado del BOE, **`mp.if.3` se titula literalmente «Acondicionamiento de los locales»** —que es la tercera materia del enunciado— y **`mp.eq.4` enumera nominalmente los «dispositivos multimedia: proyectores, altavoces inteligentes»**, que es exactamente el equipamiento de una sala de videoconferencia. Ninguna de las dos aparece en los materiales del mercado asociada a este tema. Se han convertido en el eje de §4.3 y del diagrama D18.

7. **Los dos regímenes de la sesión a distancia, contrapuestos.** Es el contenido jurídico diferencial. Verificados contra el BOE el **artículo 17 de la Ley 40/2015** —con sus cinco requisitos literales, el quórum a distancia del apartado 2, el sistema de conexión en la convocatoria del apartado 3 y el lugar de adopción del acuerdo del apartado 5— y el **artículo 46.3 de la LBRL**, introducido por el RDL 11/2020, **notablemente más restrictivo**: fuerza mayor, grave riesgo colectivo o catástrofe pública, miembros **en territorio español** y garantía del carácter público o secreto. Los materiales que tratan la videoconferencia en la Administración citan casi siempre solo el general, que es el que **no** se aplica a un Ayuntamiento. El Caso 2 está construido justamente para provocar ese error.

8. **DISCAS reproducido con sus fórmulas, no mencionado de pasada.** Extraídos del texto de la norma **ANSI/AVIXA V202.01** las dos categorías de necesidad visual (**decisión básica** y **decisión analítica**), los **factores de agudeza 200 y 3438** —con la explicación de que 3438 son los minutos de arco de un radián—, las fórmulas de altura de imagen y de distancia del espectador más lejano, y el cálculo del espectador más cercano con sus límites de **30°** y **60°**. El Caso 3 lo aplica íntegro sobre una sala real. **Es contenido que no está en ningún temario de oposición español.**

9. **Un dato declarado con su incertidumbre.** El listado oficial de normas publicadas de AVIXA indica la edición **V202.01:2026**, mientras que la ficha del producto sigue mostrando la **:2016**, que es la que se ha podido leer íntegra. Se ha optado por **declarar la vigente como :2026 y advertir de que la formulación reproducida es la de la :2016**, y por anotarlo como punto a reverificar antes de cada convocatoria en lugar de resolverlo por conjetura.

10. **Normativa de acondicionamiento y accesibilidad verificada contra fuente oficial.** Del PDF de `codigotecnico.org` proceden literalmente los **tres valores límite del tiempo de reverberación** del apartado 2.2 del **DB-HR** (0,7 s vacía · 0,5 s con butacas · 0,9 s en restaurantes) y el umbral de **350 m³**. Del PDF del BOE del **RD 193/2023** procede la **disposición final sexta** con sus cuatro fechas —**1 de enero de 2025, 2026, 2029 y 2030**— y la exigencia de **bucles de inducción magnética**. Del PDF del BOE del **TREBEP**, el **artículo 47 bis** sobre teletrabajo. Se declara expresamente en el punto 9.7 de la validación que **los valores de la UNE-EN 12464-1:2022 son la única cifra del tema que no procede del texto oficial**, por ser norma de pago.

11. **Sin fragmentos de código y sin nombres de producto.** Lo primero, por coherencia con T26, T28, T29, T30, T32, T33, T34 y T37: el enunciado no menciona ningún lenguaje. Lo segundo, porque **es el tema del temario que más rápido envejece si se escriben marcas**. Única excepción justificada: las **guías CCN-STIC de la serie 885**, que se citan por ser documentos oficiales españoles y porque su sola existencia —que exista una guía del CCN para configurar conforme al ENS una herramienta de trabajo en equipo— es en sí un dato examinable.

12. **Secuencia de letras del test fijada antes de redactar, y comprobada la cobertura por sección.** Aplicando la lección de T23 se definió de antemano la secuencia de las 60 respuestas correctas, con 20 de cada letra y sin tres iguales consecutivas; el recuento posterior por script coincidió **carácter a carácter** con la planificada, de modo que **no hizo falta ninguna corrección**. Y aplicando la lección de T36, se comprobó además el **reparto por sección**: 18 preguntas de §1, 22 de §2, 12 de §3 y 8 de §4, sin que ninguna quede por debajo de ocho.

13. **Reglas de SVG aplicadas desde el origen.** Atribución `[Fuente: …]` separada del borde y del último elemento dibujado; **ningún elemento mezcla `class` con el atributo `fill`** —se usa `style="fill:…"`, porque en la cascada CSS la clase gana al atributo, lección de T33 y T34—; **ninguna clase usada sin declarar**, comprobado por script sobre los 18 SVG, que detectó y corrigió una referencia a `.s3` en D3; y tildes revisadas también en mayúsculas y en los `aria-label`.

14. **El `build_t40.py` nace con los tres bugs del conversor ya corregidos**: el `inline()` admite negrita con cursiva anidada (T26 y T27), el manejador de blockquote convierte las tablas markdown embebidas en un callout mediante `bq_body()` (T34 y T35), y **el contenido se ha redactado sin ninguna tabla dentro de un callout**, que es la recomendación de fondo de esa lección.

### QA realizado

- **Validación XML de los 18 SVG antes de medir nada**, conforme a la lección del T32.
- **Integridad del test**: 60 preguntas, 3 opciones únicas por pregunta, coincidencia exacta entre el texto de la opción correcta y el de la solución, referencia presente en las 60. Distribución **20 A / 20 B / 20 C** y cobertura por sección comprobada.
- **Verificación aritmética** de los cuatro ejercicios resueltos del contenido y de los cálculos de los tres casos: flujos de la malla, ancho de banda con margen del 30 %, volumen del recinto frente al umbral de 350 m³ y las cuatro operaciones de DISCAS.
- **Render real** con Chrome headless y sonda `getBBox` sobre el `index.html` generado, forzando la clase activa en la pestaña de diagramas, con los **tres chequeos** de `_tools-qa/qa_svg.py`.
- **Revisión visual de las 18 capturas**, una a una.
- **Motor de test** probado sobre HTTP, no sobre `file://`.
- **Asteriscos crudos y tablas markdown sin convertir**: recuento en el `index.html` tras excluir `<script>`, `<svg>`, `<style>` y `<pre><code>`. Ambos dan **0**.
- **Ortografía** con hunspell `es_ES`, con revisión manual por el alto número de falsos positivos propios de un tema técnico.
