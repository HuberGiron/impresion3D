---
layout: default
title: Tecnologías
nav_order: 4
---

# Tecnologías de impresión 3D

La impresión 3D no es una sola tecnología. Es una familia de procesos que comparten una idea general —fabricar desde un modelo digital agregando material— pero lo hacen con materiales, mecanismos y niveles de complejidad muy diferentes.

En un FabLab, la tecnología más común suele ser la impresión por filamento fundido, conocida como **FDM** o **FFF**. Sin embargo, para comprender el campo completo conviene conocer también tecnologías de resina, sinterizado de polvo y procesos industriales más avanzados.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> árbol de clasificación de tecnologías de impresión 3D. Archivo sugerido: <code>assets/img/tecnologias/clasificacion-tecnologias.png</code>.
</div>

## 1. Familias principales de manufactura aditiva

Las tecnologías de impresión 3D pueden agruparse por la forma en que agregan o solidifican material. Algunas depositan material fundido, otras curan resinas con luz, otras fusionan polvo y otras inyectan material o aglutinante.

Las familias más relevantes para un curso introductorio son:

- **Extrusión de material:** deposita material a través de una boquilla.
- **Fotopolimerización en cuba:** solidifica resina líquida mediante luz.
- **Fusión de cama de polvo:** fusiona o sinteriza polvo con energía térmica.
- **Inyección de material:** deposita gotas de material que solidifican.
- **Inyección de aglutinante:** une polvo usando un agente adhesivo.
- **Deposición directa de energía:** deposita y funde material, comúnmente metálico.

No todas estas tecnologías son comunes en un FabLab, pero conocerlas permite ubicar qué puede hacer una impresora de escritorio y qué pertenece a procesos industriales.

## 2. FDM / FFF: extrusión de filamento

**FDM** significa *Fused Deposition Modeling*. **FFF** significa *Fused Filament Fabrication*. En la práctica, ambos términos se utilizan para describir impresoras que funden un filamento termoplástico y lo depositan capa por capa.

Stratasys describe FDM como un proceso de fabricación de objetos físicos mediante capas sucesivas de material con filamento termoplástico extruido. En el entorno maker y educativo se usa mucho el término FFF porque evita asociar el proceso exclusivamente con una marca o denominación comercial.

### Ventajas

- Bajo costo de entrada.
- Materiales accesibles.
- Mantenimiento razonable.
- Buena visibilidad del proceso.
- Ideal para educación, prototipado y piezas funcionales sencillas.

### Limitaciones

- Líneas de capa visibles.
- Resistencia dependiente de la orientación.
- Soportes necesarios en algunas geometrías.
- Precisión limitada por máquina, material y calibración.
- Acabado superficial inferior al de resina.

## 3. SLA, DLP y MSLA: impresión con resina

Las tecnologías de resina utilizan un fotopolímero líquido que se solidifica al recibir luz. Dependiendo del sistema, la luz puede provenir de un láser, un proyector o una pantalla LCD con iluminación UV.

### SLA

En SLA, un láser cura selectivamente la resina. Suele asociarse con buena precisión y superficies finas.

### DLP

En DLP, un proyector ilumina una capa completa o zonas amplias de la resina. Puede ser rápido y preciso.

### MSLA / LCD

En MSLA, una pantalla LCD enmascara la luz UV para curar la resina por capas. Es común en impresoras de resina de escritorio.

### Ventajas

- Alta resolución.
- Buen detalle fino.
- Superficies más lisas que FDM.
- Excelente para miniaturas, moldes, piezas dentales, joyería y modelos visuales.

### Limitaciones

- Manejo químico de resinas.
- Necesidad de lavado y curado posterior.
- Mayor cuidado de seguridad.
- Resinas estándar pueden ser frágiles.
- Residuos y solventes requieren manejo responsable.

<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> comparación visual entre pieza FDM y pieza de resina. Archivo sugerido: <code>assets/img/tecnologias/fdm-vs-resina.jpg</code>.
</div>

## 4. SLS: sinterizado selectivo por láser

**SLS** significa *Selective Laser Sintering*. En este proceso, una capa de polvo —normalmente nylon o polímeros similares— se extiende sobre una cama y un láser sinteriza las zonas que forman la pieza.

Una característica importante de SLS es que el polvo no sinterizado rodea la pieza y actúa como soporte. Por eso permite geometrías complejas sin los soportes tradicionales de FDM o resina.

### Ventajas

- Buenas propiedades mecánicas.
- Geometrías complejas.
- No requiere soportes convencionales.
- Adecuado para piezas funcionales.
- Permite fabricar varios objetos dentro del mismo volumen de polvo.

### Limitaciones

- Equipo más costoso.
- Manejo de polvo.
- Limpieza posterior.
- Menor accesibilidad para usuarios principiantes.
- Requiere mayor control del proceso.

## 5. MJF: Multi Jet Fusion

**Multi Jet Fusion** es una tecnología desarrollada por HP que usa agentes sobre una cama de polvo y energía térmica para formar piezas. Se ubica en aplicaciones productivas de bajo y mediano volumen, especialmente con polímeros como PA12.

Aunque no suele estar presente en FabLabs pequeños, es importante mencionarla porque representa una alternativa industrial para series cortas y piezas funcionales.

## 6. Impresión 3D metálica

La impresión 3D metálica incluye procesos como:

- **DMLS:** Direct Metal Laser Sintering.
- **SLM:** Selective Laser Melting.
- **EBM:** Electron Beam Melting.
- **DED:** Directed Energy Deposition.
- **Binder Jetting metálico.**

Estas tecnologías permiten fabricar piezas metálicas complejas para sectores como aeroespacial, biomédico, automotriz y herramientas industriales. Sin embargo, requieren equipos costosos, atmósferas controladas, polvos metálicos, seguridad avanzada y postprocesos térmicos o mecánicos.

Para un curso de FabLab, lo importante es que el lector comprenda que la impresión 3D no se limita al plástico, pero que la operación de metales pertenece a otra escala técnica, económica y de seguridad.

## 7. Comparación general de tecnologías

| Tecnología | Material típico | Nivel de acceso | Calidad visual | Resistencia funcional | Uso común |
|---|---|---:|---:|---:|---|
| FDM / FFF | Filamento termoplástico | Alto | Media | Media | FabLabs, educación, prototipado |
| SLA / DLP / MSLA | Resina fotopolimérica | Medio | Alta | Variable | Miniaturas, dental, joyería, detalle |
| SLS | Polvo polimérico | Bajo-medio | Media-alta | Alta | Piezas funcionales complejas |
| MJF | Polvo polimérico | Bajo | Media-alta | Alta | Series cortas industriales |
| Metal AM | Polvo o hilo metálico | Bajo | Alta | Alta | Aeroespacial, médico, industria avanzada |

## 8. Qué tecnología conviene para cada caso

| Necesidad | Tecnología recomendada | Razón |
|---|---|---|
| Aprender impresión 3D en un FabLab | FDM / FFF | Accesible, visible y económica |
| Prototipo de carcasa o soporte | FDM / FFF | Permite iterar rápido |
| Miniatura con mucho detalle | Resina | Mayor resolución superficial |
| Pieza mecánica compleja sin soportes | SLS | El polvo actúa como soporte |
| Serie corta de piezas funcionales | SLS o MJF | Mejor repetibilidad que FDM en producción corta |
| Implante o pieza metálica avanzada | Metal AM | Permite geometrías metálicas complejas |

## 9. Por qué FDM será el eje del curso

El resto del manual se centrará principalmente en FDM / FFF porque es la tecnología más común en espacios educativos y FabLabs. Es la más apropiada para introducir conceptos de material, laminado, orientación, soportes, tolerancias y diagnóstico de fallas.

FDM permite ver el proceso físicamente: la máquina calienta filamento, lo empuja por una boquilla, lo deposita sobre una superficie y construye el objeto. Esa visibilidad tiene un valor pedagógico enorme. El usuario puede observar la relación entre parámetros digitales y comportamiento material en tiempo real.

## Referencias

[1] Stratasys, “FDM 3D Printing – Fused Deposition Modeling.”  
[2] NIOSH, “A Guide for Makerspace Users, Schools, Libraries and Small Businesses.”  
[3] ISO, “ISO/ASTM 52900.”

## Siguiente sección

[Tecnología FDM / FFF](tecnologia-fdm.md)
