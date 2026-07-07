---
layout: default
title: Historia
nav_order: 3
---

# Historia y popularización de la impresión 3D

La historia de la impresión 3D es una transición tecnológica de más de cuarenta años en la que se cruzan patentes, laboratorios de investigación, empresas de prototipado rápido, comunidades de hardware abierto, repositorios de modelos, software libre, caída de costos, cultura maker y una nueva forma de aprender fabricación.

En este capítulo la impresión 3D se analiza como una tecnología que cambió de escala social. Primero fue una herramienta costosa para departamentos de ingeniería, laboratorios de investigación, diseño automotriz, aeroespacial y desarrollo de producto. Después se convirtió en una máquina de escritorio para diseñadores, escuelas, FabLabs y usuarios independientes. Hoy conviven ambos mundos: sistemas industriales de cientos de miles de dólares para polímeros, resinas y metales; impresoras profesionales de escritorio para ingeniería, odontología y diseño; e impresoras FDM accesibles que permiten a estudiantes y comunidades fabricar sus primeros prototipos.

Antes de la manufactura aditiva, **fabricar un prototipo físico podía tomar días, semanas o meses**. En ingeniería mecánica, diseño industrial y desarrollo de producto, una pieza requería normalmente maquinado, fundición, fabricación manual, moldes o herramentales. Esto hacía que el **error de diseño fuera caro**: una interferencia entre dos piezas, una mala ergonomía, un volumen incorrecto o un detalle geométrico mal resuelto podía descubrirse tarde.

La idea que impulsó a las primeras tecnologías de impresión 3D fue: **usar datos digitales para construir directamente un objeto físico**, capa por capa, sin fabricar primero un molde o retirar material de un bloque completo.

En sus primeras décadas, el término más usado no era "impresión 3D", sino **rapid prototyping** o prototipado rápido. El objetivo principal era acelerar el ciclo de desarrollo.

La pieza no necesariamente era final. Muchas veces era un modelo visual, una maqueta de ensamble, una pieza para verificar ergonomía, una forma para fundición a la cera perdida o un objeto para convencer a un cliente antes de fabricar el producto real.

## 1980–1986: estereolitografía, Chuck Hull y la primera patente clave

La tecnología que normalmente se reconoce como la primera impresión 3D comercial fue la **estereolitografía** o **SLA**. Chuck Hull, cofundador de 3D Systems, desarrolló la idea a inicios de los años ochenta. En 1983 produjo una de las primeras piezas impresas mediante fotopolimerización, en 1984 presentó la solicitud de patente y en 1986 se concedió la patente estadounidense **[US4575330A](https://patents.google.com/patent/US4575330A/en)**, titulada *Apparatus for Production of Three-Dimensional Objects by Stereolithography*.

La patente describe un sistema para fabricar objetos tridimensionales creando patrones de sección transversal sobre un medio líquido capaz de cambiar de estado físico, por ejemplo una resina curable con luz ultravioleta. Las capas sucesivas se integran entre sí hasta formar el objeto completo. Esa idea —convertir secciones digitales en capas físicas— sigue siendo la base conceptual de la impresión 3D actual.

### 2.1 Primera etapa comercial: 3D Systems y la SLA-1

3D Systems fue fundada en 1986 y comercializó la tecnología SLA en el ambiente industrial. La **SLA-1**, enviada comercialmente a finales de los años ochenta, se convirtió en uno de los símbolos del inicio de la impresión 3D como industria.

**Tipo de usuario de la época:**

- centros de diseño industrial;
- departamentos de ingeniería de empresas grandes;
- automotriz;
- aeroespacial;
- laboratorios de investigación;
- empresas de prototipado;
- oficinas de diseño de producto.

**Uso principal:**

- modelos conceptuales;
- validación de forma;
- prototipos para revisión visual;
- patrones para fundición;
- reducción de tiempos de diseño.

**Costo aproximado:**
Las primeras impresoras 3D industriales se encontraban en rangos de cientos de miles de dólares. Algunas fuentes históricas ubican equipos de los años ochenta en el orden de **300,000 a 400,000 USD**, sin considerar materiales, mantenimiento, software, instalación ni capacitación.

Ese dato es clave: la impresión 3D nació como tecnología de alto costo, no como herramienta doméstica. La democratización llegó mucho después.

<div class="placeholder">
<strong>Espacio sugerido para imagen histórica:</strong> 3D Systems SLA-1 o diagrama de estereolitografía con tanque de resina, láser UV y plataforma móvil. Archivo sugerido: <code>assets/img/historia/sla-1.png</code>.
</div>

## 3. 1987–1992: aparecen SLS y FDM, dos caminos que marcaron la industria

Después de SLA aparecieron otras familias tecnológicas. Dos fueron decisivas: **SLS**, basada en polvo y láser, y **FDM**, basada en extrusión de termoplástico.

### 3.1 Selective Laser Sintering: Carl Deckard, UT Austin y DTM

El **Sinterizado Selectivo por Láser** o **SLS** fue desarrollado por Carl Deckard y Joe Beaman en la Universidad de Texas en Austin durante los años ochenta. Una patente estadounidense representativa de esta familia tecnológica es **[US4863538A](https://patents.google.com/patent/US4863538A/en)**, *Method and apparatus for producing parts by selective sintering*. A diferencia de SLA, que utiliza resina líquida, SLS trabaja con polvo. Un láser sinteriza o fusiona selectivamente regiones de una cama de polvo, capa por capa.

La tecnología fue comercializada por **DTM Corporation**, empresa que después sería adquirida por 3D Systems en 2001. SLS se volvió muy importante porque permitió fabricar piezas funcionales, especialmente en polímeros como nylon, sin requerir soportes tradicionales: el polvo no sinterizado sostiene la pieza durante la fabricación.

**Tipo de usuario:**

- empresas de ingeniería avanzada;
- automotriz;
- aeroespacial;
- laboratorios de materiales;
- servicios de manufactura;
- fabricantes que necesitaban piezas funcionales de geometría compleja.

**Ventajas históricas de SLS:**

- piezas más funcionales que muchas piezas SLA tempranas;
- posibilidad de geometrías complejas;
- fabricación de lotes pequeños;
- menor dependencia de soportes;
- uso de polímeros técnicos.

**Limitaciones históricas:**

- máquinas costosas;
- control térmico complejo;
- manejo de polvo;
- postprocesado especializado;
- difícil adopción doméstica.

SLS nunca se volvió una tecnología doméstica masiva como FDM, pero sí fue una de las tecnologías que empujó a la manufactura aditiva hacia aplicaciones funcionales e industriales.

### 3.2 Fused Deposition Modeling: Scott Crump y Stratasys

La tecnología que más tarde dominaría la impresión 3D de escritorio fue **FDM** (*Fused Deposition Modeling*), patentada por Scott Crump y comercializada por **Stratasys**. La patente **[US5121329A](https://patents.google.com/patent/US5121329A/en)**, concedida en 1992, describe un método y aparato para crear objetos tridimensionales mediante deposición controlada de material.

FDM utiliza filamento termoplástico, lo calienta y lo deposita capa por capa. En el mundo abierto y maker también se usa el término **FFF** (*Fused Filament Fabrication*), especialmente para evitar el uso de una marca registrada asociada a Stratasys.

**Primer mercado de FDM:**

- ingeniería;
- prototipado funcional;
- diseño de producto;
- automotriz;
- herramentales ligeros;
- validación de piezas en ABS.

En 1992 Stratasys vendió su primera impresora FDM, la **3D Modeler**. A diferencia de SLA, FDM ofrecía una ruta con termoplásticos más familiares para ingeniería. La pieza podía no tener el acabado de una pieza de resina, pero acercaba la impresión 3D a prototipos más robustos.

<div class="placeholder">
<strong>Espacio sugerido para diagrama comparativo:</strong> SLA vs SLS vs FDM en los años noventa: resina, polvo y filamento. Archivo sugerido: <code>assets/img/historia/sla-sls-fdm.png</code>.
</div>

## 4. 1993–2000: prototipado rápido, Z Corporation y la idea de imprimir modelos más rápido

Durante los años noventa, la manufactura aditiva se mantuvo principalmente como una tecnología industrial. Los equipos eran costosos y estaban orientados a empresas que podían justificar el precio con ahorro de tiempo en diseño y desarrollo.

Una empresa importante fue **Z Corporation**, fundada en 1994 a partir de tecnología desarrollada en el MIT. Sus impresoras usaban una estrategia de **binder jetting**: depositar un aglutinante líquido sobre capas de polvo. Modelos como la **Z402** se hicieron conocidos por producir prototipos de manera rápida. En 1999, *Wired* describía la Z402 como una impresora capaz de producir modelos desde archivos CAD en minutos y como una alternativa mucho más rápida que otras tecnologías de prototipado de la época.

**Tipo de usuario de Z Corp:**

- diseño de producto;
- arquitectura;
- calzado;
- automotriz;
- laboratorios de visualización;
- empresas que necesitaban modelos físicos rápidos y visuales.

**Uso principal:**

- modelos de presentación;
- geometrías conceptuales;
- maquetas;
- prototipos de comunicación;
- modelos a color en generaciones posteriores.

La importancia de Z Corp fue cultural y tecnológica: acercó la impresión 3D a la idea de "imprimir modelos" de manera más parecida a una impresora convencional, aunque seguía siendo una solución profesional.

## 5. 2002: Stratasys Dimension y la reducción del costo profesional

Un salto relevante ocurrió en 2002 con la familia **Dimension** de Stratasys. La compañía presentó la **Dimension 3D Printer** a un precio de introducción de **29,900 USD**. Aunque hoy sigue pareciendo alto, en su momento fue importante porque bajó la barrera para diseñadores profesionales. Stratasys la presentó como una máquina confiable, compacta y relativamente simple de usar, aproximadamente a la mitad del costo de la siguiente impresora 3D de menor precio en ese momento.

El valor de Dimension fue acercar FDM a oficinas de ingeniería y diseño que no podían adquirir una plataforma industrial de cientos de miles de dólares.

**Usuarios típicos:**

- oficinas de diseño mecánico;
- departamentos de ingeniería;
- universidades;
- laboratorios de producto;
- empresas medianas con necesidad de prototipado interno.

**Para qué se usaba:**

- modelos de validación;
- pruebas de ensamble;
- prototipos en ABS;
- herramientas simples;
- revisión de interferencias;
- comunicación con clientes.

Modelos posteriores como **Dimension 1200es** ofrecían volúmenes de construcción de aproximadamente **254 × 254 × 305 mm**, con cartuchos de material ABS y soporte soluble. Esta etapa profesionalizó la impresión 3D como equipo de oficina técnica, aunque todavía no la convirtió en herramienta de bajo costo para FabLabs.

## 6. 2004–2008: RepRap y el cambio de paradigma

El cambio más importante para la democratización de la impresión 3D no vino de una gran empresa industrial, sino de una idea universitaria y abierta: **RepRap**.

El proyecto **RepRap** fue iniciado por **Adrian Bowyer** en la Universidad de Bath con el propósito de crear una impresora 3D de bajo costo, abierta y capaz de fabricar una parte significativa de sus propios componentes. RepRap no era solamente una máquina: era una propuesta de fabricación distribuida.

La idea central era radical para la época:

```text
Si una impresora puede fabricar muchas de sus propias piezas,
entonces otras personas pueden construir nuevas impresoras,
modificarlas, mejorarlas y compartirlas.
```

En 2008, el modelo **RepRap Darwin** alcanzó un hito simbólico: una máquina RepRap imprimió las piezas plásticas necesarias para construir otra máquina funcional. El Science Museum Group describe a Darwin como la primera impresora 3D autorreplicante RepRap y señala que los diseños y software eran open source, libres para descargarse y usarse.

### 6.1 Qué cambió con RepRap

RepRap cambió tres cosas al mismo tiempo:

1. **El costo**: muchas piezas podían imprimirse o conseguirse en ferreterías, tiendas de electrónica o proveedores comunes.
2. **El conocimiento**: los planos, firmware y documentación se compartían.
3. **La cultura**: los usuarios dejaron de ser solamente compradores y se volvieron constructores, modificadores y documentadores.

Esto fue fundamental para los FabLabs. Una impresora 3D dejó de ser una caja cerrada y se convirtió en un sistema que podía entenderse: motores paso a paso, varillas, correas, hotend, firmware, electrónica, G-code, calibración, extrusión y materiales.

**Costos aproximados de entrada en la etapa RepRap:**  
Mientras una impresora profesional podía costar decenas de miles de dólares, algunos proyectos y kits inspirados en RepRap comenzaron a prometer impresoras de cientos de dólares. En reportes de la época se hablaba de RepRap como una máquina construible por debajo de **400 USD**, aunque el costo real dependía fuertemente de disponibilidad de piezas, electrónica, herramientas, calidad de componentes y experiencia del usuario.

### 6.2 Por qué RepRap pudo avanzar aunque existían patentes FDM

Una pregunta importante es cómo pudo avanzar RepRap si **Stratasys** tenía protegida la tecnología FDM. La respuesta no está en una sola causa, sino en la combinación de tiempo, alcance, lenguaje técnico, mercado objetivo y diseño abierto.

Stratasys no compró originalmente FDM: la tecnología fue desarrollada por **Scott Crump**, cofundador de la empresa. La patente clave, **[US5121329A](https://patents.google.com/patent/US5121329A/en)**, titulada *Apparatus and method for creating three-dimensional objects*, fue solicitada en 1989 y concedida en 1992. Esa patente protegía el principio de crear objetos tridimensionales mediante deposición controlada de material, capa por capa. Durante los años noventa y buena parte de los dos mil, esto mantuvo la extrusión de termoplástico dentro de un mercado industrial dominado por Stratasys.

RepRap comenzó en 2005, cuando la patente base de FDM estaba cerca de expirar. Además, RepRap no nació como una empresa que vendía impresoras comerciales a departamentos de ingeniería, sino como un **proyecto académico, experimental y abierto**. Su objetivo era explorar una impresora de bajo costo, parcialmente autorreplicable y documentada públicamente. Esto redujo el riesgo de conflicto directo porque el proyecto no competía inicialmente con el negocio industrial de Stratasys.

También fue importante el uso del término **FFF** (*Fused Filament Fabrication*) en lugar de **FDM**. FDM estaba asociado a Stratasys como denominación comercial; FFF se volvió el término genérico usado por la comunidad abierta para describir impresoras que extruyen filamento fundido sin utilizar la marca comercial de Stratasys. Por eso, en muchos documentos de código abierto, educación y cultura maker se habla de FFF cuando técnicamente el principio de fabricación se parece al FDM industrial.

Las máquinas RepRap tampoco eran copias directas de equipos Stratasys. Las impresoras industriales usaban cámaras, materiales propietarios, sistemas de soporte, control térmico, software y servicios profesionales. Las RepRap usaban varillas, motores paso a paso, electrónica de bajo costo, firmware abierto, hotends simples, piezas imprimibles y materiales genéricos. Eran más limitadas, pero también más comprensibles, reparables y modificables.

La diferencia de mercado fue igual de importante. Stratasys vendía confiabilidad industrial; RepRap promovía acceso, aprendizaje y fabricación distribuida. Uno vendía soluciones profesionales cerradas; el otro construía una comunidad técnica abierta. En esa primera etapa no estaban atendiendo al mismo usuario ni al mismo nivel de exigencia.

Este contexto muestra que la democratización de la impresión 3D no ocurrió porque las patentes dejaran de importar. Ocurrió porque el principio básico empezó a salir de su periodo fuerte de protección, porque la comunidad creó arquitecturas alternativas y porque el nuevo mercado de escritorio no era todavía una amenaza directa para los equipos industriales.

Para consulta directa, las patentes principales relacionadas con este tramo histórico pueden revisarse en Google Patents:

| Patente | Tecnología / tema | Relevancia histórica |
|---|---|---|
| **[US4575330A](https://patents.google.com/patent/US4575330A/en)** | Estereolitografía, Chuck Hull / 3D Systems | Base de SLA y de la primera etapa comercial de impresión 3D. |
| **[US4863538A](https://patents.google.com/patent/US4863538A/en)** | Sinterizado selectivo por láser | Patente representativa del uso de láser para sinterizar capas de polvo. |
| **[US5121329A](https://patents.google.com/patent/US5121329A/en)** | FDM, Scott Crump / Stratasys | Patente base que protegió el principio de deposición de material capa por capa. |
| **[US6722872B1](https://patents.google.com/patent/US6722872B1/en)** | Cámara calentada / modelado a alta temperatura | Ejemplo de patente periférica posterior: no protege el concepto básico de FDM, sino mejoras industriales específicas del sistema. |


<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> RepRap Darwin, Mendel y Prusa Mendel como evolución visual. Archivo sugerido: <code>assets/img/historia/reprap-evolucion.png</code>.
</div>

## 7. 2009–2012: MakerBot, Thingiverse y el nacimiento de la impresora 3D de escritorio popular

En 2009 apareció **MakerBot Industries**, fundada por Bre Pettis, Adam Mayer y Zach Smith. MakerBot es importante porque tradujo parte del espíritu RepRap hacia productos que más personas podían comprar como kit.

### 7.1 MakerBot Cupcake CNC

La **MakerBot Cupcake CNC** fue una de las primeras impresoras 3D de escritorio ampliamente visibles para la comunidad maker. Era un kit, requería ensamblaje y ajustes, pero puso la impresión 3D al alcance de usuarios fuera de grandes empresas.

**Datos históricos destacados:**

- Año: 2009.
- Precio reportado: alrededor de **750 USD** en kit.
- Volumen aproximado de impresión reportado: cercano a **4 × 4 × 6 pulgadas**.
- Materiales: principalmente ABS y otros termoplásticos experimentales.
- Usuario objetivo: makers, artistas tecnológicos, diseñadores, ingenieros curiosos, hackerspaces, usuarios DIY.

*Wired* reportó en 2009 que MakerBot vendía kits de 750 USD, que ya había enviado más de 200 unidades y que sus usuarios podían imprimir objetos de plástico con un volumen de aproximadamente 4 × 4 × 6 pulgadas. Ese dato ilustra muy bien el cambio: de máquinas de 30,000–300,000 USD a kits de menos de 1,000 USD, aunque con más trabajo manual, menor confiabilidad y mayor necesidad de aprendizaje.

### 7.2 Thingiverse

MakerBot también impulsó **Thingiverse**, una plataforma para compartir archivos imprimibles. Esto fue tan importante como la máquina. Una impresora 3D sin modelos es una herramienta incompleta; un repositorio abierto reduce la barrera de entrada porque permite iniciar desde piezas existentes.

Thingiverse ayudó a consolidar tres prácticas que siguen vigentes:

- descargar modelos;
- modificar diseños;
- compartir remixes;
- aprender de comentarios, fallas y fotografías de otros usuarios.

En un FabLab, esta idea es central: la fabricación digital no solo depende de máquinas, sino de comunidades de archivos, documentación y aprendizaje colectivo.

### 7.3 MakerBot Thing-O-Matic

En 2010 apareció la **MakerBot Thing-O-Matic**, también como kit. Su precio de lanzamiento se reportó alrededor de **1,225 USD**. Una de sus ideas llamativas fue la plataforma de construcción automatizada, que prometía retirar piezas e imprimir trabajos consecutivos.

**Usuarios típicos:**

- hackerspaces;
- artistas;
- diseñadores;
- escuelas experimentales;
- laboratorios universitarios;
- comunidades DIY.

**Limitaciones:**

- requería calibración;
- calidad variable;
- software menos maduro;
- electrónica y mecánica sensibles;
- mucho aprendizaje por prueba y error.

Aun así, estas máquinas fueron decisivas porque crearon una generación de usuarios que aprendieron impresión 3D desde la máquina misma.

### 7.4 MakerBot, la expiración de la patente base y el giro comercial

MakerBot apareció en un momento histórico muy preciso. La patente principal de FDM de Stratasys fue solicitada en 1989, por lo que su vigencia práctica terminó alrededor de **2009**. Ese mismo año MakerBot lanzó la Cupcake CNC. La coincidencia no es menor: la expiración de la patente base abrió una ventana para que empresas de escritorio pudieran comercializar impresoras de extrusión de filamento sin enfrentar el mismo bloqueo jurídico que habría existido años antes.

Esto no significaba que todo el campo quedara libre. Stratasys y otras empresas conservaban patentes periféricas relacionadas con cámaras calentadas, cartuchos, materiales, soportes, cabezales, control térmico, trayectorias y otros detalles del sistema. Por eso las máquinas abiertas tomaron otro camino: marcos sencillos, camas calientes de bajo costo, materiales genéricos, firmware comunitario, electrónica accesible y soluciones mecánicas más simples.

MakerBot inició con una identidad cercana a RepRap: kits, documentación, comunidad y cultura abierta. Sin embargo, al crecer, la empresa empezó a moverse hacia productos más cerrados y orientados a consumidores, educación y oficinas. Ese giro produjo tensiones con parte de la comunidad maker, porque muchos usuarios habían participado bajo expectativas de apertura, modificación y reciprocidad.

En 2013, **Stratasys adquirió MakerBot**. Históricamente, este hecho es muy significativo: una compañía nacida de la cultura open source y del entusiasmo maker terminó integrada a la empresa que había construido el negocio industrial de FDM. La adquisición mostró dos cosas al mismo tiempo. Primero, que la impresión 3D de escritorio ya era un mercado suficientemente importante para las empresas industriales. Segundo, que el movimiento abierto había demostrado una ruta de acceso que las compañías tradicionales no habían desarrollado por sí solas.

La historia de MakerBot también sirve como advertencia para los FabLabs. Abrir una tecnología no solo significa vender máquinas más baratas. Implica sostener documentación, reparabilidad, comunidad, archivos, aprendizaje y posibilidad de modificación. Cuando una plataforma se cierra demasiado, puede ganar facilidad de uso, pero pierde parte del valor educativo que la hizo interesante.

## 8. 2010–2014: Prusa, Ultimaker, Printrbot y la explosión de diseños abiertos

Entre 2010 y 2014 el ecosistema de escritorio se multiplicó. No existía todavía una "impresora estándar", sino muchas variaciones basadas en ideas RepRap.

### 8.1 Prusa Mendel y Prusa i3

Josef Průša desarrolló variantes RepRap que simplificaron el diseño de impresoras FDM. La familia **Prusa Mendel** y después la **Prusa i3** fueron decisivas porque redujeron complejidad, facilitaron el ensamblaje y se volvieron ampliamente clonables.

La **Prusa i3**, publicada alrededor de 2012, se convirtió en una de las arquitecturas más influyentes de la impresión 3D FDM de escritorio: cama móvil, marco relativamente simple, componentes accesibles, electrónica abierta y una comunidad enorme. Muchos modelos económicos actuales derivan, directa o indirectamente, de esa arquitectura.

**Por qué fue importante:**

- diseño abierto;
- fácil de entender;
- fácil de modificar;
- compatible con componentes comunes;
- buena plataforma educativa;
- base para clones y mejoras.

### 8.2 Ultimaker

**Ultimaker**, nacida en Países Bajos, llevó el enfoque open source hacia una máquina de escritorio más pulida. La **Ultimaker Original**, lanzada en 2011 como kit, ofrecía un volumen de construcción aproximado de **210 × 210 × 205 mm** y se hizo conocida por velocidad, precisión y un ecosistema de software que después se consolidaría con Cura.

La **Ultimaker 2**, de 2013, se orientó a usuarios más profesionales: diseñadores, escuelas, bibliotecas, pequeñas empresas e ingenieros. Reportes de la época mencionan velocidades de 30–300 mm/s, resoluciones de capa de hasta 20 micras y volumen cercano a **225 × 225 × 205 mm**.

### 8.3 Printrbot, Portabee y otros equipos de bajo costo

En 2012 también aparecieron equipos aún más baratos y portátiles. *Wired* reportó modelos como **Printrbot Jr** en torno a **399 USD** y **Portabee** desde **480 USD** sin ensamblar. Aunque eran limitados y requerían conocimientos, mostraban que el mercado ya se había movido: una impresora 3D podía ser comprada por estudiantes avanzados, profesores, talleres comunitarios y makers.

### 8.4 Caducidad de patentes y efecto en precios

El abaratamiento no se explica por una sola causa. Ocurrió por combinación de:

- diseños RepRap abiertos;
- componentes de bajo costo;
- comunidades de firmware y slicers;
- documentación distribuida;
- disponibilidad de Arduino y electrónica económica;
- motores paso a paso y drivers accesibles;
- filamento comercial;
- caducidad o rodeo de patentes;
- competencia entre fabricantes.

Cuando las patentes de tecnologías clave fueron expirando, más empresas pudieron entrar. En FDM/FFF, el cambio fue especialmente visible: el mercado pasó de unos pocos fabricantes industriales a decenas de marcas de escritorio.

La diferencia entre la etapa industrial y la etapa abierta puede resumirse así:

| Aspecto | FDM industrial de Stratasys | FFF abierto / RepRap / primeras MakerBot |
|---|---|---|
| Mercado inicial | Empresas, ingeniería profesional, prototipado industrial | Makers, universidades, hackerspaces, FabLabs |
| Precio típico | Decenas o cientos de miles de USD | Cientos a pocos miles de USD |
| Materiales | Propietarios o controlados | Filamento genérico, experimentación comunitaria |
| Software | Cerrado o asociado a la máquina | Firmware y slicers abiertos o comunitarios |
| Mantenimiento | Servicio técnico profesional | Autorreparación, documentación y foros |
| Valor principal | Confiabilidad industrial | Acceso, aprendizaje, modificación y bajo costo |
| Riesgo técnico | Menor para el usuario final | Mayor calibración y aprendizaje |

Esta comparación explica por qué ambos mundos pudieron coexistir. El escritorio abierto no ofrecía la misma confiabilidad que un equipo industrial, pero permitía aprender, modificar y fabricar a una fracción del costo. Para la cultura FabLab, ese intercambio era aceptable e incluso valioso: la máquina no era una caja negra, sino un objeto técnico que podía estudiarse.

<div class="placeholder">
<strong>Espacio sugerido para tabla visual:</strong> comparación de costos aproximados: SLA-1, Stratasys Dimension, MakerBot Cupcake, Thing-O-Matic, Prusa i3, Ender 3, Bambu A1. Archivo sugerido: <code>assets/img/historia/costos-evolucion.png</code>.
</div>

## 9. 2012–2016: entusiasmo, burbuja de consumo y corrección del mercado

Entre 2012 y 2014 se habló mucho de una "revolución" donde cada hogar tendría una impresora 3D. Esa predicción fue exagerada. La impresión 3D se popularizó, pero no reemplazó a la manufactura tradicional ni convirtió cada casa en una fábrica.

El mercado tuvo una corrección importante:

- muchas personas compraron impresoras esperando facilidad inmediata;
- las máquinas requerían calibración;
- los materiales fallaban;
- el software aún era complejo;
- los modelos no siempre eran imprimibles;
- la calidad dependía del usuario.

MakerBot es un caso claro. Pasó de comunidad abierta y hackeable a buscar un mercado más masivo y cerrado. En 2013 fue adquirida por **Stratasys**. Después enfrentó problemas de calidad, expectativas demasiado altas, competencia creciente y una transición hacia educación y mercado profesional.

La lección histórica es importante para un FabLab: la impresión 3D no se democratiza solo vendiendo máquinas. Se democratiza cuando hay **acompañamiento, documentación, criterio de diseño, repositorios, materiales confiables y comunidades que enseñan a resolver fallas**.

## 10. 2014–2019: la impresora de escritorio madura

Después de la primera ola maker, el mercado maduró. Las impresoras se volvieron más confiables y fáciles de usar. Aparecieron o crecieron marcas que hoy siguen siendo relevantes:

- **Prusa Research**: confiabilidad, documentación, código abierto, comunidad técnica.
- **Ultimaker**: educación, diseño profesional, software Cura, perfiles de materiales.
- **Creality**: bajo costo, masificación de la arquitectura tipo i3, Ender 3.
- **Anycubic**: FDM y resina de bajo costo.
- **Formlabs**: SLA de escritorio profesional.
- **Raise3D**, **LulzBot**, **FlashForge**, **Zortrax**, entre otras: nichos educativos, profesionales o prosumer.

### 10.1 Formlabs y la resina de escritorio profesional

**Formlabs**, fundada en 2011, es relevante porque llevó la estereolitografía de escritorio a un público profesional más amplio. La **Form 1** fue financiada por Kickstarter en 2012 y abrió una ruta distinta a FDM: piezas de alta resolución, resina líquida, postcurado y aplicaciones en joyería, odontología, diseño de producto y prototipado visual.

A diferencia de FDM, donde el usuario podía modificar mucho la máquina, Formlabs apostó por un ecosistema más controlado: impresora, resinas, software y perfiles integrados. Este camino mostró que la democratización también podía ocurrir mediante máquinas más fáciles de operar, no solo mediante hardware abierto.

### 10.2 Creality Ender 3 y el bajo costo masivo

La familia **Ender 3** de Creality se volvió una referencia de entrada por precio. Aunque requiere ajustes y aprendizaje, ofreció un volumen útil, comunidad enorme y bajo costo. Modelos más recientes como **Ender-3 V3 SE** ofrecen volumen de construcción de **220 × 220 × 250 mm** y funciones que antes eran más avanzadas, como nivelación automática y velocidades más altas.

El impacto de Creality fue llevar la impresión FDM al usuario de bajo presupuesto: estudiantes, makers, escuelas con poco recurso, talleres domésticos y laboratorios que necesitaban varias máquinas económicas.

## 11. 2020: pandemia, fabricación distribuida y límites reales

La pandemia de COVID-19 mostró una cara importante de la impresión 3D: su capacidad para responder rápido cuando las cadenas de suministro tradicionales fallan. Makerspaces, universidades, empresas y usuarios fabricaron adaptadores, caretas, piezas para equipo médico no crítico, dispositivos de apoyo y prototipos.

Sin embargo, también se hicieron evidentes los límites:

- no toda pieza impresa es segura para uso médico;
- los materiales deben validarse;
- la esterilización importa;
- la repetibilidad no es automática;
- los diseños deben revisarse;
- la fabricación distribuida necesita coordinación y control de calidad.

La impresión 3D mostró su valor como herramienta de respuesta, prototipado y fabricación local, pero también confirmó que no basta con imprimir: hay que diseñar, validar y documentar.

## 12. 2020–2026: automatización, velocidad y ecosistemas integrados

La etapa actual está marcada por impresoras más rápidas, mejor calibradas y más fáciles de usar. La barrera ya no es solo el precio; ahora también importan la experiencia de usuario, el software, los sensores, los perfiles de materiales y la conectividad.

### 12.1 Prusa MK4S

La **Original Prusa MK4S** representa la continuidad del enfoque abierto y documentado. Es una impresora FDM de escritorio orientada a usuarios exigentes, educación, prototipado y laboratorios. La documentación de Prusa reporta para la familia MK4/S un volumen aproximado de **250 × 210 × 220 mm**.

**Fortalezas:**

- documentación sólida;
- comunidad;
- confiabilidad;
- reparabilidad;
- ecosistema abierto;
- perfiles de impresión maduros.

**Usuario típico:**

- universidades;
- laboratorios;
- makers avanzados;
- prototipado profesional;
- usuarios que valoran mantenimiento y documentación.

### 12.2 Bambu Lab A1 y la nueva etapa de facilidad de uso

**Bambu Lab** cambió el mercado reciente al combinar velocidad, calibración automática, ecosistema de software, conectividad y experiencia de usuario muy pulida. La **Bambu Lab A1**, que se usa como caso de estudio en este curso, tiene volumen de construcción de **256 × 256 × 256 mm**, hotend all-metal y extrusor con engranes endurecidos, según la ficha técnica del fabricante.

Su importancia no está solo en las especificaciones. Está en la experiencia:

- autocalibración;
- perfiles de material;
- integración con Bambu Studio;
- envío de archivos más directo;
- menor fricción para usuarios nuevos;
- opción de impresión multicolor con AMS Lite.

**Tipo de usuario:**

- educación;
- FabLabs;
- prototipado;
- usuarios de escritorio;
- talleres que necesitan resultados rápidos;
- personas que no quieren construir la máquina desde cero.

La A1 no reemplaza el conocimiento técnico, pero sí reduce el costo de entrada operativo. En un FabLab, eso permite que el tiempo se use más en diseño, iteración y discusión técnica, y menos en calibración inicial.

### 12.3 Formlabs Form 4 y resina profesional

En el campo de resina, **Formlabs Form 4** representa la madurez de la fotopolimerización de escritorio profesional. Formlabs reporta para la Form 4 un volumen de **20.0 × 12.5 × 21.0 cm**, y la orienta a materiales validados, alta resolución y ciclos rápidos de prototipado.

**Usuarios típicos:**

- odontología;
- joyería;
- diseño de producto;
- laboratorios;
- ingeniería;
- modelos de alta resolución.

### 12.4 SLS compacto y profesional

SLS sigue siendo menos común que FDM en espacios educativos básicos, pero también se ha compactado. 3D Systems anunció en 2023 la adquisición de **Wematter**, cuyo sistema **Gravity** buscaba llevar SLS a una forma más asequible y llave en mano. Esto muestra una tendencia: tecnologías que antes eran solo industriales empiezan a bajar de escala, aunque no necesariamente al nivel doméstico.

## 13. Comparación histórica de máquinas representativas

La siguiente tabla no pretende ser un catálogo completo. Funciona como mapa de transición: de equipos industriales a equipos de escritorio y FabLab.

| Periodo | Marca / modelo | Tecnología | Costo aproximado histórico | Capacidad / volumen reportado | Usuario típico | Aporte histórico |
|---|---|---:|---:|---:|---|---|
| 1988 | 3D Systems SLA-1 | SLA | 300,000–400,000 USD aprox. | Industrial, resina UV | R&D, automotriz, diseño industrial | Primera comercialización de impresión 3D |
| 1992 | Stratasys 3D Modeler | FDM | Industrial, alto costo | FDM con termoplásticos | Ingeniería, prototipado funcional | Introduce FDM comercial |
| 1990s | DTM Sinterstation | SLS | Industrial, alto costo | Polvo polimérico | Aeroespacial, automotriz, servicios | Piezas funcionales sin soportes tradicionales |
| 1999 | Z Corp Z402 | Binder jetting | Profesional | Modelos rápidos desde CAD | NASA, Adidas, diseño, arquitectura | Prototipado rápido visual y veloz |
| 2002 | Stratasys Dimension | FDM | 29,900 USD | Equipo de oficina técnica | Diseñadores, ingeniería, universidades | Reduce costo profesional de FDM |
| 2008 | RepRap Darwin | FFF abierto | Cientos de USD, variable | Autoconstrucción | Makers, universidades, hackerspaces | Hardware abierto y autorreplicación parcial |
| 2009 | MakerBot Cupcake CNC | FFF kit | 750 USD aprox. | 4 × 4 × 6 in aprox. | Makers, artistas, DIY | Primer gran símbolo de escritorio maker |
| 2010 | MakerBot Thing-O-Matic | FFF kit | 1,225 USD aprox. | Escritorio | Hackerspaces, diseño, arte | Automatización básica y comunidad |
| 2011 | Ultimaker Original | FFF kit | Kit prosumer | 210 × 210 × 205 mm aprox. | Makers avanzados, educación | Velocidad, precisión y ecosistema Cura |
| 2012 | Prusa i3 | FFF abierto | Variable, bajo costo | Depende de variante | Educación, makers, clones | Arquitectura abierta más influyente |
| 2018 en adelante | Creality Ender 3 | FFF | Bajo costo | 220 × 220 × 250 mm en variantes actuales | Estudiantes, makers, laboratorios | Masificación económica |
| 2024–2026 | Prusa MK4S | FFF | Prosumer/profesional | 250 × 210 × 220 mm | Educación, ingeniería, prototipado | Fiabilidad, comunidad, documentación |
| 2023–2026 | Bambu Lab A1 | FDM/FFF | Escritorio moderno | 256 × 256 × 256 mm | FabLabs, educación, prototipado | Automatización, velocidad, experiencia de usuario |
| 2024–2026 | Formlabs Form 4 | MSLA/LFD resin | Profesional escritorio | 200 × 125 × 210 mm | Dental, joyería, ingeniería | Resina profesional rápida y accesible |

## 14. Competidores y cambios de enfoque por etapas

### 14.1 1980s–1990s: pocos actores industriales

La competencia inicial estaba dominada por empresas especializadas:

- **3D Systems**: SLA, después SLS y otras tecnologías.
- **Stratasys**: FDM.
- **DTM**: SLS.
- **Z Corporation**: binder jetting para modelos rápidos.
- **EOS**: tecnologías de sinterizado y metal en Europa.
- **Objet**: material jetting y fotopolímeros.

Era un mercado de capital intensivo. La venta no era a individuos, sino a empresas, universidades y centros de desarrollo.

### 14.2 2000s: máquinas profesionales más compactas

Stratasys Dimension, Z Corp y otros equipos hicieron que algunas oficinas de ingeniería pudieran tener prototipado interno. El cliente ya no era solamente un gran laboratorio corporativo; también eran departamentos de diseño, escuelas técnicas y universidades.

### 14.3 2008–2013: explosión open source y DIY

Aquí entran:

- **RepRap**;
- **MakerBot**;
- **Prusa**;
- **Ultimaker**;
- **Printrbot**;
- **LulzBot**.

La diferencia central no era solo el precio. Era la posibilidad de modificar, reparar y entender la máquina. El usuario se volvió participante del desarrollo tecnológico.

### 14.4 2014–2019: profesionalización del escritorio

El mercado se dividió:

- bajo costo: Creality, Anycubic, clones i3;
- escritorio confiable: Prusa, Ultimaker;
- resina profesional: Formlabs;
- educación: MakerBot, Ultimaker, Prusa;
- industrial: Stratasys, 3D Systems, EOS, HP, GE Additive, Markforged.

### 14.5 2020–2026: automatización, velocidad y experiencia de usuario

El usuario actual espera que la impresora:

- calibre automáticamente;
- detecte filamento;
- tenga perfiles listos;
- imprima rápido;
- se conecte por red;
- use software amigable;
- permita monitoreo;
- produzca buenos resultados sin modificar firmware.

Marcas como **Bambu Lab** aceleraron esta expectativa. Prusa mantiene una cultura de confiabilidad y apertura. Creality compite por precio. Formlabs domina parte del escritorio profesional en resina. Stratasys, 3D Systems, EOS, HP y otras empresas siguen enfocadas en industria, producción, materiales certificados y aplicaciones de alto valor.

## 15. Qué significa democratizar la impresión 3D

Democratizar no significa que todo sea fácil ni que cualquier pieza sea imprimible sin criterio. Significa que más personas pueden participar en el ciclo de diseño-fabricación.

En el caso de FDM/FFF, la democratización dependió de una condición histórica muy concreta: el conocimiento técnico empezó a circular cuando la patente base dejó de bloquear el principio general, y la comunidad desarrolló soluciones alternativas para lo que seguía protegido o cerrado. RepRap y MakerBot no solo abarataron máquinas; cambiaron la relación del usuario con la tecnología. El usuario dejó de ser únicamente comprador de un equipo y pasó a ser constructor, reparador, diseñador, documentador y miembro de una comunidad de aprendizaje.

La democratización ocurrió por varias capas:

1. **Máquinas más baratas**: de cientos de miles de dólares a cientos de dólares.
2. **Diseños abiertos**: RepRap, Prusa y derivados.
3. **Software accesible**: Cura, PrusaSlicer, Slic3r, Tinkercad, FreeCAD, Blender.
4. **Repositorios**: Thingiverse, Printables, MakerWorld, NIH 3D.
5. **Materiales disponibles**: PLA, PETG, TPU y resinas comerciales.
6. **Comunidades**: foros, videos, documentación, perfiles compartidos.
7. **Automatización**: sensores, autocalibración, perfiles de materiales.

En un FabLab, esta historia se vuelve práctica. La impresora 3D no es solo una máquina que deposita plástico: es una puerta de entrada para entender materiales, geometría, tolerancias, mecanismos, electrónica, ergonomía y fabricación local.

## 16. Dónde estamos hoy

Hoy la impresión 3D no reemplaza a la producción masiva, pero sí ocupa un espacio cada vez más sólido:

- prototipado rápido;
- educación STEM;
- fabricación personalizada;
- piezas de bajo volumen;
- herramentales;
- jigs y fixtures;
- órtesis y dispositivos adaptados;
- odontología;
- joyería;
- modelos anatómicos;
- moldes;
- robótica educativa;
- reparación y adaptación de objetos;
- producción distribuida en situaciones específicas.

La etapa actual puede resumirse así:

```text
Antes: imprimir era difícil, caro y especializado.
Después: imprimir fue posible para makers, pero exigía mucha calibración.
Hoy: imprimir es más accesible, rápido y automático, pero diseñar bien sigue siendo el verdadero reto.
```

La impresión 3D se volvió interesante no porque todas las personas vayan a fabricar todo en casa, sino porque permite que más personas pasen de una idea a un objeto físico. Esa transición —idea, modelo, archivo, laminado, impresión, revisión— es una de las experiencias más potentes que puede ofrecer un FabLab.

## Referencias

[1] 3D Systems, “Our Story.”  
[2] 3D Systems, “Stereolithography.”  
[3] Charles W. Hull, **[US Patent US4575330A](https://patents.google.com/patent/US4575330A/en)**, “Apparatus for production of three-dimensional objects by stereolithography.”  
[4] Stratasys, **[US Patent US5121329A](https://patents.google.com/patent/US5121329A/en)**, “Apparatus and method for creating three-dimensional objects.”  
[5] Prusa Knowledge Base, “FFF/FDM.”  
[6] UltiMaker, “FDM vs FFF: Understanding 3D printing technologies.”  
[7] MakerBot, “History of 3D Printing.”  
[8] Stratasys, “Stratasys Celebrates 10-Year Anniversary of Industry's First Office 3D Printer.”  
[9] Stratasys Support, “Dimension Family 3D Printers Support.”  
[10] Science Museum Group, “Darwin RepRap self-replicating 3D printer.”  
[11] RepRap Project, “About RepRap.”  
[12] Wired, “3-D Printers Make Manufacturing Accessible.”  
[13] Wired, “Shapeways interviews MakerBot.”  
[14] Wired, “Portable and Affordable: New 3-D Printers That Cost Less Than $500.”  
[15] University of Texas at Austin, “Selective Laser Sintering, From a Texas Idea to a Global Industry”; Carl Deckard, **[US Patent US4863538A](https://patents.google.com/patent/US4863538A/en)**, “Method and apparatus for producing parts by selective sintering.”  
[16] 3D Systems, “Reinventing Metal Additive Technology.”  
[17] Formlabs, “Form 4 vs. Form 3/+.”  
[18] Prusa Knowledge Base, “FAQ - Frequently Asked Questions.”  
[19] Bambu Lab, “A1 Tech Specs.”  
[20] Stratasys, **[US Patent US6722872B1](https://patents.google.com/patent/US6722872B1/en)**, “High temperature modeling apparatus.”  
[20] Creality, “Ender-3 V3 SE.”  
[21] MakerWorld, Thingiverse, Printables y otros repositorios comunitarios de modelos 3D.

## Siguiente sección

[Tecnologías de impresión 3D](tecnologias.md)
