---
layout: default
title: Tecnologías
nav_order: 4
---

# Tecnologías de impresión 3D

La impresión 3D no es una sola máquina ni una sola forma de fabricar. Es una familia de procesos que convierten un modelo digital en una pieza física mediante la adición, solidificación o fusión controlada de material.

En un FabLab, la tecnología más importante para comenzar es **FDM / FFF**, porque combina bajo costo, materiales accesibles, mantenimiento razonable, observación directa del proceso y una curva de aprendizaje adecuada para educación, prototipado, proyectos STEM, robótica, electrónica, diseño de producto y fabricación personalizada.

Por esa razón, este capítulo inicia con FDM con mayor profundidad. Después se revisan otras tecnologías —resina, SLS, MJF y metal— no como catálogo superficial, sino como comparación técnica: cómo funcionan, qué hacen mejor que FDM, qué hacen peor, cuánto cuestan aproximadamente, qué equipos existen hoy y en qué tipo de entorno tiene sentido usarlas.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> mapa conceptual de tecnologías de impresión 3D, colocando FDM/FFF al centro como tecnología FabLab y las demás como tecnologías complementarias. Archivo sugerido: <code>assets/img/tecnologias/mapa-tecnologias-impresion-3d.png</code>.
</div>

---

## 1. La idea central: del material al objeto físico

Todas las tecnologías de impresión 3D comparten una lógica general:

```text
Modelo digital → División en capas → Construcción física → Pieza terminada
```

La diferencia está en **qué material se usa** y **cómo se solidifica**:

| Familia tecnológica | Material inicial | Cómo se forma la pieza |
|---|---|---|
| FDM / FFF | Filamento termoplástico | Se funde y se deposita por una boquilla |
| SLA / DLP / MSLA | Resina líquida fotosensible | Se cura con luz, láser, proyector o pantalla UV |
| SLS | Polvo polimérico | Se sinteriza con láser |
| MJF | Polvo polimérico | Se aplican agentes y energía térmica |
| Metal AM | Polvo o hilo metálico | Se fusiona con láser, haz de electrones, arco o energía dirigida |
| Binder Jetting | Polvo + aglutinante | Se une el polvo con un agente líquido y luego se postprocesa |
| Material Jetting | Gotas de fotopolímero | Se depositan gotas y se curan con luz |

Para el usuario de FabLab, esta clasificación sirve para tomar decisiones. No se elige una impresora 3D solamente por marca o precio; se elige según **material, resolución, resistencia, tamaño de pieza, seguridad, costo de operación, postprocesado y tipo de aplicación**.

---

# Parte I. FDM / FFF: la tecnología principal de FabLabs

## 2. Qué es FDM / FFF

**FDM** significa *Fused Deposition Modeling*. **FFF** significa *Fused Filament Fabrication*. En la práctica, ambos términos se usan para describir impresoras que toman un filamento termoplástico, lo calientan y lo depositan capa por capa.

El término **FDM** está históricamente asociado a Stratasys. En el entorno abierto, maker y educativo se volvió común usar **FFF** para referirse al mismo principio general sin usar una denominación comercial. En este curso se usarán ambos términos porque en la práctica aparecen de forma intercambiable en manuales, catálogos, software y literatura técnica.

FDM es la tecnología más común en FabLabs porque permite ver el proceso: el usuario observa cómo una trayectoria digital se convierte en una pared, cómo se genera el relleno, cómo se forman los soportes y cómo una mala orientación puede afectar la resistencia.

<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> diagrama de una impresora FDM con filamento, extrusor, hotend, boquilla, cama y pieza por capas. Archivo sugerido: <code>assets/img/tecnologias/fdm-partes-principales.png</code>.
</div>

---

## 3. Principio de funcionamiento de FDM

Una impresora FDM construye la pieza depositando material fundido. El flujo básico es:

```text
Filamento → Extrusor → Hotend → Boquilla → Capa depositada → Pieza completa
```

El filamento, normalmente de **1.75 mm**, entra al extrusor. El extrusor lo empuja hacia el hotend. El hotend lo calienta hasta que fluye. La boquilla deposita el material en una trayectoria definida por el software. Cuando una capa termina, la máquina sube o baja en el eje Z y deposita la siguiente capa.

La pieza final no es un bloque homogéneo. Está formada por paredes, capas, relleno, soportes y pequeñas discontinuidades propias del proceso.

---

## 4. Partes principales de una impresora FDM

### 4.1 Chasis

El chasis sostiene la máquina. Puede estar fabricado en aluminio extruido, acero, acrílico, madera en modelos antiguos o combinaciones de materiales. Una estructura rígida reduce vibraciones, mejora la repetibilidad y permite mantener la geometría de impresión.

Una impresora con chasis flexible puede producir capas desplazadas, superficies con ondas, vibración visible o piezas con dimensiones inconsistentes.

### 4.2 Sistema de movimiento

El sistema de movimiento posiciona la boquilla y la cama. Los diseños más comunes son:

| Arquitectura | Descripción | Ventajas | Limitaciones |
|---|---|---|---|
| Cartesiana con cama móvil | La cama se mueve en un eje y el cabezal en otro | Simple, económica, común | En piezas altas, el movimiento de la cama puede afectar estabilidad |
| CoreXY | El cabezal se mueve en X/Y con un sistema de bandas | Rápida, rígida, buena para impresoras cerradas | Ensamble y mantenimiento más complejos |
| Delta | Tres torres coordinan el efector | Movimiento rápido, estética compacta | Calibración menos intuitiva |
| Cantilever | Un brazo sostiene el eje X | Compacta y económica | Menor rigidez en algunos modelos |

En equipos modernos, además de la mecánica, importan los algoritmos de compensación de vibración, nivelación automática, sensores de carga y control de flujo.

### 4.3 Extrusor

El extrusor empuja el filamento. Usa engranes o ruedas moleteadas para controlar el avance del material.

Existen dos configuraciones principales:

| Tipo | Descripción | Ventajas | Limitaciones |
|---|---|---|---|
| Direct drive | El extrusor está cerca del hotend | Mejor para TPU y materiales flexibles; retracción más corta | Aumenta la masa del cabezal |
| Bowden | El extrusor está separado y empuja por un tubo | Cabezal más ligero | Materiales flexibles y retracción pueden ser más difíciles |

En impresoras actuales de escritorio se ha vuelto muy común el **direct drive**, especialmente porque mejora la experiencia con TPU y reduce ajustes complicados de retracción.

### 4.4 Hotend

El hotend funde el material. Incluye bloque calefactor, termistor, cartucho calefactor, disipador, garganta térmica y boquilla.

Un hotend moderno puede llegar a temperaturas entre **260 °C y 300 °C** en impresoras de escritorio comunes. Modelos más técnicos pueden superar ese rango para materiales de ingeniería.

### 4.5 Boquilla

La boquilla define el diámetro de salida. La más común es **0.4 mm**.

| Boquilla | Uso típico |
|---|---|
| 0.2 mm | Detalle fino, piezas pequeñas, más tiempo |
| 0.4 mm | Uso general, equilibrio entre calidad y velocidad |
| 0.6 mm | Piezas funcionales, mejor flujo, menos tiempo |
| 0.8 mm o más | Piezas grandes, capas gruesas, menor detalle |

Si se imprimen materiales abrasivos, como fibra de carbono, fibra de vidrio o filamentos con partículas, conviene usar boquilla endurecida.

### 4.6 Cama de impresión

La cama sostiene la pieza durante la fabricación. Puede ser de vidrio, acero flexible con PEI, superficies texturizadas, placas magnéticas u otras variantes. La cama caliente ayuda a mejorar adhesión y reducir deformaciones.

La **primera capa** es crítica. Si la primera capa falla, la impresión completa queda comprometida.

### 4.7 Ventiladores

Una impresora FDM suele tener ventilador de hotend y ventilador de pieza. El primero protege la zona fría del hotend. El segundo controla el enfriamiento del material depositado.

PLA suele beneficiarse de mayor ventilación. ABS y ASA suelen requerir menos ventilación y un ambiente térmicamente más estable.

### 4.8 Sensores y automatización

Las impresoras actuales pueden incluir:

- nivelación automática;
- sensor de filamento;
- sensor de corte o atasco;
- acelerómetros;
- cámara;
- detección de spaghetti;
- compensación de flujo;
- calibración de resonancia;
- perfiles preconfigurados;
- conectividad Wi-Fi o nube.

Estos elementos reducen la barrera de entrada. Sin embargo, una máquina automática no elimina la necesidad de comprender material, orientación, soportes y tolerancias.

---

## 5. Anatomía de una pieza FDM

Una pieza FDM se construye por regiones:

| Región | Función |
|---|---|
| Perímetros o paredes | Definen la forma externa y gran parte de la resistencia |
| Capas superiores | Cierran la pieza por arriba |
| Capas inferiores | Formaran la base |
| Infill o relleno | Aporta soporte interno y rigidez |
| Soportes | Sostienen geometrías que no pueden imprimirse en el aire |
| Costura Z | Punto de inicio/cierre de perímetros |
| Puentes | Trayectorias que cruzan espacios cortos sin soporte |
| Brim / skirt / raft | Estructuras auxiliares para purga o adhesión |

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> corte de una pieza FDM mostrando paredes, relleno, capas superiores, capas inferiores, soportes, costura Z y orientación de capas. Archivo sugerido: <code>assets/img/tecnologias/anatomia-pieza-fdm.png</code>.
</div>

---

## 6. Variables que definen la calidad en FDM

### 6.1 Altura de capa

La altura de capa afecta la resolución vertical, el tiempo de impresión y el acabado. Capas más delgadas producen superficies más suaves, pero aumentan el tiempo.

| Altura de capa | Uso típico |
|---|---|
| 0.08–0.12 mm | Detalle fino |
| 0.16–0.20 mm | Uso general |
| 0.24–0.32 mm | Prototipos rápidos y piezas grandes |

### 6.2 Temperatura

La temperatura de boquilla controla el flujo y la adhesión entre capas. Una temperatura baja puede producir subextrusión o capas débiles. Una temperatura alta puede producir hilos, pérdida de detalle o degradación.

La temperatura de cama mejora la adhesión inicial y reduce deformaciones.

### 6.3 Velocidad

Imprimir rápido reduce tiempo, pero exige más al hotend, al sistema de movimiento y al control de vibración. Una impresora puede anunciar velocidades muy altas, pero la calidad útil depende de aceleración, flujo volumétrico, geometría y material.

### 6.4 Infill

El infill no solo ahorra material. También define rigidez, soporte interno y comportamiento mecánico.

| Infill | Uso |
|---|---|
| 10–15 % | Piezas visuales |
| 15–25 % | Uso general |
| 30–50 % | Piezas funcionales |
| 80–100 % | Casos específicos, no siempre mejora proporcionalmente |

En muchas piezas funcionales, aumentar paredes/perímetros puede ser más efectivo que aumentar demasiado el infill.

### 6.5 Orientación

La orientación define resistencia, acabado, necesidad de soportes y tiempo. Una misma pieza puede comportarse de forma muy distinta según se imprima acostada, vertical o inclinada.

La dirección de las capas es especialmente importante: FDM tiende a ser anisotrópico. Es decir, la resistencia no es igual en todas las direcciones.

### 6.6 Soportes

Los soportes permiten imprimir voladizos, pero agregan tiempo, material y marcas. Un buen diseño para FDM intenta reducir soportes desde la geometría misma.

### 6.7 Humedad del filamento

Materiales como nylon, PETG, TPU y algunos PLA absorben humedad. La humedad provoca burbujas, hilos, superficie rugosa y pérdida de resistencia. Por eso los filamentos deben almacenarse correctamente y, en algunos casos, secarse antes de imprimir.

---

## 7. Ventajas de FDM frente a otras tecnologías

FDM no es la tecnología más fina ni la más industrial, pero es la más democratizadora.

| Ventaja | Por qué importa en FabLab |
|---|---|
| Bajo costo de entrada | Permite que escuelas, laboratorios y usuarios compren equipos |
| Materiales accesibles | PLA, PETG y TPU son fáciles de conseguir |
| Proceso visible | El estudiante ve cómo se fabrica la pieza |
| Mantenimiento posible | Muchas reparaciones son comprensibles y documentables |
| Buen tamaño de impresión | Las máquinas de escritorio ofrecen volúmenes útiles |
| Seguridad manejable | Con ventilación y buenas prácticas, FDM es más accesible que resina o polvo |
| Adecuada para electrónica y robótica | Carcasas, soportes, adaptadores y mecanismos simples |

---

## 8. Limitaciones de FDM

| Limitación | Consecuencia |
|---|---|
| Líneas de capa visibles | Menor acabado visual que resina |
| Anisotropía | La pieza puede romperse entre capas |
| Soportes | Algunas geometrías dejan marcas |
| Contracción térmica | Warping, especialmente en ABS/ASA |
| Tolerancias variables | Agujeros y ensambles requieren compensación |
| Menor detalle fino | No compite con resina en miniaturas o joyería |
| Productividad limitada | Cada pieza ocupa tiempo de máquina |

FDM es excelente para prototipar, aprender, fabricar herramientas auxiliares y resolver problemas reales de bajo volumen. No es ideal para todas las piezas ni para toda escala de producción.

---

## 9. Modelos FDM actuales representativos

Los precios cambian por región, promoción, envío, impuestos y disponibilidad. La siguiente tabla sirve como referencia comparativa para entender categorías de mercado. Los enlaces apuntan a páginas de fabricante o distribuidores reconocidos.

| Modelo | Tipo | Volumen de impresión | Precio de referencia | Perfil de uso | Liga |
|---|---|---:|---:|---|---|
| Bambu Lab A1 | FDM, cama móvil moderna, automatizada | 256 × 256 × 256 mm | desde aprox. 279–399 USD según configuración/promoción | FabLab, educación, usuario inicial-intermedio, multicolor con AMS Lite | [Bambu Lab A1](https://us.store.bambulab.com/products/a1) |
| Bambu Lab A1 mini | FDM compacta | 180 × 180 × 180 mm | desde aprox. 209 USD | Entrada económica, escritorio, piezas pequeñas | [Bambu Lab A1 mini](https://us.store.bambulab.com/products/a1-mini) |
| Flashforge Adventurer 5M | FDM CoreXY abierta | 220 × 220 × 220 mm | aprox. 299 USD | Usuario principiante/intermedio que busca velocidad y facilidad | [Flashforge Adventurer 5M](https://www.flashforge.com/products/adventurer-5m-3d-printer) |
| Creality Ender-3 V3 SE | FDM económica, direct drive | 220 × 220 × 250 mm | rango económico; depende de tienda y región | Entrada de bajo costo, aprendizaje, modificación | [Creality Ender-3 V3 SE](https://store.creality.com/products/ender-3-v3-se-3d-printer) |
| Original Prusa MK4S | FDM abierta/prosumer | 250 × 210 × 220 mm | kit aprox. 729 USD; ensamblada aprox. 999 USD | Educación, laboratorio, usuarios que valoran documentación y ecosistema abierto | [Original Prusa MK4S](https://www.prusa3d.com/product/original-prusa-mk4s-3d-printer/) |
| Prusa CORE One | FDM cerrada, CoreXY | 250 × 220 × 270 mm | aprox. 949 USD kit; 1199 USD ensamblada | Materiales más técnicos, mejor control térmico | [Prusa CORE One](https://www.prusa3d.com/product/original-prusa-core-one-kit/) |
| Bambu Lab P1S | FDM cerrada, CoreXY | 256 × 256 × 256 mm | rango prosumer | Impresión rápida, carcasa cerrada, materiales más exigentes que PLA/PETG | [Bambu Lab P1S](https://us.store.bambulab.com/products/p1s) |

> **Nota:** en México, los precios finales pueden cambiar mucho por importación, IVA, envío, disponibilidad local, garantía y soporte. Para compra institucional conviene comparar proveedor local, soporte, refacciones, tiempos de entrega y facturación, no solo el precio base en USD.

---

## 10. Cómo leer una tabla de especificaciones FDM

Cuando se compara una impresora FDM, no basta con mirar la velocidad máxima. Conviene revisar:

| Especificación | Pregunta técnica |
|---|---|
| Volumen de impresión | ¿La pieza cabe en la máquina? |
| Temperatura máxima de boquilla | ¿Permite PETG, TPU, ABS, ASA, nylon o PC? |
| Temperatura máxima de cama | ¿Puede controlar contracción térmica? |
| Cámara cerrada | ¿Ayuda con ABS, ASA o materiales técnicos? |
| Direct drive | ¿Facilita TPU y reduce retracción? |
| Nivelación automática | ¿Reduce errores de primera capa? |
| Sensor de filamento | ¿Evita fallas por carrete agotado? |
| Tipo de superficie | ¿Facilita adhesión y retiro de pieza? |
| Ecosistema de software | ¿El flujo es abierto, cerrado, local o nube? |
| Refacciones | ¿Hay boquillas, hotends, camas y sensores disponibles? |
| Comunidad | ¿Existen perfiles, tutoriales, repuestos y soporte? |

---

# Parte II. Tecnologías complementarias a FDM

## 11. Impresión con resina: SLA, DLP y MSLA

Las impresoras de resina usan un material líquido fotosensible que se solidifica con luz. A diferencia de FDM, donde se deposita un cordón de plástico, en resina se forma una sección completa de la pieza mediante exposición luminosa.

### 11.1 SLA

En **SLA**, un láser dibuja la sección de la pieza sobre la resina. Es una de las tecnologías históricas de impresión 3D y se asocia con precisión y buen acabado.

### 11.2 DLP

En **DLP**, un proyector ilumina la capa o zonas amplias de la capa. Puede ser rápido porque no necesita trazar punto por punto toda la geometría.

### 11.3 MSLA / LCD

En **MSLA**, una pantalla LCD actúa como máscara y deja pasar luz UV en las zonas que deben solidificarse. Es la forma más común en impresoras de resina de escritorio actuales.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> comparación visual entre FDM y resina: filamento depositado vs resina curada por luz. Archivo sugerido: <code>assets/img/tecnologias/fdm-vs-resina-proceso.png</code>.
</div>

### 11.4 Ventajas de resina respecto a FDM

| Ventaja | Explicación |
|---|---|
| Mayor detalle fino | Ideal para miniaturas, figuras, moldes, odontología y joyería |
| Mejor acabado superficial | Capas menos visibles que en FDM |
| Alta precisión visual | Muy útil para piezas pequeñas y modelos estéticos |
| Geometrías delicadas | Puede producir detalles que FDM no resuelve bien |

### 11.5 Desventajas de resina respecto a FDM

| Desventaja | Implicación |
|---|---|
| Manejo químico | Resinas requieren guantes, ventilación y cuidado |
| Postprocesado obligatorio | Lavado y curado posterior |
| Residuos | Alcohol, resina contaminada, guantes y papel deben manejarse responsablemente |
| Fragilidad | Muchas resinas estándar son más frágiles que PLA/PETG |
| Volumen útil menor | Muchas máquinas de escritorio tienen cama más pequeña que FDM |
| Mayor suciedad operativa | Derrames, olor, limpieza de tanque y película |

### 11.6 Modelos actuales de resina representativos

| Modelo | Tecnología | Volumen de impresión | Precio de referencia | Perfil de uso | Liga |
|---|---|---:|---:|---|---|
| Anycubic Photon Mono M7 | MSLA / LCD | 223 × 126 × 230 mm | aprox. 429 USD | Resina de escritorio, alta resolución, hobby avanzado | [Anycubic Photon Mono M7](https://store.anycubic.com/products/photon-mono-m7) |
| Elegoo Mars 5 Ultra | MSLA / LCD | 153.36 × 77.76 × 165 mm | aprox. 228–289 USD según tienda/región | Miniaturas, piezas pequeñas, entrada a resina | [Elegoo Mars 5 Ultra](https://www.3djake.com/elegoo/mars-5-ultra) |
| Original Prusa SL1S SPEED | MSLA / LCD | 127 × 80 × 150 mm | aprox. 1,999 USD; bundle con lavado/curado aprox. 2,599 USD | Resina de escritorio robusta, entorno educativo/prosumer | [Prusa SL1S SPEED](https://www.prusa3d.com/product/original-prusa-sl1s-speed-3d-printer/) |
| Formlabs Form 4 | MSLA / SLA de escritorio profesional | 200 × 125 × 210 mm | desde 2,625 USD paquete básico | Laboratorios, diseño, ingeniería, odontología según versión/material | [Formlabs Form 4](https://formlabs.com/products/form-4-basic-package/) |

---

## 12. SLS: sinterizado selectivo por láser

**SLS** significa *Selective Laser Sintering*. Esta tecnología usa polvo, normalmente nylon PA12 o PA11. Una capa de polvo se extiende sobre la cama y un láser sinteriza únicamente las zonas que corresponden a la pieza.

El polvo no sinterizado rodea la pieza y funciona como soporte natural. Por eso SLS puede fabricar geometrías complejas sin estructuras de soporte tradicionales.

### 12.1 Ventajas de SLS respecto a FDM

| Ventaja | Explicación |
|---|---|
| No requiere soportes convencionales | El polvo suelto sostiene la pieza |
| Buenas propiedades mecánicas | PA12 y PA11 son útiles para piezas funcionales |
| Piezas complejas | Permite geometrías internas y ensambles más difíciles en FDM |
| Producción por empaquetado | Se pueden acomodar varias piezas en el volumen de polvo |
| Mejor isotropía relativa | Generalmente menos dependiente de orientación que FDM |

### 12.2 Desventajas de SLS respecto a FDM

| Desventaja | Implicación |
|---|---|
| Costo alto de equipo | Entra en escala profesional/industrial |
| Manejo de polvo | Requiere limpieza, recuperación de polvo y seguridad |
| Postprocesado | Desempolvado y acabado posterior |
| Curva operativa | Más complejo que FDM para usuarios nuevos |
| Espacio e infraestructura | Mejor para laboratorio especializado que para aula básica |

### 12.3 Modelos SLS representativos

| Modelo | Tecnología | Volumen de impresión | Precio de referencia | Perfil de uso | Liga |
|---|---|---:|---:|---|---|
| Sinterit Lisa X | SLS compacto | hasta 130 × 180 × 330 mm | aprox. 21,990 EUR / 23,990 USD solo impresora | R&D, ingeniería, laboratorio profesional | [Sinterit Lisa X](https://sinterit.com/product/lisa-x-sls-3d-printer/) |
| Formlabs Fuse 1+ 30W | SLS de banco profesional | categoría SLS compacta | desde aprox. 29,499 USD starter; workflow completo más alto | Series cortas, piezas funcionales, laboratorios | [Formlabs Fuse 1+ 30W](https://formlabs.com/compare/markforged-vs-formlabs-fuse-1/) |

---

## 13. MJF: Multi Jet Fusion

**Multi Jet Fusion** es una tecnología desarrollada por HP. Usa una cama de polvo y agentes que se depositan selectivamente para controlar qué zonas absorben energía y se fusionan.

MJF se usa mucho en servicios industriales para series cortas y piezas funcionales de polímero, especialmente con PA12.

### Ventajas frente a FDM

- Mejor productividad por lote.
- Buena repetibilidad.
- Piezas funcionales sin soportes tradicionales.
- Adecuada para bajo y mediano volumen.
- Buena para servicios de manufactura bajo demanda.

### Desventajas frente a FDM

- Equipo costoso.
- No es común en FabLabs pequeños.
- Requiere infraestructura y postprocesado.
- Menor control directo para usuarios principiantes.
- Normalmente se accede mediante proveedores o centros de manufactura.

### Cuándo considerarla

MJF tiene sentido cuando una pieza ya fue validada y se requiere fabricar varias unidades con mejor repetibilidad que FDM, sin llegar a justificar un molde de inyección.

---

## 14. Impresión 3D metálica

La impresión metálica incluye varias tecnologías:

| Tecnología | Cómo funciona | Uso típico |
|---|---|---|
| SLM / LPBF | Funde polvo metálico con láser | Aeroespacial, médico, piezas complejas |
| DMLS | Sinteriza/fusiona polvo metálico | Ingeniería avanzada |
| EBM | Usa haz de electrones | Titanio, implantes, aeroespacial |
| DED | Deposita material y lo funde con energía dirigida | Reparación, piezas grandes |
| Binder Jetting metálico | Une polvo con aglutinante y luego sinteriza | Producción metálica en lote |

### Ventajas frente a FDM

- Materiales metálicos reales.
- Geometrías imposibles por mecanizado tradicional.
- Optimización topológica.
- Canales internos.
- Piezas biomédicas y aeroespaciales.

### Desventajas frente a FDM

- Costos muy altos.
- Seguridad avanzada.
- Polvos metálicos peligrosos.
- Atmósferas controladas.
- Postprocesos térmicos y mecánicos.
- No es tecnología de entrada para FabLabs educativos.

Para un FabLab, lo importante es conocer que existe y entender su lugar en la manufactura avanzada. No debe confundirse con filamentos FDM “metal-filled”, que normalmente son plásticos con polvo metálico y no piezas metálicas estructurales.

---

## 15. Comparación general: FDM vs otras tecnologías

| Criterio | FDM / FFF | Resina | SLS | MJF | Metal AM |
|---|---|---|---|---|---|
| Costo de entrada | Bajo | Bajo-medio | Alto | Muy alto | Muy alto |
| Facilidad para iniciar | Alta | Media | Baja | Baja | Muy baja |
| Seguridad | Moderada | Mayor cuidado químico | Manejo de polvo | Industrial | Alta complejidad |
| Detalle fino | Medio | Alto | Medio | Medio | Alto |
| Acabado superficial | Medio | Alto | Medio-alto | Medio-alto | Variable |
| Resistencia funcional | Media | Variable | Alta | Alta | Alta |
| Volumen común en escritorio | Medio | Bajo-medio | Medio | Industrial | Industrial |
| Soportes | Sí | Sí | No convencionales | No convencionales | Depende |
| Postprocesado | Bajo-medio | Obligatorio | Obligatorio | Obligatorio | Obligatorio |
| Mejor aplicación | Prototipado, FabLab, educación | Detalle visual | Piezas funcionales complejas | Series cortas | Industria avanzada |

---

## 16. Selección rápida de tecnología

| Necesidad | Tecnología recomendada | Motivo |
|---|---|---|
| Aprender impresión 3D en FabLab | FDM | Visible, económica, segura y didáctica |
| Carcasa para electrónica | FDM | Buen balance entre costo, tamaño y resistencia |
| Soporte para sensor o robot | FDM | Rápida iteración y materiales como PETG/TPU |
| Miniatura o figura detallada | Resina | Mayor resolución visual |
| Molde maestro para joyería | Resina castable | Detalle fino y proceso especializado |
| Pieza funcional compleja sin soportes | SLS | El polvo sostiene la geometría |
| Lote corto de piezas plásticas | SLS o MJF | Mejor repetibilidad y productividad |
| Implante o pieza metálica avanzada | Metal AM | Material metálico real y geometrías complejas |
| Prototipo de forma y ergonomía | FDM | Bajo costo y tamaño útil |
| Pieza final personalizada de bajo volumen | FDM, resina o SLS | Depende de detalle, resistencia y material |

---

## 17. Criterios de compra para un FabLab

Antes de comprar una impresora, conviene evaluar:

### 17.1 Costo total, no solo precio de máquina

El costo real incluye:

- impresora;
- filamento, resina o polvo;
- refacciones;
- boquillas;
- placas de impresión;
- tanques o películas en resina;
- herramientas de limpieza;
- equipo de seguridad;
- software;
- mantenimiento;
- tiempo de operador;
- garantía y soporte.

### 17.2 Disponibilidad de refacciones

Una impresora barata puede salir cara si no hay boquillas, hotends, sensores, camas, placas o soporte técnico.

### 17.3 Comunidad y documentación

Para educación, la comunidad es parte del equipo. Una impresora con muchos usuarios suele tener perfiles, tutoriales, diagnósticos, modificaciones y soluciones documentadas.

### 17.4 Software y flujo de trabajo

Algunas máquinas dependen de ecosistemas propietarios; otras trabajan con software abierto. Esto no es necesariamente bueno o malo: depende del objetivo.

Para un FabLab educativo conviene balancear:

- facilidad de uso;
- posibilidad de aprender parámetros;
- compatibilidad con formatos comunes;
- operación local;
- gestión de usuarios;
- privacidad;
- mantenimiento;
- documentación.

### 17.5 Seguridad

FDM suele ser más simple de operar, pero no significa que sea libre de riesgos. Resina y SLS requieren mayor control de químicos, polvos y residuos. Las decisiones de compra deben considerar ventilación, capacitación y disposición de residuos.

---

## 18. Recomendación para este curso

Este curso se centrará principalmente en **FDM / FFF**, porque es la tecnología más representativa para un entorno FabLab:

- permite iniciar rápido;
- hace visible el proceso;
- conecta diseño digital con objeto físico;
- usa materiales accesibles;
- permite reparar, modificar y aprender;
- sirve para prototipos, soportes, carcasas, robótica, docencia y proyectos DIY.

Las demás tecnologías se deben entender como ampliaciones del ecosistema. Resina es excelente cuando el detalle importa. SLS y MJF son potentes cuando se buscan piezas funcionales complejas o lotes cortos. La impresión metálica pertenece a una escala industrial avanzada.

El criterio importante no es elegir “la mejor impresora”, sino elegir **el proceso adecuado para la pieza, el material, el usuario y el contexto de fabricación**.

---

## 19. Referencias y ligas de consulta

[1] Stratasys, “FDM 3D Printing – Fused Deposition Modeling.”  
<https://www.stratasys.com/en/guide-to-3d-printing/technologies-and-materials/fdm-technology/>

[2] Bambu Lab, “A1 Technical Specifications.”  
<https://bambulab.com/en/a1/tech-specs>

[3] Bambu Lab Store, “Bambu Lab A1.”  
<https://us.store.bambulab.com/products/a1>

[4] Bambu Lab Store, “A1 mini.”  
<https://us.store.bambulab.com/products/a1-mini>

[5] Flashforge, “Adventurer 5M.”  
<https://www.flashforge.com/products/adventurer-5m-3d-printer>

[6] Creality, “Ender-3 V3 SE.”  
<https://store.creality.com/products/ender-3-v3-se-3d-printer>

[7] Original Prusa, “Original Prusa MK4S.”  
<https://www.prusa3d.com/product/original-prusa-mk4s-3d-printer/>

[8] Anycubic, “Photon Mono M7.”  
<https://store.anycubic.com/products/photon-mono-m7>

[9] Formlabs, “Form 4 Basic Package.”  
<https://formlabs.com/products/form-4-basic-package/>

[10] Sinterit, “Lisa X SLS 3D Printer.”  
<https://sinterit.com/product/lisa-x-sls-3d-printer/>

[11] Formlabs, “Fuse 1+ 30W.”  
<https://formlabs.com/compare/markforged-vs-formlabs-fuse-1/>

[12] NIOSH, “3D Printing with Filaments: Health and Safety Questions to Ask.”  
<https://www.cdc.gov/niosh/docs/2024-103/>

---

## Siguiente sección

[Materiales para impresión 3D](materiales.md)
