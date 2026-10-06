# Tema 40 — Catálogo de Diagramas

> **Título oficial**: Herramientas de trabajo en grupo. Sistemas de videoconferencia. Acondicionamiento de salas y equipos.
>
> **Versión**: v1.0
> **Fecha**: 2026-08-27
> **Autor**: ETRIVIUM
> **Formato**: SVG inline (zero-dependencias, escalable, imprimible, accesible con role/aria-label)
> **Paleta**: Ayuntamiento de Madrid #0055a0 (primario) + #d13c3c (alertas) + #2d8659 (ventajas) + #e89822 (callouts)
> **Nota técnica**: las clases CSS de cada SVG llevan sufijo numérico único (`.t1`, `.h1`…) para evitar colisiones de estilos entre los 18 diagramas embebidos en la misma página. Ningún elemento mezcla `class` con el atributo `fill`: cuando hace falta un color distinto del de su clase se usa `style="fill:…"`, porque en la cascada CSS **la clase gana al atributo de presentación**.

---

## Índice de diagramas

| ID | Título | Sección | Tipo | Formato |
|---|---|---|---|---|
| D1 | Las 3C del trabajo en grupo y la matriz de Johansen | §1 | Modelo + matriz | 680×300 |
| D2 | Los tres modelos de despliegue y la frontera de responsabilidad | §1.1.1 | Comparativa de capas | 680×340 |
| D3 | Identidad federada: SAML, OpenID Connect y SCIM | §1.1.2 | Flujo + reparto de papeles | 680×340 |
| D4 | Canales síncronos y asíncronos: coste de interrupción | §1.2.1 | Eje comparativo | 680×328 |
| D5 | Edición concurrente: bloqueo, transformación operacional y CRDT | §1.2.2 | Comparativa de tres vías | 680×346 |
| D6 | El ciclo de vida de la información en el espacio colaborativo | §1.3 | Cadena de controles | 680×326 |
| D7 | Punto a punto, malla y servidor central: cuántos flujos | §2.1.1 | Topologías + cálculo | 680×352 |
| D8 | MCU frente a SFU: la comparación central | §2.1.2 | Tabla-esquema | 680×352 |
| D9 | H.323: los cuatro elementos y los protocolos internos | §2.2.1 | Arquitectura | 680×362 |
| D10 | SIP: el establecimiento de una llamada paso a paso | §2.2.1 | Diagrama de secuencia | 680×346 |
| D11 | La pila de WebRTC y el bloque de RFC de enero de 2021 | §2.2.2 | Pila de protocolos | 680×352 |
| D12 | Travesía de NAT: STUN pregunta, TURN carga, ICE decide | §2.2.2 | Escenario + candidatos | 680×378 |
| D13 | Códecs de audio y vídeo: tabla de decisión | §2.3.1 | Escala comparativa | 680×346 |
| D14 | Los cuatro parámetros de calidad y sus umbrales | §2.3.2 | Umbrales + marcado DSCP | 680×340 |
| D15 | Interoperabilidad: las cuatro vías, de la limpia a la sucia | §2.4.2 | Escala de degradación | 680×332 |
| D16 | Acondicionamiento de la sala: acústica y luz, con sus cotas | §3.1.1 | Corte de sala + valores | 680×366 |
| D17 | DISCAS: cómo se calcula el tamaño de la pantalla | §3.2.2 | Planta + fórmulas | 680×392 |
| D18 | Los dos regímenes de la sesión a distancia y el ENS de la sala | §4 | Comparativa jurídica | 680×384 |

---

## D1 · Las 3C del trabajo en grupo y la matriz de Johansen

**Sección**: §1 — Herramientas de trabajo en grupo
**Propósito**: Fijar de una sola vez los dos esquemas de clasificación del tema: las tres funciones del *groupware* y la matriz de dos ejes de Johansen, con ejemplos colocados en su celda.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Las tres funciones del trabajo en grupo (comunicación, coordinación y colaboración) y la matriz de Johansen, que clasifica el groupware según dos ejes, el tiempo y el lugar, en cuatro celdas: cara a cara, síncrono distribuido, asíncrono en el mismo lugar y asíncrono distribuido">
  <style>.h1{font:700 13px system-ui,sans-serif;fill:#0055a0}.k1{font:700 10px system-ui,sans-serif;fill:#0055a0}.d1{font:9px system-ui,sans-serif;fill:#333}.n1{font:8.5px system-ui,sans-serif;fill:#666}.w1{font:700 11px system-ui,sans-serif;fill:#fff}.g1{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h1">Las 3C del trabajo en grupo y la matriz de Johansen</text>
  <text x="340" y="35" text-anchor="middle" class="n1">Los dos esquemas de clasificación clave de toda la sección</text>

  <text x="24" y="53" class="k1">LAS TRES FUNCIONES (3C)</text>
  <rect x="22" y="60" width="272" height="42" rx="4" fill="#eef4fa"/>
  <rect x="22" y="60" width="30" height="42" rx="4" fill="#0055a0"/>
  <text x="37" y="86" text-anchor="middle" class="w1">C</text>
  <text x="60" y="76" class="k1">COMUNICACIÓN</text>
  <text x="60" y="90" class="d1">Intercambiar información. Unidad: el mensaje</text>

  <rect x="22" y="108" width="272" height="42" rx="4" fill="#fdf3e3"/>
  <rect x="22" y="108" width="30" height="42" rx="4" fill="#e89822"/>
  <text x="37" y="134" text-anchor="middle" class="w1">C</text>
  <text x="60" y="124" class="k1">COORDINACIÓN</text>
  <text x="60" y="138" class="d1">Quién hace qué y cuándo. Unidad: la tarea</text>

  <rect x="22" y="156" width="272" height="42" rx="4" fill="#e6f2ec"/>
  <rect x="22" y="156" width="30" height="42" rx="4" fill="#2d8659"/>
  <text x="37" y="182" text-anchor="middle" class="w1">C</text>
  <text x="60" y="172" class="k1">COLABORACIÓN</text>
  <text x="60" y="186" class="d1">Producir juntos. Unidad: el artefacto</text>

  <text x="318" y="53" class="k1">MATRIZ DE JOHANSEN (1988): TIEMPO × LUGAR</text>
  <rect x="316" y="60" width="86" height="20" rx="3" fill="#0055a0"/>
  <rect x="404" y="60" width="126" height="20" rx="3" fill="#0055a0"/>
  <text x="467" y="74" text-anchor="middle" class="w1">MISMO LUGAR</text>
  <rect x="532" y="60" width="126" height="20" rx="3" fill="#0055a0"/>
  <text x="595" y="74" text-anchor="middle" class="w1">DISTINTO LUGAR</text>

  <rect x="316" y="84" width="86" height="54" rx="3" fill="#0055a0"/>
  <text x="359" y="107" text-anchor="middle" class="w1">MISMO</text>
  <text x="359" y="121" text-anchor="middle" class="w1">TIEMPO</text>
  <rect x="404" y="84" width="126" height="54" rx="3" fill="#eef4fa"/>
  <text x="410" y="100" class="k1">Cara a cara</text>
  <text x="410" y="114" class="d1">Sala de reuniones</text>
  <text x="410" y="127" class="d1">Pizarra, mesa interactiva</text>
  <rect x="532" y="84" width="126" height="54" rx="3" fill="#e6f2ec"/>
  <text x="538" y="100" class="g1">Síncrono distribuido</text>
  <text x="538" y="114" class="d1">Videoconferencia, chat</text>
  <text x="538" y="127" class="d1">Edición simultánea</text>

  <rect x="316" y="142" width="86" height="54" rx="3" fill="#0055a0"/>
  <text x="359" y="165" text-anchor="middle" class="w1">DISTINTO</text>
  <text x="359" y="179" text-anchor="middle" class="w1">TIEMPO</text>
  <rect x="404" y="142" width="126" height="54" rx="3" fill="#eef4fa"/>
  <text x="410" y="158" class="k1">Asíncrono, mismo sitio</text>
  <text x="410" y="172" class="d1">Tablón de anuncios</text>
  <text x="410" y="185" class="d1">Turnos sobre un puesto</text>
  <rect x="532" y="142" width="126" height="54" rx="3" fill="#fdf3e3"/>
  <text x="538" y="158" class="k1">Asíncrono distribuido</text>
  <text x="538" y="172" class="d1">Correo, foro, wiki</text>
  <text x="538" y="185" class="d1">Repositorio, flujo trabajo</text>

  <rect x="22" y="212" width="636" height="52" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="230" text-anchor="middle" class="k1">CSCW es la DISCIPLINA (Grief y Cashman, 1984) · GROUPWARE es el PRODUCTO</text>
  <text x="340" y="245" text-anchor="middle" class="d1">El caso típico da una herramienta y pide su celda. El correo va abajo a la derecha; la videoconferencia, arriba a la derecha</text>
  <text x="340" y="258" text-anchor="middle" class="d1">Cuando una organización dice que la herramienta no funciona, lo que falla casi siempre es la COORDINACIÓN, no la comunicación</text>

  <text x="658" y="288" text-anchor="end" class="n1">[Fuente: Ellis, Gibbs y Rein (CACM, 1991) · Johansen (1988)]</text>
</svg>
```

---

## D2 · Los tres modelos de despliegue y la frontera de responsabilidad

**Sección**: §1.1.1 — Modelos de servicio en la nube, locales e híbridos
**Propósito**: Mostrar que lo que cambia entre modelos no es dónde está el servidor, sino **dónde cae la frontera de responsabilidad**, y anclar el precepto que extiende el ENS al proveedor.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Comparación de los tres modelos de despliegue de una herramienta de trabajo en grupo: local, híbrido y software como servicio, mostrando qué capas opera la organización y cuáles el proveedor, y las medidas del Esquema Nacional de Seguridad que aplican al proveedor">
  <style>.h2{font:700 13px system-ui,sans-serif;fill:#0055a0}.k2{font:700 10px system-ui,sans-serif;fill:#0055a0}.d2{font:9px system-ui,sans-serif;fill:#333}.n2{font:8.5px system-ui,sans-serif;fill:#666}.w2{font:700 9.5px system-ui,sans-serif;fill:#fff}.s2{font:8.5px system-ui,sans-serif;fill:#fff}.g2{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h2">Los tres modelos de despliegue: quién opera cada capa</text>
  <text x="340" y="35" text-anchor="middle" class="n2">Azul oscuro = lo opera la ORGANIZACIÓN · Gris = lo opera el PROVEEDOR</text>

  <text x="110" y="55" text-anchor="middle" class="k2">LOCAL (on-premise)</text>
  <text x="340" y="55" text-anchor="middle" class="k2">HÍBRIDO</text>
  <text x="570" y="55" text-anchor="middle" class="k2">SaaS (nube)</text>

  <rect x="22" y="62" width="176" height="22" fill="#0055a0"/><text x="110" y="77" text-anchor="middle" class="w2">Aplicación</text>
  <rect x="22" y="86" width="176" height="22" fill="#0055a0"/><text x="110" y="101" text-anchor="middle" class="w2">Datos y usuarios</text>
  <rect x="22" y="110" width="176" height="22" fill="#0055a0"/><text x="110" y="125" text-anchor="middle" class="w2">Sistema operativo</text>
  <rect x="22" y="134" width="176" height="22" fill="#0055a0"/><text x="110" y="149" text-anchor="middle" class="w2">Servidor y red</text>
  <rect x="22" y="158" width="176" height="22" fill="#0055a0"/><text x="110" y="173" text-anchor="middle" class="w2">Centro de datos</text>

  <rect x="252" y="62" width="176" height="22" fill="#0055a0"/><text x="340" y="77" text-anchor="middle" class="w2">Aplicación (mixta)</text>
  <rect x="252" y="86" width="176" height="22" fill="#0055a0"/><text x="340" y="101" text-anchor="middle" class="w2">Datos y usuarios</text>
  <rect x="252" y="110" width="176" height="22" fill="#0055a0"/><text x="340" y="125" text-anchor="middle" class="w2">Identidad (interna)</text>
  <rect x="252" y="134" width="176" height="22" fill="#8a949e"/><text x="340" y="149" text-anchor="middle" class="w2">Servidor y red</text>
  <rect x="252" y="158" width="176" height="22" fill="#8a949e"/><text x="340" y="173" text-anchor="middle" class="w2">Centro de datos</text>

  <rect x="482" y="62" width="176" height="22" fill="#8a949e"/><text x="570" y="77" text-anchor="middle" class="w2">Aplicación</text>
  <rect x="482" y="86" width="176" height="22" fill="#0055a0"/><text x="570" y="101" text-anchor="middle" class="w2">Datos y usuarios</text>
  <rect x="482" y="110" width="176" height="22" fill="#8a949e"/><text x="570" y="125" text-anchor="middle" class="w2">Sistema operativo</text>
  <rect x="482" y="134" width="176" height="22" fill="#8a949e"/><text x="570" y="149" text-anchor="middle" class="w2">Servidor y red</text>
  <rect x="482" y="158" width="176" height="22" fill="#8a949e"/><text x="570" y="173" text-anchor="middle" class="w2">Centro de datos</text>

  <rect x="22" y="192" width="636" height="34" rx="4" fill="#e6f2ec"/>
  <text x="32" y="207" class="g2">RESPONSABILIDAD COMPARTIDA — la frase que hay que saber decir</text>
  <text x="32" y="220" class="d2">El proveedor responde de la seguridad DEL servicio; la organización, de la seguridad EN el servicio: cuentas, permisos y compartición</text>

  <rect x="22" y="234" width="636" height="48" rx="4" fill="#fdf3e3"/>
  <text x="32" y="249" class="k2">EL ENS NO SE QUEDA EN LA PUERTA DEL AYUNTAMIENTO — art. 2.3 del RD 311/2022</text>
  <text x="32" y="262" class="d2">op.nub.1 Protección de servicios en la nube: aplica en las TRES categorías (+R1 en MEDIA, +R1+R2 en ALTA). Sus cuatro exigencias:</text>
  <text x="32" y="275" class="d2">pruebas de penetración · transparencia · cifrado y gestión de claves · JURISDICCIÓN DE LOS DATOS · op.ext.1-4: NO aplican en BÁSICA</text>

  <text x="340" y="300" text-anchor="middle" class="k2">El principio español no es «nube primero» sino «NUBE HÍBRIDA PRIMERO» (Estrategia de nube híbrida de las AAPP, 2022)</text>

  <text x="658" y="328" text-anchor="end" class="n2">[Fuente: RD 311/2022, anexo II · Estrategia de nube híbrida de las AAPP]</text>
</svg>
```

---

## D3 · Identidad federada: SAML, OpenID Connect y SCIM

**Sección**: §1.1.2 — Gestión de identidades y control de acceso federado
**Propósito**: Separar sin ambigüedad los tres protocolos por su función —autenticar, autorizar y aprovisionar— y mostrar que la credencial nunca llega al proveedor de servicio.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Esquema de la federación de identidad: el usuario se autentica ante el proveedor de identidad de su organización, que emite un aserto firmado al proveedor de servicio; la contraseña nunca llega a la plataforma. Se comparan SAML 2.0, OpenID Connect sobre OAuth 2.0 y SCIM 2.0 por su función">
  <style>.h3{font:700 13px system-ui,sans-serif;fill:#0055a0}.k3{font:700 10px system-ui,sans-serif;fill:#0055a0}.d3{font:9px system-ui,sans-serif;fill:#333}.n3{font:8.5px system-ui,sans-serif;fill:#666}.w3{font:700 10px system-ui,sans-serif;fill:#fff}.r3{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g3{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h3">Identidad federada: quién autentica, quién autoriza y quién aprovisiona</text>

  <rect x="30" y="40" width="150" height="46" rx="5" fill="#0055a0"/>
  <text x="105" y="60" text-anchor="middle" class="w3">USUARIO</text>
  <text x="105" y="76" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">Empleado municipal</text>

  <rect x="265" y="40" width="150" height="46" rx="5" fill="#0055a0"/>
  <text x="340" y="60" text-anchor="middle" class="w3">PROVEEDOR DE IDENTIDAD</text>
  <text x="340" y="76" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">Directorio del Ayuntamiento</text>

  <rect x="500" y="40" width="150" height="46" rx="5" fill="#2d8659"/>
  <text x="575" y="60" text-anchor="middle" class="w3">PROVEEDOR DE SERVICIO</text>
  <text x="575" y="76" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">Plataforma colaborativa</text>

  <line x1="180" y1="56" x2="258" y2="56" stroke="#0055a0" stroke-width="1.6" marker-end="url(#a3)"/>
  <text x="219" y="51" text-anchor="middle" class="n3">1. Credencial</text>
  <line x1="415" y1="70" x2="493" y2="70" stroke="#2d8659" stroke-width="1.6" marker-end="url(#a3b)"/>
  <text x="454" y="63" text-anchor="middle" class="g3">2. Aserto</text>
  <defs>
    <marker id="a3" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker>
    <marker id="a3b" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#2d8659"/></marker>
  </defs>

  <rect x="22" y="98" width="636" height="24" rx="4" fill="#fbe9e9"/>
  <text x="340" y="114" text-anchor="middle" class="r3">LA CONTRASEÑA NUNCA LLEGA AL PROVEEDOR DE SERVICIO — solo llega una afirmación firmada por el proveedor de identidad</text>

  <rect x="22" y="134" width="206" height="90" rx="4" fill="#eef4fa"/>
  <rect x="22" y="134" width="206" height="20" rx="4" fill="#0055a0"/>
  <text x="125" y="148" text-anchor="middle" class="w3">SAML 2.0 — AUTENTICA</text>
  <text x="32" y="170" class="d3">OASIS, marzo de 2005. XML</text>
  <text x="32" y="184" class="d3">Unidad: el ASERTO (autenticación,</text>
  <text x="32" y="197" class="d3">atributo, decisión de autorización)</text>
  <text x="32" y="210" class="d3">Perfil de navegador con POST</text>
  <text x="32" y="220" class="n3">El clásico de la federación en las AAPP</text>

  <rect x="237" y="134" width="206" height="90" rx="4" fill="#eef4fa"/>
  <rect x="237" y="134" width="206" height="20" rx="4" fill="#0055a0"/>
  <text x="340" y="148" text-anchor="middle" class="w3">OAuth 2.0 + OIDC</text>
  <text x="247" y="170" class="d3">OAuth 2.0 = RFC 6749: AUTORIZA</text>
  <text x="247" y="184" class="d3">OpenID Connect = capa encima:</text>
  <text x="247" y="197" class="d3">AUTENTICA, con testigo de identidad</text>
  <text x="247" y="210" class="d3">en formato JWT (RFC 7519)</text>
  <text x="247" y="220" class="n3">OAuth por sí solo NO autentica</text>

  <rect x="452" y="134" width="206" height="90" rx="4" fill="#e6f2ec"/>
  <rect x="452" y="134" width="206" height="20" rx="4" fill="#2d8659"/>
  <text x="555" y="148" text-anchor="middle" class="w3">SCIM 2.0 — APROVISIONA</text>
  <text x="462" y="170" class="d3">RFC 7643 esquema · RFC 7644</text>
  <text x="462" y="184" class="d3">protocolo (API REST sobre JSON)</text>
  <text x="462" y="197" class="d3">Crea, modifica y BORRA cuentas</text>
  <text x="462" y="210" class="d3">Alta y baja propagadas solas</text>
  <text x="462" y="220" class="n3">Sin él nacen las cuentas huérfanas</text>

  <rect x="22" y="238" width="636" height="46" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="256" text-anchor="middle" class="k3">LA FRASE QUE HAY QUE LLEVAR MEMORIZADA</text>
  <text x="340" y="272" text-anchor="middle" class="k3">«OAuth 2.0 AUTORIZA · OpenID Connect AUTENTICA · SCIM APROVISIONA»</text>

  <text x="340" y="300" text-anchor="middle" class="d3">El ENS lo exige en op.acc.5 (usuarios externos) y op.acc.6 (usuarios de la organización), que empujan hacia el segundo factor en MEDIA y ALTA</text>

  <text x="658" y="328" text-anchor="end" class="n3">[Fuente: OASIS SAML 2.0 · RFC 6749 · RFC 7519 · RFC 7643 y 7644]</text>
</svg>
```

---

## D4 · Canales síncronos y asíncronos: coste de interrupción

**Sección**: §1.2.1 — Comunicación e intercambio de información síncrono y asíncrono
**Propósito**: Ordenar los canales por el turno que imponen al receptor, que es el criterio que de verdad decide la gobernanza de una plataforma, y colgar de cada uno su protocolo normalizado.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 328" role="img" aria-label="Los canales de comunicación de una plataforma de trabajo en grupo ordenados por el coste de interrupción que imponen al receptor, desde el repositorio documental y el correo, que son asíncronos, hasta la videoconferencia y la llamada, que son síncronos, con el protocolo normalizado de cada uno">
  <style>.h4{font:700 13px system-ui,sans-serif;fill:#0055a0}.k4{font:700 10px system-ui,sans-serif;fill:#0055a0}.d4{font:9px system-ui,sans-serif;fill:#333}.n4{font:8.5px system-ui,sans-serif;fill:#666}.w4{font:700 10px system-ui,sans-serif;fill:#fff}.r4{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}</style>
  <text x="340" y="19" text-anchor="middle" class="h4">Los canales, ordenados por el turno que imponen al receptor</text>
  <text x="340" y="35" text-anchor="middle" class="n4">La gobernanza de una plataforma consiste en decidir qué se comunica por cada uno. Convertirlo todo en síncrono es el error clásico</text>

  <rect x="22" y="48" width="636" height="16" rx="8" fill="#eef4fa"/>
  <rect x="22" y="48" width="212" height="16" rx="8" fill="#2d8659"/>
  <rect x="446" y="48" width="212" height="16" rx="8" fill="#d13c3c"/>
  <text x="128" y="60" text-anchor="middle" class="w4">ASÍNCRONO</text>
  <text x="340" y="60" text-anchor="middle" class="k4">INTERMEDIO</text>
  <text x="552" y="60" text-anchor="middle" class="w4">SÍNCRONO</text>
  <text x="22" y="78" class="n4">Coste de interrupción BAJO: el receptor decide cuándo atiende</text>
  <text x="658" y="78" text-anchor="end" class="n4">Coste de interrupción ALTO: turno inmediato</text>

  <rect x="22" y="88" width="152" height="76" rx="4" fill="#e6f2ec"/>
  <text x="98" y="105" text-anchor="middle" class="k4">REPOSITORIO Y WIKI</text>
  <text x="30" y="121" class="d4">Conocimiento duradero</text>
  <text x="30" y="134" class="d4">Historial de versiones</text>
  <text x="30" y="147" class="d4">WebDAV, RFC 4918</text>
  <text x="30" y="159" class="n4">Distinto tiempo, distinto lugar</text>

  <rect x="184" y="88" width="152" height="76" rx="4" fill="#e6f2ec"/>
  <text x="260" y="105" text-anchor="middle" class="k4">CORREO ELECTRÓNICO</text>
  <text x="192" y="121" class="d4">El único canal interoperable</text>
  <text x="192" y="134" class="d4">entre organizaciones distintas</text>
  <text x="192" y="147" class="d4">SMTP 5321 · IMAP4rev2 9051</text>
  <text x="192" y="159" class="n4">Y la mayor superficie de ataque</text>

  <rect x="346" y="88" width="152" height="76" rx="4" fill="#fdf3e3"/>
  <text x="422" y="105" text-anchor="middle" class="k4">MENSAJERÍA Y PRESENCIA</text>
  <text x="354" y="121" class="d4">Cuasi síncrono: se espera</text>
  <text x="354" y="134" class="d4">respuesta pronto, no ya</text>
  <text x="354" y="147" class="d4">XMPP 6120 y 6121 · PIDF 3863</text>
  <text x="354" y="159" class="n4">La presencia es dato laboral</text>

  <rect x="508" y="88" width="150" height="76" rx="4" fill="#fbe9e9"/>
  <text x="583" y="105" text-anchor="middle" class="k4">VIDEOCONFERENCIA</text>
  <text x="516" y="121" class="d4">Exige presencia simultánea</text>
  <text x="516" y="134" class="d4">de todas las partes</text>
  <text x="516" y="147" class="d4">SIP 3261 · RTP 3550 · WebRTC</text>
  <text x="516" y="159" class="n4">Es toda la sección 2 del tema</text>

  <rect x="22" y="180" width="636" height="42" rx="4" fill="#eef4fa"/>
  <text x="32" y="196" class="k4">LA SEÑALIZACIÓN MODERNA VIAJA POR WEBSOCKET (RFC 6455), NO POR HTTP CONVENCIONAL</text>
  <text x="32" y="211" class="d4">Canal bidireccional y persistente, abierto promoviendo una conexión HTTP. Sostiene el «alguien está escribiendo» y la señalización</text>

  <rect x="22" y="232" width="636" height="58" rx="5" fill="none" stroke="#d13c3c" stroke-width="1.5"/>
  <text x="340" y="249" text-anchor="middle" class="r4">DOS TRAMPAS COMUNES</text>
  <text x="340" y="266" text-anchor="middle" class="d4">XMPP NO es un protocolo de videoconferencia: su señalización multimedia es la extensión Jingle (XEP-0166)</text>
  <text x="340" y="281" text-anchor="middle" class="d4">Y la presencia publicada es un dato sobre la actividad del empleado: arts. 87 y 88 de la LOPDGDD</text>

  <text x="658" y="316" text-anchor="end" class="n4">[Fuente: RFC 6120, 6121, 6455, 9051 · LO 3/2018]</text>
</svg>
```

---

## D5 · Edición concurrente: bloqueo, transformación operacional y CRDT

**Sección**: §1.2.2 — Gestión documental y edición concurrente
**Propósito**: Contraponer las tres únicas familias de solución al problema de la actualización perdida, con su coste y con la pista que las delata en un enunciado.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 346" role="img" aria-label="Las tres familias de solución a la edición concurrente de documentos: bloqueo pesimista, transformación operacional con servidor central y tipos de datos replicados sin conflictos o CRDT, comparadas por simultaneidad, necesidad de servidor central y soporte de trabajo sin conexión">
  <style>.h5{font:700 13px system-ui,sans-serif;fill:#0055a0}.k5{font:700 10px system-ui,sans-serif;fill:#0055a0}.d5{font:9px system-ui,sans-serif;fill:#333}.n5{font:8.5px system-ui,sans-serif;fill:#666}.w5{font:700 10px system-ui,sans-serif;fill:#fff}.r5{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g5{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h5">Edición concurrente: las tres únicas familias de solución</text>

  <rect x="22" y="30" width="636" height="26" rx="4" fill="#fbe9e9"/>
  <text x="340" y="47" text-anchor="middle" class="r5">EL PROBLEMA: LA ACTUALIZACIÓN PERDIDA — dos personas abren el mismo documento y gana quien guarda la última</text>

  <rect x="22" y="66" width="206" height="150" rx="4" fill="#eef4fa"/>
  <rect x="22" y="66" width="206" height="22" rx="4" fill="#0055a0"/>
  <text x="125" y="82" text-anchor="middle" class="w5">1 · BLOQUEO (pesimista)</text>
  <text x="32" y="104" class="d5">Quien abre RESERVA el documento</text>
  <text x="32" y="117" class="d5">y nadie más escribe hasta que</text>
  <text x="32" y="130" class="d5">lo devuelve. Método LOCK de</text>
  <text x="32" y="143" class="d5">WebDAV (RFC 4918)</text>
  <text x="32" y="163" class="g5">+ Cero conflictos posibles</text>
  <text x="32" y="176" class="g5">+ Simple de auditar</text>
  <text x="32" y="192" class="r5">− CERO SIMULTANEIDAD</text>
  <text x="32" y="205" class="r5">− Bloqueo huérfano</text>

  <rect x="237" y="66" width="206" height="150" rx="4" fill="#fdf3e3"/>
  <rect x="237" y="66" width="206" height="22" rx="4" fill="#e89822"/>
  <text x="340" y="82" text-anchor="middle" class="w5">2 · TRANSFORMACIÓN OPERACIONAL</text>
  <text x="247" y="104" class="d5">No se transmite el documento:</text>
  <text x="247" y="117" class="d5">se transmiten OPERACIONES, que</text>
  <text x="247" y="130" class="d5">se transforman una contra otra</text>
  <text x="247" y="143" class="d5">para converger (Ellis y Gibbs)</text>
  <text x="247" y="163" class="g5">+ Simultaneidad real</text>
  <text x="247" y="176" class="g5">+ Carácter a carácter</text>
  <text x="247" y="192" class="r5">− NECESITA SERVIDOR CENTRAL</text>
  <text x="247" y="205" class="r5">− Difícil de implementar bien</text>

  <rect x="452" y="66" width="206" height="150" rx="4" fill="#e6f2ec"/>
  <rect x="452" y="66" width="206" height="22" rx="4" fill="#2d8659"/>
  <text x="555" y="82" text-anchor="middle" class="w5">3 · CRDT (sin conflictos)</text>
  <text x="462" y="104" class="d5">Las estructuras se diseñan para</text>
  <text x="462" y="117" class="d5">que las operaciones CONMUTEN:</text>
  <text x="462" y="130" class="d5">da igual el orden de llegada</text>
  <text x="462" y="143" class="d5">Los hay de estado y de operación</text>
  <text x="462" y="163" class="g5">+ NO NECESITA SERVIDOR CENTRAL</text>
  <text x="462" y="176" class="g5">+ Base del modo SIN CONEXIÓN</text>
  <text x="462" y="192" class="r5">− Coste en metadatos</text>
  <text x="462" y="205" class="n5">Shapiro y otros, INRIA, 2011</text>

  <rect x="22" y="230" width="636" height="46" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="248" text-anchor="middle" class="k5">LA PISTA QUE DELATA LA RESPUESTA EN UN ENUNCIADO</text>
  <text x="340" y="265" text-anchor="middle" class="d5">Si el enunciado menciona MODO SIN CONEXIÓN o SINCRONIZACIÓN ENTRE VARIOS DISPOSITIVOS del mismo usuario, la respuesta es CRDT</text>

  <rect x="22" y="286" width="636" height="34" rx="4" fill="#fdf3e3"/>
  <text x="32" y="301" class="k5">Y LO QUE NO RESUELVE NINGUNA DE LAS TRES: SACAR EL DOCUMENTO FUERA</text>
  <text x="32" y="314" class="d5">Antes de publicar hay que congelar la versión, exportarla al formato del ENI y LIMPIARLA de metadatos y comentarios — es mp.info.5</text>

  <text x="658" y="336" text-anchor="end" class="n5">[Fuente: Ellis, Gibbs y Rein (1991) · Shapiro y otros (2011) · RFC 4918 · RD 311/2022]</text>
</svg>
```

---

## D6 · El ciclo de vida de la información en el espacio colaborativo

**Sección**: §1.3 — Seguridad y gobernanza del espacio de trabajo
**Propósito**: Seguir el dato desde que nace hasta que se destruye y colgar de cada tramo el control y la medida del ENS que le corresponden, incluida la más olvidada de todas.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 326" role="img" aria-label="El ciclo de vida de la información en un espacio de trabajo compartido, en cinco tramos: clasificación, protección, control de la compartición, conservación y destrucción, con la medida del Esquema Nacional de Seguridad aplicable a cada tramo">
  <style>.h6{font:700 13px system-ui,sans-serif;fill:#0055a0}.k6{font:700 10px system-ui,sans-serif;fill:#0055a0}.d6{font:9px system-ui,sans-serif;fill:#333}.n6{font:8.5px system-ui,sans-serif;fill:#666}.w6{font:700 9.5px system-ui,sans-serif;fill:#fff}.r6{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.c6{font:700 9px system-ui,sans-serif;fill:#e89822}</style>
  <text x="340" y="19" text-anchor="middle" class="h6">El ciclo de vida del dato, y el control que toca en cada tramo</text>

  <rect x="22" y="34" width="120" height="58" rx="4" fill="#0055a0"/>
  <text x="82" y="52" text-anchor="middle" class="w6">1 · CLASIFICAR</text>
  <text x="82" y="68" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">Etiquetas: pública,</text>
  <text x="82" y="80" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">interna, confidencial</text>

  <rect x="152" y="34" width="120" height="58" rx="4" fill="#0055a0"/>
  <text x="212" y="52" text-anchor="middle" class="w6">2 · PROTEGER</text>
  <text x="212" y="68" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">Cifrado en tránsito</text>
  <text x="212" y="80" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">y en reposo</text>

  <rect x="282" y="34" width="120" height="58" rx="4" fill="#e89822"/>
  <text x="342" y="52" text-anchor="middle" class="w6">3 · COMPARTIR</text>
  <text x="342" y="68" text-anchor="middle" style="fill:#fff3e0;font:8.5px system-ui,sans-serif">DLP, invitados con</text>
  <text x="342" y="80" text-anchor="middle" style="fill:#fff3e0;font:8.5px system-ui,sans-serif">caducidad</text>

  <rect x="412" y="34" width="120" height="58" rx="4" fill="#0055a0"/>
  <text x="472" y="52" text-anchor="middle" class="w6">4 · CONSERVAR</text>
  <text x="472" y="68" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">Retención por tipo</text>
  <text x="472" y="80" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">de contenido</text>

  <rect x="542" y="34" width="116" height="58" rx="4" fill="#2d8659"/>
  <text x="600" y="52" text-anchor="middle" class="w6">5 · DESTRUIR</text>
  <text x="600" y="68" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">Borrado automático</text>
  <text x="600" y="80" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">con retención legal</text>

  <text x="82" y="108" text-anchor="middle" class="c6">mp.info.2</text>
  <text x="212" y="108" text-anchor="middle" class="c6">mp.com.2 y 3</text>
  <text x="342" y="108" text-anchor="middle" class="c6">op.acc.4 · mp.s.1</text>
  <text x="472" y="108" text-anchor="middle" class="c6">RGPD art. 5.1.e)</text>
  <text x="600" y="108" text-anchor="middle" class="c6">mp.si.5</text>

  <rect x="22" y="122" width="636" height="52" rx="4" fill="#fbe9e9"/>
  <text x="32" y="139" class="r6">LA MEDIDA MÁS OLVIDADA DEL ENS: mp.info.5, LIMPIEZA DE DOCUMENTOS</text>
  <text x="32" y="153" class="d6">«Se retirará toda la información adicional contenida en CAMPOS OCULTOS, METADATOS, COMENTARIOS O REVISIONES ANTERIORES,</text>
  <text x="32" y="166" class="d6">salvo cuando sea pertinente para el receptor». Confidencialidad. APLICA EN LOS TRES NIVELES, incluido el BAJO</text>

  <rect x="22" y="186" width="312" height="72" rx="4" fill="#eef4fa"/>
  <text x="32" y="202" class="k6">LAS DOS FUERZAS QUE TIRAN EN SENTIDO CONTRARIO</text>
  <text x="32" y="217" class="d6">El RGPD empuja a BORRAR: minimización (art. 5.1.c) y</text>
  <text x="32" y="230" class="d6">limitación del plazo (art. 5.1.e)</text>
  <text x="32" y="243" class="d6">El archivo y la prueba empujan a CONSERVAR</text>
  <text x="32" y="254" class="n6">Se concilian con retención diferenciada por tipo</text>

  <rect x="346" y="186" width="312" height="72" rx="4" fill="#e6f2ec"/>
  <text x="356" y="202" class="k6">EL REPARTO RAZONABLE EN UNA PLATAFORMA</text>
  <text x="356" y="217" class="d6">Mensajería: retención CORTA</text>
  <text x="356" y="230" class="d6">Correo: retención MEDIA</text>
  <text x="356" y="243" class="d6">Documento de expediente: la que fije el archivo</text>
  <text x="356" y="254" class="n6">Grabación de reunión: la MÁS CORTA de todas</text>

  <rect x="22" y="270" width="636" height="34" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="286" text-anchor="middle" class="k6">EL MAYOR VECTOR DE FUGA NO ES EL MALICIOSO: ES EL ACCIDENTAL</text>
  <text x="340" y="299" text-anchor="middle" class="d6">El enlace de compartición demasiado abierto y el adjunto al destinatario equivocado causan más incidentes que cualquier ataque</text>

  <text x="658" y="318" text-anchor="end" class="n6">[Fuente: RD 311/2022, anexo II · Reglamento (UE) 2016/679]</text>
</svg>
```

---

## D7 · Punto a punto, malla y servidor central: cuántos flujos

**Sección**: §2.1.1 — Modelos de comunicación punto a punto y multipunto
**Propósito**: Es el diagrama de cálculo del tema. Fija las fórmulas de la malla y muestra por qué el cuello de botella es la subida y no la bajada.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="Comparación del número de flujos en tres topologías de videoconferencia: punto a punto entre dos participantes, malla completa entre cinco participantes con veinte flujos, y servidor central con una sola conexión por participante; con la tabla de crecimiento del ancho de banda de subida según el número de participantes">
  <style>.h7{font:700 13px system-ui,sans-serif;fill:#0055a0}.k7{font:700 10px system-ui,sans-serif;fill:#0055a0}.d7{font:9px system-ui,sans-serif;fill:#333}.n7{font:8.5px system-ui,sans-serif;fill:#666}.w7{font:700 9px system-ui,sans-serif;fill:#fff}.r7{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g7{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h7">Cuántos flujos genera una reunión, según la topología</text>

  <text x="105" y="42" text-anchor="middle" class="k7">PUNTO A PUNTO (N = 2)</text>
  <circle cx="55" cy="88" r="17" fill="#0055a0"/><text x="55" y="92" text-anchor="middle" class="w7">A</text>
  <circle cx="155" cy="88" r="17" fill="#0055a0"/><text x="155" y="92" text-anchor="middle" class="w7">B</text>
  <line x1="72" y1="88" x2="138" y2="88" stroke="#2d8659" stroke-width="2"/>
  <text x="105" y="122" text-anchor="middle" class="g7">2 flujos. Retardo mínimo</text>
  <text x="105" y="135" text-anchor="middle" class="d7">Extremo a extremo trivial</text>

  <text x="340" y="42" text-anchor="middle" class="k7">MALLA COMPLETA (N = 5)</text>
  <g stroke="#d13c3c" stroke-width="0.9" opacity="0.75">
    <line x1="340" y1="62" x2="399" y2="105"/><line x1="340" y1="62" x2="377" y2="146"/>
    <line x1="340" y1="62" x2="303" y2="146"/><line x1="340" y1="62" x2="281" y2="105"/>
    <line x1="399" y1="105" x2="377" y2="146"/><line x1="399" y1="105" x2="303" y2="146"/>
    <line x1="399" y1="105" x2="281" y2="105"/><line x1="377" y1="146" x2="303" y2="146"/>
    <line x1="377" y1="146" x2="281" y2="105"/><line x1="303" y1="146" x2="281" y2="105"/>
  </g>
  <circle cx="340" cy="62" r="14" fill="#d13c3c"/><text x="340" y="66" text-anchor="middle" class="w7">A</text>
  <circle cx="399" cy="105" r="14" fill="#d13c3c"/><text x="399" y="109" text-anchor="middle" class="w7">B</text>
  <circle cx="377" cy="146" r="14" fill="#d13c3c"/><text x="377" y="150" text-anchor="middle" class="w7">C</text>
  <circle cx="303" cy="146" r="14" fill="#d13c3c"/><text x="303" y="150" text-anchor="middle" class="w7">D</text>
  <circle cx="281" cy="105" r="14" fill="#d13c3c"/><text x="281" y="109" text-anchor="middle" class="w7">E</text>
  <text x="340" y="180" text-anchor="middle" class="r7">5 × 4 = 20 flujos</text>

  <text x="575" y="42" text-anchor="middle" class="k7">SERVIDOR CENTRAL (N = 5)</text>
  <rect x="551" y="92" width="48" height="26" rx="4" fill="#2d8659"/>
  <text x="575" y="109" text-anchor="middle" class="w7">MCU/SFU</text>
  <circle cx="575" cy="62" r="12" fill="#0055a0"/>
  <circle cx="630" cy="90" r="12" fill="#0055a0"/>
  <circle cx="618" cy="140" r="12" fill="#0055a0"/>
  <circle cx="532" cy="140" r="12" fill="#0055a0"/>
  <circle cx="520" cy="90" r="12" fill="#0055a0"/>
  <g stroke="#2d8659" stroke-width="1.6">
    <line x1="575" y1="74" x2="575" y2="92"/><line x1="618" y1="94" x2="599" y2="99"/>
    <line x1="606" y1="136" x2="592" y2="118"/><line x1="544" y1="136" x2="558" y2="118"/>
    <line x1="532" y1="94" x2="551" y2="99"/>
  </g>
  <text x="575" y="180" text-anchor="middle" class="g7">1 conexión por participante</text>

  <rect x="22" y="196" width="636" height="46" rx="4" fill="#eef4fa"/>
  <text x="32" y="212" class="k7">LAS FÓRMULAS QUE HAY QUE SABER</text>
  <text x="32" y="227" class="d7">Malla: CADA participante sostiene N−1 subidas y N−1 bajadas · EL SISTEMA, N × (N−1) flujos · Crecimiento CUADRÁTICO en el sistema</text>
  <text x="32" y="238" class="n7">Con servidor central: cada participante sube 1 flujo. Baja 1 si el servidor MEZCLA (MCU) y hasta N−1 si REENVÍA (SFU)</text>

  <rect x="22" y="252" width="636" height="22" rx="3" fill="#0055a0"/>
  <text x="70" y="267" text-anchor="middle" class="w7">Participantes</text>
  <text x="200" y="267" text-anchor="middle" class="w7">Flujos del sistema en malla</text>
  <text x="380" y="267" text-anchor="middle" class="w7">Subida por participante (720p a 1,54 Mbit/s)</text>
  <text x="570" y="267" text-anchor="middle" class="w7">Viabilidad</text>

  <rect x="22" y="276" width="636" height="18" fill="#f5f8fb"/>
  <text x="70" y="289" text-anchor="middle" class="d7">4</text><text x="200" y="289" text-anchor="middle" class="d7">12</text>
  <text x="380" y="289" text-anchor="middle" class="d7">4,6 Mbit/s</text><text x="570" y="289" text-anchor="middle" class="g7">Viable</text>

  <rect x="22" y="294" width="636" height="18" fill="#fff"/>
  <text x="70" y="307" text-anchor="middle" class="d7">6</text><text x="200" y="307" text-anchor="middle" class="d7">30</text>
  <text x="380" y="307" text-anchor="middle" class="d7">7,7 Mbit/s</text><text x="570" y="307" text-anchor="middle" class="d7">En el límite</text>

  <rect x="22" y="312" width="636" height="18" fill="#fbe9e9"/>
  <text x="70" y="325" text-anchor="middle" class="d7">10</text><text x="200" y="325" text-anchor="middle" class="d7">90</text>
  <text x="380" y="325" text-anchor="middle" class="d7">13,9 Mbit/s</text><text x="570" y="325" text-anchor="middle" class="r7">Inviable: manda la SUBIDA</text>

  <text x="658" y="346" text-anchor="end" class="n7">[Fuente: RFC 7667, RTP Topologies · elaboración propia]</text>
</svg>
```

---

## D8 · MCU frente a SFU: la comparación central

**Sección**: §2.1.2 — Infraestructura central de conmutación: MCU y SFU
**Propósito**: Fijar la comparación fila a fila, incluida la consecuencia que casi nunca se explica: la MCU impide el cifrado extremo a extremo y la SFU lo permite mediante SFrame.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="Comparación entre la unidad de control multipunto (MCU), que decodifica, mezcla y vuelve a codificar, y la unidad de reenvío selectivo (SFU), que reenvía los flujos sin decodificarlos, en siete criterios: bajada, cómputo del servidor, retardo, composición, cifrado extremo a extremo, exigencia al cliente y uso típico">
  <style>.h8{font:700 13px system-ui,sans-serif;fill:#0055a0}.k8{font:700 10px system-ui,sans-serif;fill:#0055a0}.d8{font:9px system-ui,sans-serif;fill:#333}.n8{font:8.5px system-ui,sans-serif;fill:#666}.w8{font:700 10px system-ui,sans-serif;fill:#fff}.r8{font:700 9px system-ui,sans-serif;fill:#d13c3c}.g8{font:700 9px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h8">MCU frente a SFU: la comparación central de la sección 2</text>

  <rect x="22" y="32" width="312" height="66" rx="4" fill="#fdf3e3"/>
  <rect x="22" y="32" width="312" height="22" rx="4" fill="#e89822"/>
  <text x="178" y="48" text-anchor="middle" class="w8">MCU — MEZCLA Y TRANSCODIFICA</text>
  <text x="32" y="70" class="d8">Decodifica todos los flujos, los compone en UNA imagen</text>
  <text x="32" y="83" class="d8">y la vuelve a codificar. En la RFC 7667 es un MEZCLADOR</text>
  <text x="32" y="94" class="n8">En H.323 se descompone en MC (control) y MP (procesado)</text>

  <rect x="346" y="32" width="312" height="66" rx="4" fill="#e6f2ec"/>
  <rect x="346" y="32" width="312" height="22" rx="4" fill="#2d8659"/>
  <text x="502" y="48" text-anchor="middle" class="w8">SFU — REENVÍA SIN DECODIFICAR</text>
  <text x="356" y="70" class="d8">No decodifica nada: reenvía los flujos tal cual, eligiendo</text>
  <text x="356" y="83" class="d8">cuáles y con qué calidad. Es un REENVIADOR SELECTIVO</text>
  <text x="356" y="94" class="n8">Es la arquitectura DOMINANTE en las plataformas actuales</text>

  <rect x="22" y="108" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="122" y="122" text-anchor="middle" class="w8">Criterio</text>
  <text x="340" y="122" text-anchor="middle" class="w8">MCU</text>
  <text x="560" y="122" text-anchor="middle" class="w8">SFU</text>

  <rect x="22" y="130" width="636" height="18" fill="#f5f8fb"/>
  <text x="30" y="143" class="d8">Bajada por participante</text>
  <text x="340" y="143" text-anchor="middle" class="d8">1 flujo, siempre igual</text>
  <text x="560" y="143" text-anchor="middle" class="d8">Hasta N−1 flujos</text>

  <rect x="22" y="148" width="636" height="18" fill="#fff"/>
  <text x="30" y="161" class="d8">Cómputo en el servidor</text>
  <text x="340" y="161" text-anchor="middle" class="r8">MUY ALTO (transcodifica)</text>
  <text x="560" y="161" text-anchor="middle" class="g8">MUY BAJO (solo mueve paquetes)</text>

  <rect x="22" y="166" width="636" height="18" fill="#f5f8fb"/>
  <text x="30" y="179" class="d8">Retardo añadido</text>
  <text x="340" y="179" text-anchor="middle" class="r8">Sí: decodificar y recodificar</text>
  <text x="560" y="179" text-anchor="middle" class="g8">Mínimo</text>

  <rect x="22" y="184" width="636" height="18" fill="#fff"/>
  <text x="30" y="197" class="d8">Composición de la vista</text>
  <text x="340" y="197" text-anchor="middle" class="d8">Única, la decide el servidor</text>
  <text x="560" y="197" text-anchor="middle" class="d8">Libre en cada cliente</text>

  <rect x="22" y="202" width="636" height="18" fill="#f5f8fb"/>
  <text x="30" y="215" class="d8">Cifrado extremo a extremo</text>
  <text x="340" y="215" text-anchor="middle" class="r8">IMPOSIBLE: para mezclar hay que descifrar</text>
  <text x="560" y="215" text-anchor="middle" class="g8">POSIBLE con SFrame (RFC 9605)</text>

  <rect x="22" y="220" width="636" height="18" fill="#fff"/>
  <text x="30" y="233" class="d8">Exigencia al terminal</text>
  <text x="340" y="233" text-anchor="middle" class="g8">Mínima: sirve un equipo antiguo</text>
  <text x="560" y="233" text-anchor="middle" class="r8">Alta: decodifica y compone</text>

  <rect x="22" y="238" width="636" height="18" fill="#f5f8fb"/>
  <text x="30" y="251" class="d8">Uso típico</text>
  <text x="340" y="251" text-anchor="middle" class="d8">Salas heredadas, interoperación</text>
  <text x="560" y="251" text-anchor="middle" class="d8">Reunión moderna en la nube</text>

  <rect x="22" y="266" width="312" height="58" rx="4" fill="#eef4fa"/>
  <text x="32" y="282" class="k8">LAS DOS TÉCNICAS QUE HACEN VIABLE LA SFU</text>
  <text x="32" y="296" class="d8">SIMULCAST (RFC 8853): cada emisor sube VARIAS calidades</text>
  <text x="32" y="308" class="d8">a la vez y la SFU elige la que conviene a cada receptor</text>
  <text x="32" y="320" class="d8">SVC: un flujo en CAPAS; la SFU descarta capas</text>

  <rect x="346" y="266" width="312" height="58" rx="4" fill="#e6f2ec"/>
  <text x="356" y="282" class="k8">EL CIFRADO DE GRUPO, NORMALIZADO EN 2023 Y 2024</text>
  <text x="356" y="296" class="d8">SFrame (RFC 9605, agosto de 2024): cifra el FOTOGRAMA,</text>
  <text x="356" y="308" class="d8">no el paquete; la SFU encamina pero no descifra</text>
  <text x="356" y="320" class="d8">MLS (RFC 9420, julio de 2023): lo mismo para mensajería</text>

  <text x="658" y="344" text-anchor="end" class="n8">[Fuente: RFC 7667 · RFC 8853 · RFC 9605 · RFC 9420]</text>
</svg>
```

---

## D9 · H.323: los cuatro elementos y los protocolos internos

**Sección**: §2.2.1 — Protocolos de señalización H.323 y SIP
**Propósito**: Fijar la arquitectura de H.323 con la nomenclatura exacta y su versión vigente, que casi ningún temario recoge bien.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 362" role="img" aria-label="Arquitectura de H.323 con sus cuatro elementos: terminal, pasarela, controlador de acceso y unidad de control multipunto, y los protocolos internos H.225.0 de señalización, H.245 de control, H.235 de seguridad, H.239 de segundo flujo de vídeo y la serie H.460 de travesía de cortafuegos">
  <style>.h9{font:700 13px system-ui,sans-serif;fill:#0055a0}.k9{font:700 10px system-ui,sans-serif;fill:#0055a0}.d9{font:9px system-ui,sans-serif;fill:#333}.n9{font:8.5px system-ui,sans-serif;fill:#666}.w9{font:700 10px system-ui,sans-serif;fill:#fff}.s9{font:8.5px system-ui,sans-serif;fill:#dce8f4}.g9{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h9">H.323: los cuatro elementos de la arquitectura</text>
  <text x="340" y="35" text-anchor="middle" class="n9">UIT-T · Versión vigente: la 8, aprobada en MARZO DE 2022 (no la 7 de 2009 que citan casi todos los temarios)</text>

  <rect x="22" y="48" width="150" height="70" rx="5" fill="#0055a0"/>
  <text x="97" y="66" text-anchor="middle" class="w9">TERMINAL</text>
  <text x="97" y="83" text-anchor="middle" class="s9">El punto final</text>
  <text x="97" y="96" text-anchor="middle" class="s9">AUDIO obligatorio</text>
  <text x="97" y="109" text-anchor="middle" class="s9">Vídeo y datos, opcionales</text>

  <rect x="184" y="48" width="150" height="70" rx="5" fill="#0055a0"/>
  <text x="259" y="66" text-anchor="middle" class="w9">PASARELA (gateway)</text>
  <text x="259" y="83" text-anchor="middle" class="s9">Traduce a otras redes:</text>
  <text x="259" y="96" text-anchor="middle" class="s9">RDSI (H.320), telefonía,</text>
  <text x="259" y="109" text-anchor="middle" class="s9">SIP</text>

  <rect x="346" y="48" width="150" height="70" rx="5" fill="#e89822"/>
  <text x="421" y="66" text-anchor="middle" class="w9">CONTROLADOR DE ACCESO</text>
  <text x="421" y="83" text-anchor="middle" style="fill:#fff3e0;font:8.5px system-ui,sans-serif">OPCIONAL pero decisivo</text>
  <text x="421" y="96" text-anchor="middle" style="fill:#fff3e0;font:8.5px system-ui,sans-serif">Traduce direcciones, admite</text>
  <text x="421" y="109" text-anchor="middle" style="fill:#fff3e0;font:8.5px system-ui,sans-serif">llamadas y gestiona la ZONA</text>

  <rect x="508" y="48" width="150" height="70" rx="5" fill="#2d8659"/>
  <text x="583" y="66" text-anchor="middle" class="w9">MCU</text>
  <text x="583" y="83" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">Unidad de control</text>
  <text x="583" y="96" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">multipunto, compuesta de</text>
  <text x="583" y="109" text-anchor="middle" style="fill:#dff0e8;font:8.5px system-ui,sans-serif">MC (control) + MP (proceso)</text>

  <text x="24" y="140" class="k9">LOS PROTOCOLOS DE LA FAMILIA — lo que hace cada uno</text>

  <rect x="22" y="148" width="312" height="22" rx="3" fill="#eef4fa"/>
  <text x="30" y="163" class="d9"><tspan class="k9">H.225.0</tspan>  ·  RAS y señalización de llamada</text>
  <rect x="22" y="174" width="312" height="22" rx="3" fill="#eef4fa"/>
  <text x="30" y="189" class="d9"><tspan class="k9">H.245</tspan>  ·  Control, capacidades y canales lógicos</text>
  <rect x="22" y="200" width="312" height="22" rx="3" fill="#eef4fa"/>
  <text x="30" y="215" class="d9"><tspan class="k9">H.235</tspan>  ·  Seguridad y cifrado</text>

  <rect x="346" y="148" width="312" height="22" rx="3" fill="#fdf3e3"/>
  <text x="354" y="163" class="d9"><tspan class="k9">H.239</tspan>  ·  SEGUNDO FLUJO de vídeo (dual stream)</text>
  <rect x="346" y="174" width="312" height="22" rx="3" fill="#eef4fa"/>
  <text x="354" y="189" class="d9"><tspan class="k9">H.450.x</tspan>  ·  Servicios suplementarios</text>
  <rect x="346" y="200" width="312" height="22" rx="3" fill="#eef4fa"/>
  <text x="354" y="215" class="d9"><tspan class="k9">H.460.18/.19</tspan>  ·  Travesía de NAT y cortafuegos</text>

  <rect x="22" y="234" width="636" height="40" rx="4" fill="#fdf3e3"/>
  <text x="32" y="250" class="k9">H.239, EL DATO DE H.323 MÁS RELEVANTE DESPUÉS DE LOS CUATRO ELEMENTOS</text>
  <text x="32" y="265" class="d9">Es el mecanismo del SEGUNDO FLUJO DE VÍDEO: permite ver a la vez a la persona que habla y la presentación que comparte</text>

  <rect x="22" y="284" width="636" height="44" rx="5" fill="none" stroke="#0055a0" stroke-width="1.5"/>
  <text x="340" y="301" text-anchor="middle" class="k9">CODIFICACIÓN BINARIA ASN.1 CON REGLAS EMPAQUETADAS (PER)</text>
  <text x="340" y="317" text-anchor="middle" class="d9">Compacto y eficiente, y difícil de depurar — es la diferencia con SIP, que es texto. Y H.323 NO transporta el media: eso lo hace RTP</text>

  <text x="658" y="354" text-anchor="end" class="n9">[Fuente: UIT-T H.323 (03/2022), H.225.0, H.245, H.239]</text>
</svg>
```

---

## D10 · SIP: el establecimiento de una llamada paso a paso

**Sección**: §2.2.1 — Protocolos de señalización H.323 y SIP
**Propósito**: Mostrar la secuencia canónica de SIP y, sobre todo, el hecho que más se falla: el media no pasa por el servidor apoderado.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 346" role="img" aria-label="Diagrama de secuencia del establecimiento de una llamada SIP entre dos agentes de usuario a través de un servidor apoderado, con los mensajes INVITE, 100 Trying, 180 Ringing, 200 OK y ACK, y el flujo RTP que va directamente entre los extremos sin pasar por el servidor">
  <style>.h10{font:700 13px system-ui,sans-serif;fill:#0055a0}.k10{font:700 10px system-ui,sans-serif;fill:#0055a0}.d10{font:9px system-ui,sans-serif;fill:#333}.n10{font:8.5px system-ui,sans-serif;fill:#666}.w10{font:700 9.5px system-ui,sans-serif;fill:#fff}.m10{font:700 9px system-ui,sans-serif;fill:#0055a0}.g10{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h10">SIP: establecimiento de una llamada (RFC 3261, IETF, julio de 2002)</text>

  <rect x="40" y="32" width="120" height="24" rx="4" fill="#0055a0"/>
  <text x="100" y="48" text-anchor="middle" class="w10">AGENTE A (llama)</text>
  <rect x="280" y="32" width="120" height="24" rx="4" fill="#e89822"/>
  <text x="340" y="48" text-anchor="middle" class="w10">APODERADO (proxy)</text>
  <rect x="520" y="32" width="120" height="24" rx="4" fill="#0055a0"/>
  <text x="580" y="48" text-anchor="middle" class="w10">AGENTE B (recibe)</text>

  <line x1="100" y1="60" x2="100" y2="250" stroke="#c8d4de" stroke-width="1.4" stroke-dasharray="4,3"/>
  <line x1="340" y1="60" x2="340" y2="250" stroke="#c8d4de" stroke-width="1.4" stroke-dasharray="4,3"/>
  <line x1="580" y1="60" x2="580" y2="250" stroke="#c8d4de" stroke-width="1.4" stroke-dasharray="4,3"/>

  <line x1="100" y1="78" x2="334" y2="78" stroke="#0055a0" stroke-width="1.5" marker-end="url(#a10)"/>
  <text x="215" y="73" text-anchor="middle" class="m10">INVITE (lleva la OFERTA SDP)</text>
  <line x1="340" y1="94" x2="574" y2="94" stroke="#0055a0" stroke-width="1.5" marker-end="url(#a10)"/>
  <text x="458" y="89" text-anchor="middle" class="m10">INVITE</text>
  <line x1="334" y1="112" x2="106" y2="112" stroke="#8a949e" stroke-width="1.3" marker-end="url(#a10g)"/>
  <text x="220" y="107" text-anchor="middle" class="n10">100 Trying (provisional, 1xx)</text>
  <line x1="574" y1="130" x2="346" y2="130" stroke="#8a949e" stroke-width="1.3" marker-end="url(#a10g)"/>
  <text x="460" y="125" text-anchor="middle" class="n10">180 Ringing</text>
  <line x1="334" y1="148" x2="106" y2="148" stroke="#8a949e" stroke-width="1.3" marker-end="url(#a10g)"/>
  <text x="220" y="143" text-anchor="middle" class="n10">180 Ringing</text>
  <line x1="574" y1="166" x2="346" y2="166" stroke="#2d8659" stroke-width="1.6" marker-end="url(#a10v)"/>
  <text x="460" y="161" text-anchor="middle" class="g10">200 OK (lleva la RESPUESTA SDP)</text>
  <line x1="334" y1="184" x2="106" y2="184" stroke="#2d8659" stroke-width="1.6" marker-end="url(#a10v)"/>
  <text x="220" y="179" text-anchor="middle" class="g10">200 OK</text>
  <line x1="100" y1="202" x2="574" y2="202" stroke="#0055a0" stroke-width="1.5" marker-end="url(#a10)"/>
  <text x="340" y="197" text-anchor="middle" class="m10">ACK</text>

  <rect x="108" y="216" width="464" height="26" rx="13" fill="#2d8659"/>
  <text x="340" y="233" text-anchor="middle" class="w10">MEDIA POR RTP — DIRECTAMENTE ENTRE LOS EXTREMOS, SIN PASAR POR EL APODERADO</text>

  <defs>
    <marker id="a10" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#0055a0"/></marker>
    <marker id="a10g" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#8a949e"/></marker>
    <marker id="a10v" markerWidth="8" markerHeight="8" refX="7" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 z" fill="#2d8659"/></marker>
  </defs>

  <rect x="22" y="256" width="312" height="52" rx="4" fill="#eef4fa"/>
  <text x="32" y="272" class="k10">MÉTODOS Y ENTIDADES</text>
  <text x="32" y="286" class="d10">INVITE · ACK · BYE · CANCEL · REGISTER · OPTIONS</text>
  <text x="32" y="299" class="d10">Agente de usuario · apoderado · redirección · registrador</text>

  <rect x="346" y="256" width="312" height="52" rx="4" fill="#fdf3e3"/>
  <text x="356" y="272" class="k10">SDP NO NEGOCIA NADA: ES UN FORMATO</text>
  <text x="356" y="286" class="d10">Vigente: RFC 8866 (enero 2021), que OBSOLETÓ la RFC 4566</text>
  <text x="356" y="299" class="d10">Lo negocia el modelo oferta/respuesta de la RFC 3264</text>

  <text x="658" y="336" text-anchor="end" class="n10">[Fuente: RFC 3261 · RFC 8866 · RFC 3264 · RFC 3550]</text>
</svg>
```

---

## D11 · La pila de WebRTC y el bloque de RFC de enero de 2021

**Sección**: §2.2.2 — El estándar WebRTC y la comunicación en tiempo real
**Propósito**: Presentar la pila completa por capas y el mapa de RFC, señalando el hueco deliberado —la señalización— y la actualización de JSEP que ningún temario recoge.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 352" role="img" aria-label="La pila de protocolos de WebRTC por capas: interfaz de JavaScript del W3C, medios y datos, SRTP y SCTP, DTLS, ICE con STUN y TURN, y UDP; con el mapa de las RFC publicadas en bloque en enero de 2021 y la advertencia de que WebRTC no define la señalización y de que el cifrado es obligatorio">
  <style>.h11{font:700 13px system-ui,sans-serif;fill:#0055a0}.k11{font:700 10px system-ui,sans-serif;fill:#0055a0}.d11{font:9px system-ui,sans-serif;fill:#333}.n11{font:8.5px system-ui,sans-serif;fill:#666}.w11{font:700 10px system-ui,sans-serif;fill:#fff}.r11{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.c11{font:700 8.5px system-ui,sans-serif;fill:#e89822}</style>
  <text x="340" y="19" text-anchor="middle" class="h11">WebRTC: la pila y el bloque de RFC de enero de 2021</text>
  <text x="340" y="35" text-anchor="middle" class="n11">W3C define la interfaz de JavaScript · IETF define los protocolos que van por debajo</text>

  <rect x="22" y="46" width="320" height="24" rx="3" fill="#0055a0"/>
  <text x="182" y="62" text-anchor="middle" class="w11">API del W3C: RTCPeerConnection · getUserMedia</text>
  <rect x="22" y="74" width="156" height="24" rx="3" fill="#2d8659"/>
  <text x="100" y="90" text-anchor="middle" class="w11">MEDIA (audio y vídeo)</text>
  <rect x="186" y="74" width="156" height="24" rx="3" fill="#e89822"/>
  <text x="264" y="90" text-anchor="middle" class="w11">CANALES DE DATOS</text>
  <rect x="22" y="102" width="156" height="24" rx="3" fill="#2d8659"/>
  <text x="100" y="118" text-anchor="middle" class="w11">SRTP (RFC 3711)</text>
  <rect x="186" y="102" width="156" height="24" rx="3" fill="#e89822"/>
  <text x="264" y="118" text-anchor="middle" class="w11">SCTP</text>
  <rect x="22" y="130" width="320" height="24" rx="3" fill="#0055a0"/>
  <text x="182" y="146" text-anchor="middle" class="w11">DTLS — negocia las claves (DTLS-SRTP, RFC 5764)</text>
  <rect x="22" y="158" width="320" height="24" rx="3" fill="#0055a0"/>
  <text x="182" y="174" text-anchor="middle" class="w11">ICE (8445) con STUN (8489) y TURN (8656)</text>
  <rect x="22" y="186" width="320" height="24" rx="3" fill="#8a949e"/>
  <text x="182" y="202" text-anchor="middle" class="w11">UDP (y TCP como último recurso)</text>

  <rect x="354" y="46" width="304" height="164" rx="4" fill="#eef4fa"/>
  <text x="364" y="62" class="k11">EL MAPA DE RFC — casi todo, enero de 2021</text>
  <text x="364" y="78" class="d11">8825  Visión general del conjunto</text>
  <text x="364" y="91" class="d11">8826 / 8827  Seguridad y su arquitectura</text>
  <text x="364" y="104" class="d11">8834 / 8835  Uso de RTP · Transportes</text>
  <text x="364" y="117" class="d11">8831 / 8832  Canales de datos y su establecimiento</text>
  <text x="364" y="130" class="d11">8830  Identificación de flujos (msid)</text>
  <text x="364" y="143" class="d11">8836  Requisitos de control de congestión</text>
  <text x="364" y="156" class="d11">8837  MARCADO DSCP para calidad de servicio</text>
  <text x="364" y="169" class="d11">8853 / 8858 / 8864  Simulcast · Multiplexación · Datos en SDP</text>
  <text x="364" y="182" class="d11">8865  TEXTO EN TIEMPO REAL (T.140): accesibilidad</text>
  <text x="364" y="199" class="c11">8829  JSEP → HOY SUSTITUIDA POR LA RFC 9429 (abril de 2024)</text>

  <rect x="22" y="222" width="312" height="66" rx="4" fill="#fbe9e9"/>
  <text x="32" y="238" class="r11">1 · NO DEFINE LA SEÑALIZACIÓN — es deliberado</text>
  <text x="32" y="252" class="d11">Cómo se avisa al otro extremo lo resuelve la aplicación,</text>
  <text x="32" y="265" class="d11">normalmente por WebSocket. Lo que sí normaliza es QUÉ se</text>

  <rect x="346" y="222" width="312" height="66" rx="4" fill="#e6f2ec"/>
  <text x="356" y="238" class="k11">2 · EL CIFRADO ES OBLIGATORIO, NO OPCIONAL</text>
  <text x="356" y="252" class="d11">No hay WebRTC sin cifrar: media por SRTP con claves</text>
  <text x="356" y="265" class="d11">negociadas por DTLS-SRTP; datos por SCTP sobre DTLS</text>

  <text x="32" y="278" class="d11">intercambia: descripciones SDP con oferta/respuesta (JSEP)</text>
  <text x="356" y="278" class="d11">Por tanto, el cifrado NO es opcional</text>

  <rect x="22" y="300" width="636" height="24" rx="4" fill="#fdf3e3"/>
  <text x="340" y="316" text-anchor="middle" class="k11">CÓDECS OBLIGATORIOS: audio, OPUS y G.711 (RFC 7874) · vídeo, VP8 y H.264 Constrained Baseline (RFC 7742)</text>

  <text x="658" y="344" text-anchor="end" class="n11">[Fuente: RFC 8825 y bloque asociado · RFC 9429 · W3C WebRTC 1.0]</text>
</svg>
```

---

## D12 · Travesía de NAT: STUN pregunta, TURN carga, ICE decide

**Sección**: §2.2.2 — El estándar WebRTC y la comunicación en tiempo real
**Propósito**: Deshacer la confusión más repetida del tema separando las tres piezas por su función y por su coste, y mostrando los tres tipos de candidato.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 378" role="img" aria-label="Esquema de la travesía de traducción de direcciones de red en WebRTC: STUN descubre la dirección pública y no transporta media, TURN retransmite todo el tráfico cuando no hay camino directo y es el recurso caro, e ICE es el algoritmo que recoge los tres tipos de candidato, los empareja y elige el mejor camino">
  <style>.h12{font:700 13px system-ui,sans-serif;fill:#0055a0}.k12{font:700 10px system-ui,sans-serif;fill:#0055a0}.d12{font:9px system-ui,sans-serif;fill:#333}.n12{font:8.5px system-ui,sans-serif;fill:#666}.w12{font:700 9.5px system-ui,sans-serif;fill:#fff}.r12{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g12{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h12">Travesía de NAT: tres piezas que se confunden y no deben confundirse</text>

  <rect x="30" y="34" width="90" height="40" rx="4" fill="#0055a0"/>
  <text x="75" y="51" text-anchor="middle" class="w12">EQUIPO A</text>
  <text x="75" y="66" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">192.168.1.20</text>
  <rect x="128" y="34" width="50" height="40" rx="4" fill="#8a949e"/>
  <text x="153" y="58" text-anchor="middle" class="w12">NAT</text>

  <rect x="560" y="34" width="90" height="40" rx="4" fill="#0055a0"/>
  <text x="605" y="51" text-anchor="middle" class="w12">EQUIPO B</text>
  <text x="605" y="66" text-anchor="middle" style="fill:#dce8f4;font:8.5px system-ui,sans-serif">10.0.0.7</text>
  <rect x="502" y="34" width="50" height="40" rx="4" fill="#8a949e"/>
  <text x="527" y="58" text-anchor="middle" class="w12">NAT</text>

  <line x1="178" y1="60" x2="502" y2="60" stroke="#0055a0" stroke-width="2.2"/>
  <text x="340" y="52" text-anchor="middle" class="k12">CAMINO DIRECTO — el que ICE prefiere siempre</text>

  <rect x="196" y="88" width="130" height="28" rx="4" fill="#2d8659"/>
  <text x="261" y="106" text-anchor="middle" class="w12">STUN — barato</text>
  <rect x="354" y="88" width="130" height="28" rx="4" fill="#d13c3c"/>
  <text x="419" y="106" text-anchor="middle" class="w12">TURN — caro</text>

  <text x="340" y="132" text-anchor="middle" class="d12">Los dos son SERVIDORES AUXILIARES y NO están en el camino del media: STUN solo responde a una pregunta y TURN</text>
  <text x="340" y="144" text-anchor="middle" class="d12">solo entra en juego cuando el camino directo no existe. Quien decide cuál se usa es ICE, que no es un servidor</text>

  <rect x="22" y="158" width="206" height="88" rx="4" fill="#e6f2ec"/>
  <rect x="22" y="158" width="206" height="20" rx="4" fill="#2d8659"/>
  <text x="125" y="172" text-anchor="middle" class="w12">STUN — RFC 8489 (feb. 2020)</text>
  <text x="32" y="193" class="g12">PREGUNTA</text>
  <text x="32" y="207" class="d12">«¿Con qué dirección y puerto</text>
  <text x="32" y="220" class="d12">me ves?». Devuelve el candidato</text>
  <text x="32" y="233" class="d12">reflexivo por servidor</text>
  <text x="32" y="243" class="n12">NO transporta media. Obsoletó la 5389</text>

  <rect x="237" y="158" width="206" height="88" rx="4" fill="#fbe9e9"/>
  <rect x="237" y="158" width="206" height="20" rx="4" fill="#d13c3c"/>
  <text x="340" y="172" text-anchor="middle" class="w12">TURN — RFC 8656 (feb. 2020)</text>
  <text x="247" y="193" class="r12">CARGA</text>
  <text x="247" y="207" class="d12">Retransmite TODO el media cuando</text>
  <text x="247" y="220" class="d12">no hay camino directo posible</text>
  <text x="247" y="233" class="d12">Funciona siempre; hay que dimensionarlo</text>
  <text x="247" y="243" class="n12">Obsoletó las RFC 5766 y 6156</text>

  <rect x="452" y="158" width="206" height="88" rx="4" fill="#eef4fa"/>
  <rect x="452" y="158" width="206" height="20" rx="4" fill="#0055a0"/>
  <text x="555" y="172" text-anchor="middle" class="w12">ICE — RFC 8445 (jul. 2018)</text>
  <text x="462" y="193" class="k12">DECIDE</text>
  <text x="462" y="207" class="d12">NO es un servidor: es el ALGORITMO</text>
  <text x="462" y="220" class="d12">Recoge candidatos, los empareja,</text>
  <text x="462" y="233" class="d12">comprueba y elige el mejor camino</text>
  <text x="462" y="243" class="n12">Obsoletó la RFC 5245</text>

  <rect x="22" y="260" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="130" y="274" text-anchor="middle" class="w12">Tipo de candidato</text>
  <text x="360" y="274" text-anchor="middle" class="w12">De dónde sale</text>
  <text x="570" y="274" text-anchor="middle" class="w12">Preferencia de ICE</text>

  <rect x="22" y="282" width="636" height="18" fill="#f5f8fb"/>
  <text x="130" y="295" text-anchor="middle" class="d12">Anfitrión (host)</text>
  <text x="360" y="295" text-anchor="middle" class="d12">La dirección local de la propia interfaz</text>
  <text x="570" y="295" text-anchor="middle" class="g12">La más alta</text>

  <rect x="22" y="300" width="636" height="18" fill="#fff"/>
  <text x="130" y="313" text-anchor="middle" class="d12">Reflexivo por servidor</text>
  <text x="360" y="313" text-anchor="middle" class="d12">La que descubre STUN a través del NAT</text>
  <text x="570" y="313" text-anchor="middle" class="d12">Intermedia</text>

  <rect x="22" y="318" width="636" height="18" fill="#fbe9e9"/>
  <text x="130" y="331" text-anchor="middle" class="d12">Retransmitido (relay)</text>
  <text x="360" y="331" text-anchor="middle" class="d12">La que ofrece TURN retransmitiendo</text>
  <text x="570" y="331" text-anchor="middle" class="r12">La más baja: último recurso</text>

  <text x="340" y="352" text-anchor="middle" class="k12">REGLA MNEMOTÉCNICA: STUN PREGUNTA · TURN CARGA · ICE DECIDE</text>

  <text x="658" y="368" text-anchor="end" class="n12">[Fuente: RFC 8489 · RFC 8656 · RFC 8445]</text>
</svg>
```

---

## D13 · Códecs de audio y vídeo: tabla de decisión

**Sección**: §2.3.1 — Códecs de compresión de audio y vídeo
**Propósito**: Concentrar en un solo sitio los códecs con su año, su organismo y su tasa, y marcar los cuatro obligatorios en WebRTC, que conviene retener como conjunto.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 346" role="img" aria-label="Tabla de códecs de vídeo y de audio usados en videoconferencia, con su organismo, año y característica principal, marcando en verde los cuatro obligatorios en WebRTC: Opus y G punto 711 en audio y VP8 y H punto 264 en vídeo, y mostrando la escala de eficiencia por generación">
  <style>.h13{font:700 13px system-ui,sans-serif;fill:#0055a0}.k13{font:700 10px system-ui,sans-serif;fill:#0055a0}.d13{font:9px system-ui,sans-serif;fill:#333}.n13{font:8.5px system-ui,sans-serif;fill:#666}.w13{font:700 9.5px system-ui,sans-serif;fill:#fff}.g13{font:700 9px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h13">Códecs: los cuatro obligatorios en WebRTC y la escala de eficiencia</text>

  <rect x="22" y="32" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="90" y="46" text-anchor="middle" class="w13">VÍDEO</text>
  <text x="230" y="46" text-anchor="middle" class="w13">Organismo y año</text>
  <text x="452" y="46" text-anchor="middle" class="w13">Lo que hay que saber de él</text>
  <text x="622" y="46" text-anchor="middle" class="w13">WebRTC</text>

  <rect x="22" y="54" width="636" height="17" fill="#f5f8fb"/>
  <text x="90" y="66" text-anchor="middle" class="d13">H.261 y H.263</text><text x="230" y="66" text-anchor="middle" class="d13">UIT-T, 1988 y 1996</text>
  <text x="452" y="66" text-anchor="middle" class="d13">Videoconferencia sobre RDSI (H.320). Históricos</text><text x="622" y="66" text-anchor="middle" class="n13">—</text>

  <rect x="22" y="71" width="636" height="17" fill="#e6f2ec"/>
  <text x="90" y="83" text-anchor="middle" class="d13">H.264 / AVC</text><text x="230" y="83" text-anchor="middle" class="d13">UIT-T e ISO/IEC, 2003</text>
  <text x="452" y="83" text-anchor="middle" class="d13">El más extendido. Carga útil RTP en la RFC 6184</text><text x="622" y="83" text-anchor="middle" class="g13">OBLIGATORIO</text>

  <rect x="22" y="88" width="636" height="17" fill="#e6f2ec"/>
  <text x="90" y="100" text-anchor="middle" class="d13">VP8</text><text x="230" y="100" text-anchor="middle" class="d13">Google, RFC 6386, 2011</text>
  <text x="452" y="100" text-anchor="middle" class="d13">Libre de regalías. El otro obligatorio, no alternativa</text><text x="622" y="100" text-anchor="middle" class="g13">OBLIGATORIO</text>

  <rect x="22" y="105" width="636" height="17" fill="#f5f8fb"/>
  <text x="90" y="117" text-anchor="middle" class="d13">H.265 / HEVC</text><text x="230" y="117" text-anchor="middle" class="d13">UIT-T e ISO/IEC, 2013</text>
  <text x="452" y="117" text-anchor="middle" class="d13">Mitad de tasa que H.264. Frenado por las patentes. RFC 7798</text><text x="622" y="117" text-anchor="middle" class="n13">Opcional</text>

  <rect x="22" y="122" width="636" height="17" fill="#fff"/>
  <text x="90" y="134" text-anchor="middle" class="d13">VP9 y AV1</text><text x="230" y="134" text-anchor="middle" class="d13">Google 2013 · AOMedia 2018</text>
  <text x="452" y="134" text-anchor="middle" class="d13">Libres de regalías, con escalabilidad. AV1 en ascenso</text><text x="622" y="134" text-anchor="middle" class="n13">Opcional</text>

  <rect x="22" y="139" width="636" height="17" fill="#fdf3e3"/>
  <text x="90" y="151" text-anchor="middle" class="d13">H.266 / VVC</text><text x="230" y="151" text-anchor="middle" class="d13">UIT-T e ISO/IEC, 6-jul-2020</text>
  <text x="452" y="151" text-anchor="middle" class="d13">Entre un 40 y un 50 % menos que HEVC. Para 4K, 8K y HDR</text><text x="622" y="151" text-anchor="middle" class="n13">Opcional</text>

  <rect x="22" y="166" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="90" y="180" text-anchor="middle" class="w13">AUDIO</text>
  <text x="230" y="180" text-anchor="middle" class="w13">Tasa binaria</text>
  <text x="452" y="180" text-anchor="middle" class="w13">Lo que hay que saber de él</text>
  <text x="622" y="180" text-anchor="middle" class="w13">WebRTC</text>

  <rect x="22" y="188" width="636" height="17" fill="#e6f2ec"/>
  <text x="90" y="200" text-anchor="middle" class="d13">G.711</text><text x="230" y="200" text-anchor="middle" class="d13">64 kbit/s</text>
  <text x="452" y="200" text-anchor="middle" class="d13">PCM, banda estrecha (3,4 kHz). El clásico de la telefonía</text><text x="622" y="200" text-anchor="middle" class="g13">OBLIGATORIO</text>

  <rect x="22" y="205" width="636" height="17" fill="#f5f8fb"/>
  <text x="90" y="217" text-anchor="middle" class="d13">G.722</text><text x="230" y="217" text-anchor="middle" class="d13">64, 56 y 48 kbit/s</text>
  <text x="452" y="217" text-anchor="middle" class="d13">Banda ancha de 7 kHz: salto de calidad a igual tasa</text><text x="622" y="217" text-anchor="middle" class="n13">Opcional</text>

  <rect x="22" y="222" width="636" height="17" fill="#fff"/>
  <text x="90" y="234" text-anchor="middle" class="d13">G.729</text><text x="230" y="234" text-anchor="middle" class="d13">8 kbit/s</text>
  <text x="452" y="234" text-anchor="middle" class="d13">Voz muy comprimida, para enlaces estrechos</text><text x="622" y="234" text-anchor="middle" class="n13">Opcional</text>

  <rect x="22" y="239" width="636" height="17" fill="#e6f2ec"/>
  <text x="90" y="251" text-anchor="middle" class="d13">Opus</text><text x="230" y="251" text-anchor="middle" class="d13">6 a 510 kbit/s</text>
  <text x="452" y="251" text-anchor="middle" class="d13">RFC 6716. Adaptativo, banda completa. Trama de 2,5 a 60 ms</text><text x="622" y="251" text-anchor="middle" class="g13">OBLIGATORIO</text>

  <rect x="22" y="270" width="312" height="50" rx="4" fill="#eef4fa"/>
  <text x="32" y="286" class="k13">LA ESCALA DE EFICIENCIA, POR GENERACIONES</text>
  <text x="32" y="300" class="d13">Cada generación da la MITAD de tasa a igual calidad</text>
  <text x="32" y="313" class="d13">H.264 → HEVC ≈ −50 %  ·  HEVC → VVC ≈ −40 a −50 %</text>

  <rect x="346" y="270" width="312" height="50" rx="4" fill="#fdf3e3"/>
  <text x="356" y="286" class="k13">EL DETALLE PROPIO DEL TIEMPO REAL</text>
  <text x="356" y="300" class="d13">NO se usan imágenes B: predecir desde imágenes futuras</text>
  <text x="356" y="313" class="d13">obliga a esperar, y esa espera es retardo. Solo I y P</text>

  <text x="658" y="338" text-anchor="end" class="n13">[Fuente: RFC 6716, 7742 y 7874 · UIT-T H.264, H.265, H.266, G.711, G.722, G.729]</text>
</svg>
```

---

## D14 · Los cuatro parámetros de calidad y sus umbrales

**Sección**: §2.3.2 — Calidad de servicio y gestión de ancho de banda
**Propósito**: Reunir los cuatro umbrales como conjunto, con el efecto perceptible de cada uno y el marcado DSCP recomendado.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" role="img" aria-label="Los cuatro parámetros de calidad de una comunicación en tiempo real con sus umbrales: ancho de banda según resolución, retardo de 150 milisegundos según la recomendación G punto 114, fluctuación por debajo de 30 milisegundos y pérdida de paquetes por debajo del 1 por ciento; con las tres estrategias de mejora y el marcado DSCP recomendado por la RFC 8837">
  <style>.h14{font:700 13px system-ui,sans-serif;fill:#0055a0}.k14{font:700 10px system-ui,sans-serif;fill:#0055a0}.d14{font:9px system-ui,sans-serif;fill:#333}.n14{font:8.5px system-ui,sans-serif;fill:#666}.w14{font:700 9.5px system-ui,sans-serif;fill:#fff}.r14{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g14{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h14">Los cuatro parámetros de calidad, sus umbrales y su efecto</text>

  <rect x="22" y="32" width="156" height="78" rx="4" fill="#eef4fa"/>
  <rect x="22" y="32" width="156" height="20" rx="4" fill="#0055a0"/>
  <text x="100" y="46" text-anchor="middle" class="w14">1 · ANCHO DE BANDA</text>
  <text x="30" y="67" class="d14">360p ≈ 0,5 Mbit/s</text>
  <text x="30" y="80" class="d14">720p ≈ 1,5 Mbit/s</text>
  <text x="30" y="93" class="d14">1080p ≈ 3 Mbit/s</text>
  <text x="30" y="105" class="n14">Efecto: baja la calidad</text>

  <rect x="186" y="32" width="156" height="78" rx="4" fill="#fbe9e9"/>
  <rect x="186" y="32" width="156" height="20" rx="4" fill="#d13c3c"/>
  <text x="264" y="46" text-anchor="middle" class="w14">2 · RETARDO</text>
  <text x="194" y="67" class="r14">≤ 150 ms boca a oreja</text>
  <text x="194" y="80" class="d14">150 a 400 ms: con reservas</text>
  <text x="194" y="93" class="d14">&gt; 400 ms: inaceptable</text>
  <text x="194" y="105" class="n14">La gente se pisa. UIT-T G.114</text>

  <rect x="350" y="32" width="156" height="78" rx="4" fill="#fdf3e3"/>
  <rect x="350" y="32" width="156" height="20" rx="4" fill="#e89822"/>
  <text x="428" y="46" text-anchor="middle" class="w14">3 · FLUCTUACIÓN (jitter)</text>
  <text x="358" y="67" class="d14">Objetivo: &lt; 30 ms</text>
  <text x="358" y="80" class="d14">Se absorbe con un almacén</text>
  <text x="358" y="93" class="d14">intermedio, que AÑADE retardo</text>
  <text x="358" y="105" class="n14">Compromiso central del diseño</text>

  <rect x="514" y="32" width="144" height="78" rx="4" fill="#fbe9e9"/>
  <rect x="514" y="32" width="144" height="20" rx="4" fill="#d13c3c"/>
  <text x="586" y="46" text-anchor="middle" class="w14">4 · PÉRDIDA</text>
  <text x="522" y="67" class="r14">Objetivo: &lt; 1 %</text>
  <text x="522" y="80" class="d14">Audio: cortes, se disimulan</text>
  <text x="522" y="93" class="d14">Vídeo: rompe la predicción</text>
  <text x="522" y="105" class="n14">Pide imagen I: FIR y PLI</text>

  <text x="24" y="132" class="k14">LAS TRES ESTRATEGIAS, EN ORDEN DE COSTE Y DE ALCANCE</text>

  <rect x="22" y="140" width="206" height="62" rx="4" fill="#eef4fa"/>
  <text x="32" y="156" class="k14">A · SOBREDIMENSIONAR</text>
  <text x="32" y="171" class="d14">Poner capacidad de sobra</text>
  <text x="32" y="184" class="d14">Funciona DENTRO de la red propia</text>
  <text x="32" y="196" class="n14">Y no funciona fuera de ella</text>

  <rect x="237" y="140" width="206" height="62" rx="4" fill="#fdf3e3"/>
  <text x="247" y="156" class="k14">B · PRIORIZAR (DiffServ)</text>
  <text x="247" y="171" class="d14">Marcar con DSCP (RFC 2474)</text>
  <text x="247" y="184" class="d14">Solo sirve si la red lo RESPETA</text>
  <text x="247" y="196" class="n14">Fuera del dominio propio se reescribe</text>

  <rect x="452" y="140" width="206" height="62" rx="4" fill="#e6f2ec"/>
  <text x="462" y="156" class="k14">C · ADAPTAR (congestión)</text>
  <text x="462" y="171" class="d14">El extremo mide con RTCP y</text>
  <text x="462" y="184" class="d14">ajusta la tasa del códec (RFC 8836)</text>
  <text x="462" y="196" class="g14">Sostiene la reunión por internet</text>

  <rect x="22" y="216" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="140" y="230" text-anchor="middle" class="w14">Flujo</text>
  <text x="330" y="230" text-anchor="middle" class="w14">Marcado DSCP recomendado (RFC 8837)</text>
  <text x="560" y="230" text-anchor="middle" class="w14">Por qué</text>

  <rect x="22" y="238" width="636" height="18" fill="#e6f2ec"/>
  <text x="140" y="251" text-anchor="middle" class="d14">Audio</text>
  <text x="330" y="251" text-anchor="middle" class="g14">EF (46) — reenvío expedito</text>
  <text x="560" y="251" text-anchor="middle" class="d14">Sin audio no hay reunión</text>

  <rect x="22" y="256" width="636" height="18" fill="#f5f8fb"/>
  <text x="140" y="269" text-anchor="middle" class="d14">Vídeo de alta prioridad</text>
  <text x="330" y="269" text-anchor="middle" class="d14">AF41 (34)</text>
  <text x="560" y="269" text-anchor="middle" class="d14">Importante, pero prescindible</text>

  <rect x="22" y="274" width="636" height="18" fill="#fff"/>
  <text x="140" y="287" text-anchor="middle" class="d14">Datos y compartición</text>
  <text x="330" y="287" text-anchor="middle" class="d14">Clases inferiores</text>
  <text x="560" y="287" text-anchor="middle" class="d14">Tolera retardo</text>

  <text x="340" y="310" text-anchor="middle" class="k14">EL PRINCIPIO: EL AUDIO SE PRIORIZA POR ENCIMA DEL VÍDEO — una reunión sin vídeo funciona; sin audio, no existe</text>

  <text x="658" y="332" text-anchor="end" class="n14">[Fuente: UIT-T G.114 · RFC 2474 · RFC 8836 · RFC 8837]</text>
</svg>
```

---

## D15 · Interoperabilidad: las cuatro vías, de la limpia a la sucia

**Sección**: §2.4.2 — Interoperabilidad entre sistemas y entornos heterogéneos
**Propósito**: Ordenar las opciones por lo que cuestan y cerrar con el dato jurídico que las acompaña: la audioconferencia basta para una sesión válida.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 332" role="img" aria-label="Las cuatro vías de interoperación entre sistemas de videoconferencia heterogéneos, ordenadas de menor a mayor coste: estándar común, pasarela que traduce señalización, transcodificación que traduce también el media, y acceso telefónico como mínimo común denominador; con los cuatro requisitos que hay que exigir en un pliego">
  <style>.h15{font:700 13px system-ui,sans-serif;fill:#0055a0}.k15{font:700 10px system-ui,sans-serif;fill:#0055a0}.d15{font:9px system-ui,sans-serif;fill:#333}.n15{font:8.5px system-ui,sans-serif;fill:#666}.w15{font:700 9.5px system-ui,sans-serif;fill:#fff}.g15{font:700 9.5px system-ui,sans-serif;fill:#2d8659}.r15{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}</style>
  <text x="340" y="19" text-anchor="middle" class="h15">Las cuatro vías de interoperación, ordenadas por lo que cuestan</text>

  <rect x="22" y="32" width="636" height="14" rx="7" fill="#eef4fa"/>
  <rect x="22" y="32" width="159" height="14" rx="7" fill="#2d8659"/>
  <rect x="499" y="32" width="159" height="14" rx="7" fill="#d13c3c"/>
  <text x="22" y="60" class="g15">SIN COSTE</text>
  <text x="658" y="60" text-anchor="end" class="r15">MÁXIMA DEGRADACIÓN</text>

  <rect x="22" y="68" width="152" height="94" rx="4" fill="#e6f2ec"/>
  <rect x="22" y="68" width="152" height="20" rx="4" fill="#2d8659"/>
  <text x="98" y="82" text-anchor="middle" class="w15">1 · ESTÁNDAR COMÚN</text>
  <text x="30" y="103" class="d15">Todos los extremos hablan</text>
  <text x="30" y="116" class="d15">SIP y RTP, con códecs</text>
  <text x="30" y="129" class="d15">compartidos</text>
  <text x="30" y="146" class="g15">Coste: CERO</text>
  <text x="30" y="157" class="n15">Lo que exigir en el pliego</text>

  <rect x="184" y="68" width="152" height="94" rx="4" fill="#eef4fa"/>
  <rect x="184" y="68" width="152" height="20" rx="4" fill="#0055a0"/>
  <text x="260" y="82" text-anchor="middle" class="w15">2 · PASARELA</text>
  <text x="192" y="103" class="d15">Traduce SEÑALIZACIÓN:</text>
  <text x="192" y="116" class="d15">H.323 a SIP, SIP a WebRTC,</text>
  <text x="192" y="129" class="d15">red telefónica a SIP</text>
  <text x="192" y="146" class="k15">Coste: BAJO</text>
  <text x="192" y="157" class="n15">Si los códecs coinciden</text>

  <rect x="346" y="68" width="152" height="94" rx="4" fill="#fdf3e3"/>
  <rect x="346" y="68" width="152" height="20" rx="4" fill="#e89822"/>
  <text x="422" y="82" text-anchor="middle" class="w15">3 · TRANSCODIFICACIÓN</text>
  <text x="354" y="103" class="d15">Traduce también el MEDIA:</text>
  <text x="354" y="116" class="d15">decodifica y recodifica</text>
  <text x="354" y="129" class="d15">Funciona siempre</text>
  <text x="354" y="146" class="r15">Coste: ALTO</text>
  <text x="354" y="157" class="n15">Cómputo, retardo y CALIDAD</text>

  <rect x="508" y="68" width="150" height="94" rx="4" fill="#fbe9e9"/>
  <rect x="508" y="68" width="150" height="20" rx="4" fill="#d13c3c"/>
  <text x="583" y="82" text-anchor="middle" class="w15">4 · ACCESO TELEFÓNICO</text>
  <text x="516" y="103" class="d15">El mínimo común</text>
  <text x="516" y="116" class="d15">denominador: entrar</text>
  <text x="516" y="129" class="d15">por teléfono</text>
  <text x="516" y="146" class="r15">Se pierde el vídeo</text>
  <text x="516" y="157" class="n15">Y funciona SIEMPRE</text>

  <rect x="22" y="176" width="636" height="40" rx="4" fill="#e6f2ec"/>
  <text x="32" y="192" class="g15">EL DATO JURÍDICO QUE ACOMPAÑA A LA CUARTA VÍA, Y QUE LA HACE MEJOR DE LO QUE PARECE</text>
  <text x="32" y="207" class="d15">El art. 17.1 de la Ley 40/2015 considera medios válidos «el correo electrónico, LAS AUDIOCONFERENCIAS y las videoconferencias»</text>

  <rect x="22" y="226" width="636" height="76" rx="4" fill="#eef4fa"/>
  <text x="32" y="242" class="k15">LOS CUATRO REQUISITOS QUE HAY QUE EXIGIR EN UN PLIEGO PARA NO QUEDAR ATRAPADO</text>
  <text x="32" y="258" class="d15">1. Señalización normalizada: SIP (RFC 3261) y, si hay parque heredado, H.323</text>
  <text x="32" y="271" class="d15">2. Códecs normalizados: H.264 y VP8 en vídeo, Opus y G.711 en audio — el mínimo de WebRTC, que garantiza el entendimiento</text>
  <text x="32" y="284" class="d15">3. Acceso por NAVEGADOR sin instalación, basado en WebRTC, y acceso telefónico de respaldo</text>
  <text x="32" y="297" class="d15">4. EXPORTABILIDAD: grabaciones y actas en formatos del ENI, no en contenedor propietario. Sin marca (art. 126.6 LCSP)</text>

  <text x="658" y="324" text-anchor="end" class="n15">[Fuente: RFC 3261 · Ley 40/2015, art. 17.1 · RD 4/2010 (ENI) · Ley 9/2017]</text>
</svg>
```

---

## D16 · Acondicionamiento de la sala: acústica y luz, con sus cotas

**Sección**: §3.1.1 — Acústica, insonorización y acondicionamiento lumínico
**Propósito**: Separar aislamiento de acondicionamiento —la confusión central del epígrafe— y reunir en un sitio los valores normativos exigibles, que son datos cerrados.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 366" role="img" aria-label="Acondicionamiento de una sala de videoconferencia: distinción entre aislamiento acústico, que impide que el sonido entre o salga, y acondicionamiento acústico, que controla la reverberación interior; valores límite del tiempo de reverberación del Documento Básico HR del Código Técnico de la Edificación y valores de iluminación de la norma UNE-EN 12464-1 de 2022">
  <style>.h16{font:700 13px system-ui,sans-serif;fill:#0055a0}.k16{font:700 10px system-ui,sans-serif;fill:#0055a0}.d16{font:9px system-ui,sans-serif;fill:#333}.n16{font:8.5px system-ui,sans-serif;fill:#666}.w16{font:700 9.5px system-ui,sans-serif;fill:#fff}.r16{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g16{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h16">Acondicionamiento de salas: dos acústicas distintas y sus cifras</text>

  <rect x="22" y="32" width="312" height="80" rx="4" fill="#eef4fa"/>
  <rect x="22" y="32" width="312" height="20" rx="4" fill="#0055a0"/>
  <text x="178" y="46" text-anchor="middle" class="w16">AISLAMIENTO ACÚSTICO (insonorización)</text>
  <text x="32" y="67" class="d16">Impedir que el sonido ENTRE o SALGA de la sala</text>
  <text x="32" y="81" class="d16">Se resuelve con MASA, ESTANQUEIDAD y DESACOPLAMIENTO:</text>
  <text x="32" y="94" class="d16">tabique pesado, puerta con junta, sin rendijas, suelo flotante</text>
  <text x="32" y="107" class="k16">Sirve para: la CONFIDENCIALIDAD y el ruido exterior</text>

  <rect x="346" y="32" width="312" height="80" rx="4" fill="#e6f2ec"/>
  <rect x="346" y="32" width="312" height="20" rx="4" fill="#2d8659"/>
  <text x="502" y="46" text-anchor="middle" class="w16">ACONDICIONAMIENTO ACÚSTICO (corrección)</text>
  <text x="356" y="67" class="d16">Controlar cómo se comporta el sonido DENTRO de la sala</text>
  <text x="356" y="81" class="d16">Se resuelve con ABSORCIÓN y DIFUSIÓN: paneles, moqueta,</text>
  <text x="356" y="94" class="d16">cortinas, techo absorbente</text>
  <text x="356" y="107" class="g16">Sirve para: la INTELIGIBILIDAD</text>

  <rect x="22" y="120" width="636" height="24" rx="4" fill="#fbe9e9"/>
  <text x="340" y="136" text-anchor="middle" class="r16">SON PROBLEMAS DISTINTOS Y CONTRAPUESTOS: una sala bien aislada suele tener una acústica interior pésima</text>

  <text x="24" y="164" class="k16">TIEMPO DE REVERBERACIÓN — VALORES LÍMITE DEL CTE, DOCUMENTO BÁSICO HR (RD 1371/2007), APARTADO 2.2</text>

  <rect x="22" y="172" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="200" y="186" text-anchor="middle" class="w16">Recinto</text>
  <text x="452" y="186" text-anchor="middle" class="w16">Condición</text>
  <text x="610" y="186" text-anchor="middle" class="w16">Límite</text>

  <rect x="22" y="194" width="636" height="18" fill="#f5f8fb"/>
  <text x="200" y="207" text-anchor="middle" class="d16">Aula o sala de conferencias</text>
  <text x="452" y="207" text-anchor="middle" class="d16">VACÍA, sin ocupación ni mobiliario, V &lt; 350 m³</text>
  <text x="610" y="207" text-anchor="middle" class="r16">T ≤ 0,7 s</text>

  <rect x="22" y="212" width="636" height="18" fill="#fff"/>
  <text x="200" y="225" text-anchor="middle" class="d16">Aula o sala de conferencias</text>
  <text x="452" y="225" text-anchor="middle" class="d16">Vacía pero INCLUYENDO EL TOTAL DE LAS BUTACAS</text>
  <text x="610" y="225" text-anchor="middle" class="r16">T ≤ 0,5 s</text>

  <rect x="22" y="230" width="636" height="18" fill="#f5f8fb"/>
  <text x="200" y="243" text-anchor="middle" class="d16">Restaurante o comedor</text>
  <text x="452" y="243" text-anchor="middle" class="d16">Vacío</text>
  <text x="610" y="243" text-anchor="middle" class="r16">T ≤ 0,9 s</text>

  <rect x="22" y="248" width="636" height="18" fill="#fdf3e3"/>
  <text x="200" y="261" text-anchor="middle" class="d16">Aula o sala de conferencias</text>
  <text x="452" y="261" text-anchor="middle" class="d16">Volumen MAYOR que 350 m³</text>
  <text x="610" y="261" text-anchor="middle" class="k16">Estudio específico</text>

  <rect x="22" y="276" width="312" height="60" rx="4" fill="#eef4fa"/>
  <text x="32" y="292" class="k16">ILUMINACIÓN — UNE-EN 12464-1:2022</text>
  <text x="32" y="307" class="d16">Oficinas y salas de reuniones y conferencias:</text>
  <text x="32" y="320" class="d16">500 lx · UGR ≤ 19 · Uo ≥ 0,60 · Ra ≥ 80</text>
  <text x="32" y="331" class="n16">Sobre el plano de trabajo, a 0,85 m del suelo</text>

  <rect x="346" y="276" width="312" height="60" rx="4" fill="#fdf3e3"/>
  <text x="356" y="292" class="k16">LAS TRES REGLAS PROPIAS DE UNA SALA DE VÍDEO</text>
  <text x="356" y="307" class="d16">1. Luz DE FRENTE, no de detrás: la ventana al fondo</text>
  <text x="356" y="320" class="d16">convierte a la persona en silueta   2. Luz DIFUSA</text>
  <text x="356" y="331" class="d16">3. Zonificada y regulable: la luz y la pantalla se estorban</text>

  <text x="658" y="358" text-anchor="end" class="n16">[Fuente: CTE DB-HR (RD 1371/2007), ap. 2.2 · UNE-EN 12464-1:2022 · ANSI/AVIXA V201.01:2021]</text>
</svg>
```

---

## D17 · DISCAS: cómo se calcula el tamaño de la pantalla

**Sección**: §3.2.2 — Visualización, cableado y electrónica de red
**Propósito**: Es el contenido más diferencial de §3. Fija las dos categorías, los dos factores de agudeza y las fórmulas, y muestra la zona de visión válida en planta.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 392" role="img" aria-label="La norma DISCAS de AVIXA para calcular el tamaño mínimo de imagen: dos categorías de necesidad visual, decisión básica con factor de agudeza 200 y decisión analítica con factor de agudeza 3438, sus fórmulas, y la zona de visión válida en planta delimitada por el espectador más cercano y el más lejano">
  <style>.h17{font:700 13px system-ui,sans-serif;fill:#0055a0}.k17{font:700 10px system-ui,sans-serif;fill:#0055a0}.d17{font:9px system-ui,sans-serif;fill:#333}.n17{font:8.5px system-ui,sans-serif;fill:#666}.w17{font:700 9.5px system-ui,sans-serif;fill:#fff}.f17{font:700 11px ui-monospace,monospace;fill:#0055a0}.g17{font:700 9.5px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="340" y="19" text-anchor="middle" class="h17">DISCAS: el tamaño de la pantalla no es una opinión, es una norma</text>
  <text x="340" y="35" text-anchor="middle" class="n17">ANSI/AVIXA V202.01 — edición vigente :2026 · formulación de la edición :2016</text>

  <rect x="22" y="48" width="312" height="104" rx="4" fill="#eef4fa"/>
  <rect x="22" y="48" width="312" height="20" rx="4" fill="#0055a0"/>
  <text x="178" y="62" text-anchor="middle" class="w17">DECISIÓN BÁSICA (BDM) — factor de agudeza 200</text>
  <text x="32" y="83" class="d17">El espectador decide SIN resolver cada detalle:</text>
  <text x="32" y="96" class="d17">presentaciones, aulas, salas de juntas, señalización</text>
  <text x="178" y="118" text-anchor="middle" class="f17">IH = FV / (200 × %EH)</text>
  <text x="178" y="134" text-anchor="middle" class="f17">FV = IH × %EH × 200</text>
  <text x="32" y="147" class="n17">%EH = altura del elemento más pequeño, en % de la altura de imagen</text>

  <rect x="346" y="48" width="312" height="104" rx="4" fill="#fdf3e3"/>
  <rect x="346" y="48" width="312" height="20" rx="4" fill="#e89822"/>
  <text x="502" y="62" text-anchor="middle" class="w17">DECISIÓN ANALÍTICA (ADM) — factor de agudeza 3438</text>
  <text x="356" y="83" class="d17">El espectador debe RESOLVER CADA ELEMENTO: imagen</text>
  <text x="356" y="96" class="d17">médica, planos, esquemas, inspección, análisis forense</text>
  <text x="502" y="118" text-anchor="middle" class="f17">IH = (IR × FV) / 3438</text>
  <text x="502" y="134" text-anchor="middle" class="f17">FV = (IH / IR) × 3438</text>
  <text x="356" y="147" class="n17">IR = resolución vertical · 3438 = minutos de arco de un radián</text>

  <text x="24" y="172" class="k17">LA ZONA DE VISIÓN VÁLIDA, EN PLANTA</text>

  <rect x="250" y="182" width="180" height="9" fill="#0055a0"/>
  <text x="242" y="190" text-anchor="end" class="k17">PANTALLA</text>

  <path d="M250 191 L140 292 L540 292 L430 191 Z" fill="#e6f2ec" stroke="#2d8659" stroke-width="1.2"/>
  <line x1="222" y1="217" x2="458" y2="217" stroke="#d13c3c" stroke-width="1.4" stroke-dasharray="5,3"/>
  <line x1="141" y1="291" x2="539" y2="291" stroke="#d13c3c" stroke-width="1.4" stroke-dasharray="5,3"/>
  <text x="340" y="250" text-anchor="middle" class="g17">ZONA DE VISIÓN CONFORME</text>
  <text x="340" y="266" text-anchor="middle" class="d17">La delimitan las dos líneas rojas</text>

  <text x="30" y="212" class="n17">IO = desplazamiento</text>
  <text x="30" y="224" class="n17">vertical de la imagen</text>
  <text x="30" y="284" class="n17">1,732 = tan 60°</text>
  <text x="30" y="296" class="n17">(30° sobre el ojo)</text>
  <text x="556" y="212" class="n17">CV: espectador</text>
  <text x="556" y="224" class="n17">MÁS CERCANO</text>
  <text x="556" y="284" class="n17">FV: espectador</text>
  <text x="556" y="296" class="n17">MÁS LEJANO</text>

  <text x="340" y="312" text-anchor="middle" class="d17">CV = (IH + IO) × 1,732 · Y en el plano horizontal: ningún espectador a más de 60° de cualquier punto de la imagen</text>

  <rect x="22" y="324" width="636" height="46" rx="4" fill="#fdf3e3"/>
  <text x="32" y="339" class="k17">LA CONSECUENCIA PRESUPUESTARIA QUE NADIE ESPERA</text>
  <text x="32" y="352" class="d17">La pantalla que la norma exige suele ser bastante mayor que la que se instala por costumbre. Si no cabe, la salida no es resignarse:</text>
  <text x="32" y="364" class="d17">es ACERCAR al espectador más lejano o AUMENTAR el tamaño de letra, que es lo que hace crecer el %EH y relaja la exigencia</text>

  <text x="658" y="384" text-anchor="end" class="n17">[Fuente: ANSI/AVIXA V202.01 (DISCAS)]</text>
</svg>
```

---

## D18 · Los dos regímenes de la sesión a distancia y el ENS de la sala

**Sección**: §4 — Marco jurídico y aplicación en la Administración pública
**Propósito**: Cerrar el tema con la comparación jurídica que más se falla y con el mapa de medidas del ENS que recaen sobre una sala municipal, incluida la que nombra los proyectores.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 384" role="img" aria-label="Comparación entre el régimen general del artículo 17 de la Ley 40/2015, que permite las sesiones a distancia de los órganos colegiados como regla ordinaria, y el régimen local del artículo 46.3 de la Ley 7/1985, que solo las permite ante fuerza mayor, grave riesgo colectivo o catástrofe pública y con los miembros en territorio español; con las medidas del Esquema Nacional de Seguridad aplicables a una sala municipal">
  <style>.h18{font:700 13px system-ui,sans-serif;fill:#0055a0}.k18{font:700 10px system-ui,sans-serif;fill:#0055a0}.d18{font:9px system-ui,sans-serif;fill:#333}.n18{font:8.5px system-ui,sans-serif;fill:#666}.w18{font:700 9.5px system-ui,sans-serif;fill:#fff}.r18{font:700 9.5px system-ui,sans-serif;fill:#d13c3c}.g18{font:700 9.5px system-ui,sans-serif;fill:#2d8659}.c18{font:700 9px ui-monospace,monospace;fill:#0055a0}</style>
  <text x="340" y="19" text-anchor="middle" class="h18">Sesión a distancia: hay DOS regímenes, y el local es el estricto</text>

  <rect x="22" y="32" width="312" height="140" rx="4" fill="#e6f2ec"/>
  <rect x="22" y="32" width="312" height="22" rx="4" fill="#2d8659"/>
  <text x="178" y="48" text-anchor="middle" class="w18">GENERAL — art. 17 de la Ley 40/2015</text>
  <text x="32" y="70" class="g18">LA SESIÓN A DISTANCIA ES LA REGLA ORDINARIA</text>
  <text x="32" y="84" class="d18">«Todos los órganos colegiados se podrán constituir [...]</text>
  <text x="32" y="97" class="d18">tanto de forma presencial como a distancia, salvo que su</text>
  <text x="32" y="110" class="d18">reglamento interno recoja expresa y excepcionalmente</text>
  <text x="32" y="123" class="d18">lo contrario»</text>
  <text x="32" y="140" class="k18">Ap. 2: quórum con asistencia presencial O A DISTANCIA</text>
  <text x="32" y="153" class="k18">Ap. 3: la convocatoria dice el SISTEMA DE CONEXIÓN</text>
  <text x="32" y="166" class="k18">Ap. 5: el acuerdo se adopta EN LA SEDE DEL ÓRGANO</text>

  <rect x="346" y="32" width="312" height="140" rx="4" fill="#fbe9e9"/>
  <rect x="346" y="32" width="312" height="22" rx="4" fill="#d13c3c"/>
  <text x="502" y="48" text-anchor="middle" class="w18">LOCAL — art. 46.3 de la Ley 7/1985 (LBRL)</text>
  <text x="356" y="70" class="r18">LA SESIÓN A DISTANCIA ES EXCEPCIONAL</text>
  <text x="356" y="84" class="d18">Solo cuando concurran «situaciones excepcionales de</text>
  <text x="356" y="97" class="d18">FUERZA MAYOR, de GRAVE RIESGO COLECTIVO, o</text>
  <text x="356" y="110" class="d18">CATÁSTROFES PÚBLICAS», apreciadas por el alcalde</text>
  <text x="356" y="123" class="d18">o presidente (introducido por el RDL 11/2020)</text>
  <text x="356" y="140" class="r18">Los miembros, EN TERRITORIO ESPAÑOL</text>
  <text x="356" y="153" class="r18">Identidad acreditada</text>
  <text x="356" y="166" class="r18">Garantizado el carácter PÚBLICO O SECRETO</text>

  <rect x="22" y="182" width="636" height="20" rx="3" fill="#0055a0"/>
  <text x="150" y="196" text-anchor="middle" class="w18">Requisito del art. 17.1</text>
  <text x="450" y="196" text-anchor="middle" class="w18">Su traducción técnica en el sistema</text>

  <rect x="22" y="204" width="636" height="17" fill="#f5f8fb"/>
  <text x="150" y="216" text-anchor="middle" class="d18">1. IDENTIDAD de los miembros</text>
  <text x="450" y="216" text-anchor="middle" class="d18">Identidad federada y segundo factor; nombre verificado. Nunca enlace anónimo</text>

  <rect x="22" y="221" width="636" height="17" fill="#fff"/>
  <text x="150" y="233" text-anchor="middle" class="d18">2. CONTENIDO de las manifestaciones</text>
  <text x="450" y="233" text-anchor="middle" class="d18">Audio inteligible — de ahí toda la sección 3 — y, en su caso, grabación o acta</text>

  <rect x="22" y="238" width="636" height="17" fill="#f5f8fb"/>
  <text x="150" y="250" text-anchor="middle" class="d18">3. MOMENTO en que se producen</text>
  <text x="450" y="250" text-anchor="middle" class="d18">Marca de tiempo fiable y registro de conexiones: quién estaba en cada votación</text>

  <rect x="22" y="255" width="636" height="17" fill="#fff"/>
  <text x="150" y="267" text-anchor="middle" class="d18">4. INTERACTIVIDAD en tiempo real</text>
  <text x="450" y="267" text-anchor="middle" class="d18">Retardo dentro del umbral de la G.114 y canal de petición de palabra</text>

  <rect x="22" y="272" width="636" height="17" fill="#fbe9e9"/>
  <text x="150" y="284" text-anchor="middle" class="d18">5. DISPONIBILIDAD de los medios</text>
  <text x="450" y="284" text-anchor="middle" class="r18">Redundancia y respaldo telefónico: un corte en la votación VICIA EL ACUERDO</text>

  <rect x="22" y="300" width="636" height="58" rx="4" fill="#fdf3e3"/>
  <text x="32" y="316" class="k18">EL ENS DE UNA SALA MUNICIPAL — la familia mp.if y la medida que nombra los proyectores</text>
  <text x="32" y="330" class="d18"><tspan class="c18">mp.if.3</tspan> ACONDICIONAMIENTO DE LOS LOCALES: temperatura y humedad · amenazas del análisis de riesgos · protección del CABLEADO</text>
  <text x="32" y="342" class="d18"><tspan class="c18">mp.eq.4</tspan> «otros dispositivos conectados a la red» enumera los «DISPOSITIVOS MULTIMEDIA: PROYECTORES, ALTAVOCES INTELIGENTES»</text>
  <text x="32" y="354" class="d18"><tspan class="c18">mp.if.1</tspan> áreas separadas · <tspan class="c18">mp.if.2</tspan> identificación de las personas · <tspan class="c18">mp.eq.1</tspan> puesto despejado · <tspan class="c18">mp.com.4</tspan> segmento separado</text>

  <text x="658" y="376" text-anchor="end" class="n18">[Fuente: Ley 40/2015, art. 17 · Ley 7/1985, art. 46.3 · RD 311/2022, anexo II]</text>
</svg>
```

---
