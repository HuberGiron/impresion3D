---
layout: default
title: Slicers y laminado
nav_exclude: true
---

# Slicers y laminado

El slicer o laminador es el software que convierte un modelo 3D en instrucciones que la impresora puede ejecutar. Es una de las piezas más importantes del flujo de impresión 3D, porque ahí se decide cómo se construirá físicamente la pieza.

Un mismo modelo puede producir resultados muy diferentes si se cambia la orientación, la altura de capa, el relleno, los soportes, la temperatura o la velocidad. Por eso, el slicer no debe verse como un simple paso administrativo antes de imprimir. Es el espacio donde el usuario traduce una intención de diseño en una estrategia de fabricación.

<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> captura de un slicer mostrando modelo, capas, soportes y vista previa. Archivo sugerido: <code>assets/img/slicers/vista-previa-slicer.png</code>.
</div>

## 1. Qué significa laminar

Laminar significa dividir un modelo 3D en capas horizontales. Cada capa se convierte en trayectorias que la impresora ejecuta con movimientos controlados.

El slicer calcula:

- perímetros;
- relleno;
- capas superiores e inferiores;
- soportes;
- movimientos de viaje;
- retracciones;
- temperaturas;
- velocidades;
- ventilación;
- tiempo estimado;
- material estimado.

## 2. Entrada y salida del slicer

### Entrada

El slicer recibe modelos como:

- STL;
- OBJ;
- 3MF;
- STEP, en algunos programas;
- archivos de proyecto.

### Salida

El resultado puede ser:

- G-code;
- archivo compatible con una impresora específica;
- proyecto 3MF con parámetros;
- archivo enviado por red o nube al equipo.

## 3. Altura de capa

La altura de capa define el espesor vertical de cada capa. Es uno de los parámetros más visibles.

- Capas bajas: más detalle vertical, mejor superficie, mayor tiempo.
- Capas altas: impresión más rápida, menor detalle, líneas más visibles.

Con una boquilla de 0.4 mm, es común usar alturas de capa como 0.12, 0.16, 0.20 o 0.28 mm. La documentación de PrusaSlicer recomienda que la altura de capa se mantenga por debajo de aproximadamente el 80% del diámetro de boquilla; por ejemplo, con boquilla de 0.4 mm, una altura máxima razonable ronda 0.32 mm.

## 4. Ancho de línea

El ancho de línea es el ancho de material depositado. Suele estar relacionado con el diámetro de la boquilla, pero puede ajustarse dentro de ciertos límites.

Un ancho mayor puede mejorar adhesión y resistencia, pero reduce detalle. Un ancho menor puede mejorar detalle, pero puede generar líneas débiles si se configura mal.

## 5. Temperatura de boquilla

La temperatura debe corresponder al material. Cada filamento tiene un rango recomendado. La temperatura afecta flujo, adhesión entre capas, stringing, detalle y resistencia.

Ejemplos generales:

- PLA: temperatura moderada.
- PETG: temperatura mayor que PLA.
- ABS/ASA: temperatura más alta y ambiente controlado.
- TPU: temperatura variable según formulación.
- Nylon: temperatura alta y filamento seco.

## 6. Temperatura de cama

La cama caliente ayuda a que la primera capa se adhiera. También reduce deformación en materiales con mayor contracción.

Si la temperatura es insuficiente, la pieza puede despegarse. Si es excesiva, puede aparecer deformación en la base.

## 7. Velocidad

La velocidad afecta el tiempo de impresión y la calidad. Una impresora moderna puede moverse rápido, pero la velocidad útil depende de material, hotend, flujo máximo, aceleración, geometría y enfriamiento.

Imprimir muy rápido puede producir:

- pérdida de detalle;
- mala adhesión;
- vibraciones;
- ghosting;
- subextrusión;
- ruido;
- fallas en esquinas.

## 8. Perímetros

Los perímetros o paredes definen la estructura externa de la pieza. Para piezas funcionales, aumentar perímetros puede ser más efectivo que aumentar mucho el relleno.

Ejemplo:

- pieza visual: 2 perímetros pueden ser suficientes;
- pieza funcional: 3 a 5 perímetros pueden mejorar resistencia;
- pieza con tornillos: conviene reforzar zonas de unión.

## 9. Capas superiores e inferiores

Estas capas cierran la pieza. Si son pocas, el relleno puede verse o la superficie puede quedar débil. Si son demasiadas, aumenta tiempo y material sin necesidad.

## 10. Infill o relleno

El infill define la estructura interna. No todas las piezas requieren alto porcentaje de relleno. Una pieza con buenos perímetros puede ser resistente con relleno moderado.

Patrones comunes:

- rectilíneo;
- grid;
- triangular;
- cúbico;
- gyroid;
- panal;
- concéntrico.

La documentación de UltiMaker Cura describe múltiples configuraciones de infill y permite ajustar densidad, patrón y comportamiento interno de la pieza.

## 11. Soportes

Los soportes permiten imprimir geometrías con voladizos. Sin ellos, el material fundido se depositaría en el aire y caería o deformaría.

Tipos comunes:

- soportes normales;
- soportes tipo árbol;
- soportes orgánicos;
- soporte desde cama;
- soporte en todas partes;
- interfaz de soporte.

Los soportes deben usarse con criterio. Aumentan tiempo, material y postprocesado. Además, pueden dejar marcas.

## 12. Orientación de pieza

La orientación es una de las decisiones más importantes. Afecta:

- resistencia;
- acabado superficial;
- cantidad de soportes;
- tiempo;
- precisión;
- estabilidad en cama;
- dirección de capas.

Una pieza que soporta carga debe orientarse considerando la dirección de esfuerzo. En FDM, la unión entre capas puede ser más débil que el material dentro de la capa.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> misma pieza orientada de tres formas, mostrando diferencia en soportes y dirección de esfuerzo. Archivo sugerido: <code>assets/img/slicers/orientacion-pieza.png</code>.
</div>

## 13. Adhesión a cama

Opciones comunes:

- **Skirt:** línea alrededor de la pieza para purgar y verificar flujo.
- **Brim:** borde unido a la pieza para mejorar adhesión.
- **Raft:** base completa debajo de la pieza.

El brim es útil para piezas con poca superficie de contacto o materiales propensos a warping. El raft se usa menos en impresoras modernas, pero puede ayudar en casos difíciles.

## 14. Retracción

La retracción retira ligeramente el filamento cuando la boquilla viaja sin imprimir. Ayuda a reducir hilos o stringing.

Si la retracción es insuficiente, aparecen hilos. Si es excesiva, puede causar atascos, huecos o desgaste del filamento.

## 15. Costura Z

La costura Z es el punto donde el slicer inicia o termina perímetros. Puede configurarse para alinearse, ocultarse en una esquina o distribuirse. La elección depende de si se prioriza estética o uniformidad.

## 16. Vista previa por capas

La vista previa permite revisar antes de imprimir:

- si los soportes aparecen donde se necesitan;
- si hay zonas sin material;
- si las paredes son demasiado delgadas;
- si el relleno tiene sentido;
- si la primera capa es adecuada;
- si el tiempo estimado es razonable;
- si hay movimientos extraños.

Una buena práctica en FabLab es enseñar a revisar la vista previa antes de ocupar máquina.

## 17. Slicers comunes

### 17.1 Bambu Studio

Software oficial de Bambu Lab. Está orientado a impresoras Bambu y ofrece flujo por proyecto, perfiles integrados y herramientas de laminado.

### 17.2 OrcaSlicer

Slicer derivado de Bambu Studio y PrusaSlicer, usado por muchos usuarios avanzados por sus opciones de calibración y compatibilidad.

### 17.3 PrusaSlicer

Slicer desarrollado por Prusa Research, con fuerte presencia en la comunidad de impresión 3D.

### 17.4 Cura

Slicer de UltiMaker, ampliamente usado y compatible con muchas impresoras.

## 18. El slicer como espacio de decisión

El slicer no solo prepara una impresión; expresa una estrategia. Dos usuarios pueden imprimir la misma pieza con resultados distintos porque decidieron diferente:

- orientación;
- altura de capa;
- material;
- relleno;
- soportes;
- velocidad;
- temperatura;
- adhesión.

Aprender a usar el slicer es aprender a pensar la fabricación.

## Referencias

[1] Bambu Lab, “Bambu Studio.”  
[2] Prusa Research, “Layers and perimeters.”  
[3] UltiMaker, “Cura infill settings.”

## Siguiente sección

[Bambu Lab A1 y Bambu Studio](bambu-a1.md)
