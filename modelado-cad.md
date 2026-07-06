---
layout: default
title: Modelado CAD
nav_order: 10
---

# Modelado CAD: paramétrico y orgánico

Para imprimir una pieza en 3D se necesita un modelo digital. Ese modelo puede generarse de muchas formas, pero una de las más importantes es el diseño asistido por computadora o **CAD**.

No todos los programas de modelado piensan la geometría de la misma manera. Algunos están orientados a piezas técnicas con medidas precisas; otros están pensados para formas artísticas, personajes, superficies orgánicas o escultura digital. Para impresión 3D conviene distinguir entre **modelado paramétrico** y **modelado orgánico**.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> comparación entre una pieza paramétrica con cotas y una figura orgánica modelada como malla. Archivo sugerido: <code>assets/img/modelado/parametrico-vs-organico.png</code>.
</div>

## 1. CAD paramétrico

El CAD paramétrico se basa en operaciones controladas por dimensiones, restricciones y relaciones geométricas. Es el tipo de modelado más usado en ingeniería mecánica, diseño de producto, manufactura y piezas funcionales.

Una pieza paramétrica suele construirse mediante:

- bocetos 2D;
- líneas, círculos, arcos y perfiles;
- restricciones geométricas;
- cotas;
- extrusiones;
- revoluciones;
- cortes;
- redondeos;
- chaflanes;
- patrones;
- operaciones booleanas;
- ensambles.

La gran ventaja es que el diseño puede modificarse de forma controlada. Si una perforación debe cambiar de 3 mm a 4 mm, se modifica una cota. Si una pieza debe alargarse 10 mm, se ajusta una dimensión. Esto es esencial para piezas que deben ensamblar o cumplir medidas.

## 2. Ejemplos de software paramétrico

- Fusion.
- SolidWorks.
- FreeCAD.
- Onshape.
- Inventor.
- Creo.
- Siemens NX.
- OpenSCAD, desde un enfoque programático.

En un FabLab, FreeCAD, Onshape, Fusion educativo y Tinkercad suelen ser opciones frecuentes dependiendo del nivel del usuario.

## 3. Cuándo usar CAD paramétrico

CAD paramétrico es preferible cuando la pieza:

- debe tener medidas precisas;
- se ensambla con otros componentes;
- usa tornillos, tuercas o insertos;
- tiene agujeros funcionales;
- requiere tolerancias;
- debe modificarse varias veces;
- pertenece a un mecanismo;
- forma parte de un proyecto de ingeniería;
- debe documentarse con planos.

Ejemplos:

- soporte para sensor;
- carcasa para electrónica;
- base para motor;
- acoplamiento;
- adaptador;
- pieza de robot;
- guía mecánica;
- fixture de laboratorio.

## 4. Modelado orgánico

El modelado orgánico se enfoca en formas libres, suaves o artísticas. En lugar de partir de cotas y restricciones, trabaja con mallas, superficies, escultura digital, subdivisión y deformación.

Es común en:

- personajes;
- miniaturas;
- esculturas;
- figuras anatómicas;
- ornamentos;
- superficies naturales;
- modelos artísticos;
- objetos decorativos.

Software común:

- Blender;
- ZBrush;
- Nomad Sculpt;
- Meshmixer;
- SculptGL.

## 5. Ventajas del modelado orgánico

- Permite formas difíciles de crear con CAD paramétrico.
- Es adecuado para detalles visuales.
- Facilita esculturas, personajes y texturas.
- Funciona bien con tabletas gráficas o herramientas de escultura.
- Es compatible con flujos de animación, render y arte digital.

## 6. Limitaciones del modelado orgánico para impresión 3D

Las formas orgánicas pueden verse muy bien en pantalla, pero presentar problemas para impresión:

- mallas demasiado densas;
- superficies sin espesor;
- geometría no-manifold;
- detalles demasiado finos;
- escala indefinida;
- falta de planos de apoyo;
- dificultad para modificar medidas exactas;
- ausencia de tolerancias funcionales.

Por eso, una figura orgánica puede requerir reparación de malla, reducción de polígonos, corte en partes o preparación especial antes de imprimirse.

## 7. Comparación entre CAD paramétrico y modelado orgánico

| Criterio | CAD paramétrico | Modelado orgánico |
|---|---|---|
| Mejor para | Piezas técnicas | Formas libres |
| Control dimensional | Alto | Medio o bajo |
| Edición por cotas | Sí | Limitada |
| Ensambles | Muy adecuado | Poco adecuado |
| Detalle artístico | Limitado | Alto |
| Malla final | Exportada al final | Normalmente nativa |
| Riesgo de errores de malla | Bajo-medio | Medio-alto |
| Uso típico | Ingeniería, producto, robótica | Arte, miniaturas, anatomía |

## 8. Modelar pensando en impresión 3D

Diseñar para impresión 3D requiere pensar en el proceso de fabricación desde el inicio. No basta con que la pieza exista en el software.

Criterios importantes:

- evitar paredes demasiado delgadas;
- considerar dirección de impresión;
- reducir voladizos innecesarios;
- pensar dónde quedarán los soportes;
- diseñar bases estables;
- incorporar holguras para ensamble;
- redondear esquinas internas;
- evitar detalles más pequeños que la boquilla;
- considerar el material;
- dividir piezas grandes en partes ensamblables.

## 9. Archivos fuente y archivos exportados

Un error frecuente en impresión 3D es conservar solo el STL. El STL sirve para imprimir, pero no es el mejor archivo para editar.

Conviene conservar:

- archivo nativo CAD;
- STEP si es una pieza técnica;
- STL o 3MF para impresión;
- capturas de parámetros de laminado;
- notas de versión.

En proyectos de FabLab, documentar el archivo fuente permite que otra persona modifique, corrija o adapte la pieza posteriormente.

## 10. Diseño paramétrico como cultura de iteración

El diseño paramétrico se alinea muy bien con el prototipado porque permite modificar dimensiones de forma controlada. Si una pieza no ajusta, se cambia una cota; si una pared es débil, se aumenta espesor; si una perforación queda pequeña, se corrige el diámetro.

Esta capacidad de corrección es central en fabricación digital. Una pieza impresa no debe entenderse como resultado final inmediato, sino como una versión dentro de un proceso de mejora.

## Referencias

[1] Tinkercad Help Center, “Export filetypes.”  
[2] FreeCAD Documentation, “Part Design Workbench.”  
[3] Blender Manual, “Modeling.”

## Siguiente sección

[Escaneo 3D](escaneo-3d.md)
