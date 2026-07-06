---
layout: default
title: Archivos 3D y mallas
nav_order: 9
---

# Archivos 3D y mallas

Para imprimir en 3D, la máquina necesita información geométrica. Esa información debe describir la forma del objeto de manera que el software pueda dividirlo en capas y generar trayectorias de impresión.

En muchos flujos de trabajo, la geometría se transfiere como una **malla**. Una malla no es el objeto sólido en sí, sino una representación de su superficie mediante pequeños polígonos, normalmente triángulos. Entender qué es una malla ayuda a explicar muchos problemas comunes de impresión: agujeros, paredes sin espesor, normales invertidas, geometría no-manifold o modelos que se ven bien pero no se pueden laminar correctamente.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> esfera representada como malla triangular, mostrando vértices, aristas y caras. Archivo sugerido: <code>assets/img/archivos/malla-triangular.png</code>.
</div>

## 1. Qué es una malla

Una malla está formada por:

- **vértices:** puntos en el espacio;
- **aristas:** líneas que conectan vértices;
- **caras:** superficies formadas por aristas;
- **normales:** direcciones que indican hacia dónde apunta una cara;
- **volumen implícito:** interpretación de qué lado de la superficie corresponde al interior.

En impresión 3D, la malla debe describir una superficie cerrada que pueda interpretarse como un volumen. Si la malla tiene agujeros, caras duplicadas o intersecciones internas, el slicer puede producir resultados incorrectos.

## 2. Malla cerrada o watertight

Un modelo imprimible debe ser, idealmente, **cerrado**. Esto significa que no debe tener huecos en la superficie. Una forma práctica de imaginarlo es pensar en una pieza que pudiera llenarse con agua sin fugas; de ahí viene el término *watertight*.

Cuando una malla no está cerrada, el software puede no saber qué es interior y qué es exterior. Esto puede generar capas faltantes, superficies abiertas o trayectorias inesperadas.

## 3. Geometría no-manifold

Una malla no-manifold contiene configuraciones que no representan correctamente un sólido físico. Por ejemplo:

- una arista compartida por más de dos caras;
- caras internas duplicadas;
- superficies que se cruzan;
- paredes sin espesor;
- vértices conectados de manera ambigua.

En pantalla, un modelo no-manifold puede verse correcto. Sin embargo, al laminarlo puede producir errores, huecos o piezas defectuosas.

## 4. Normales

Las normales indican la dirección de una superficie. En una malla correcta, las normales deben apuntar hacia el exterior de la pieza. Si algunas normales están invertidas, el software puede interpretar zonas externas como internas o viceversa.

Algunos slicers corrigen automáticamente este problema, pero no siempre. Por eso es importante revisar la malla cuando un modelo descargado o generado produce comportamientos extraños.

## 5. STL

**STL** es el formato más común en impresión 3D. Representa la superficie de un modelo mediante triángulos. Su popularidad se debe a que es simple, ampliamente compatible y aceptado por casi todos los slicers.

### Ventajas

- Muy compatible.
- Ligero en modelos simples.
- Fácil de exportar desde muchos programas.
- Adecuado para impresión básica.

### Limitaciones

- No conserva historial paramétrico.
- No almacena de forma robusta color, material o parámetros de impresión.
- Puede tener problemas de unidades.
- Convierte superficies curvas en aproximaciones triangulares.
- No conserva intención de diseño.

Un archivo STL puede ser suficiente para imprimir, pero no siempre es ideal para editar. Si se necesita modificar una pieza técnica, es mejor contar con el archivo fuente o con un formato CAD como STEP.

## 6. OBJ

**OBJ** es un formato frecuente en gráficos 3D, animación, escultura digital y modelos con textura. Puede almacenar información asociada a materiales visuales y coordenadas de textura.

### Ventajas

- Útil para modelos orgánicos.
- Puede incluir información visual.
- Compatible con Blender y otros programas de modelado.

### Limitaciones

- No siempre está optimizado para manufactura.
- Puede incluir elementos visuales innecesarios para impresión.
- Puede contener mallas complejas difíciles de reparar.

OBJ es útil cuando se trabaja con formas artísticas, escaneos o modelos visuales, pero para impresión técnica muchas veces se prefiere STL, 3MF o STEP.

## 7. 3MF

**3MF** es un formato más moderno creado específicamente para impresión 3D y manufactura aditiva. El 3MF Consortium lo presenta como un formato de fidelidad completa para impresión 3D y manufactura aditiva, diseñado para superar limitaciones de formatos existentes.

A diferencia de STL, 3MF puede almacenar más información en un solo archivo:

- geometría;
- unidades;
- materiales;
- colores;
- metadatos;
- información de proyecto;
- configuraciones de impresión, según el flujo de software;
- varios objetos en una misma escena.

### Ventajas

- Mejor manejo de unidades.
- Puede incluir varios objetos.
- Puede conservar más información del proyecto.
- Es práctico para compartir configuraciones de impresión.
- Es usado por slicers modernos.

### Limitaciones

- No todos los programas lo manejan igual.
- Puede incluir información dependiente de un ecosistema de software.
- No sustituye al archivo CAD original para edición paramétrica.

## 8. STEP y formatos CAD

Aunque no siempre se usa directamente para imprimir, **STEP** es importante porque conserva información geométrica CAD de mayor calidad que una malla triangulada. Es útil cuando se desea editar una pieza técnica con precisión.

Diferencia clave:

- STL describe una superficie triangulada.
- STEP describe geometría CAD más editable.

Para piezas funcionales, mecánicas o de ensamble, conviene conservar el archivo CAD original y exportar una malla solo al final.

## 9. Resolución de exportación

Cuando se exporta a STL, las superficies curvas se convierten en triángulos. Si la resolución es baja, las curvas se ven facetadas. Si la resolución es demasiado alta, el archivo puede volverse pesado sin aportar una mejora visible.

La exportación debe equilibrar:

- calidad geométrica;
- tamaño de archivo;
- capacidad del slicer;
- nivel de detalle necesario;
- tamaño real de la pieza.

## 10. Escala y unidades

Uno de los errores más comunes es abrir un archivo y encontrarlo demasiado grande o demasiado pequeño. Esto ocurre porque algunos formatos no almacenan unidades de forma explícita o porque el programa exportó en pulgadas y el slicer interpretó milímetros.

Antes de imprimir, siempre debe revisarse la escala real:

- largo;
- ancho;
- alto;
- diámetro de agujeros;
- espesor de paredes;
- distancia entre puntos de ensamble.

## 11. Errores frecuentes de archivo

| Problema | Descripción | Efecto posible |
|---|---|---|
| Agujeros | La malla no está cerrada | Capas faltantes |
| Normales invertidas | Caras apuntan hacia adentro | Superficies mal interpretadas |
| No-manifold | Geometría ambigua | Laminado incorrecto |
| Pared sin espesor | Superficie sin volumen | No se imprime o sale débil |
| Intersecciones internas | Objetos se cruzan | Trayectorias erróneas |
| Escala incorrecta | Unidades mal interpretadas | Pieza demasiado grande/pequeña |
| Exceso de polígonos | Malla demasiado densa | Archivo pesado y lento |
| Detalle demasiado fino | Elementos menores que la boquilla | Detalle perdido |

## 12. Criterios para aceptar un archivo antes de imprimir

Antes de enviar un modelo a imprimir, conviene revisar:

- que el archivo abra correctamente;
- que la escala sea correcta;
- que la base toque la cama;
- que la malla no tenga errores críticos;
- que las paredes tengan espesor suficiente;
- que los detalles sean imprimibles;
- que la orientación tenga sentido;
- que el slicer genere capas completas;
- que el tiempo y material sean razonables.

## 13. Por qué este tema importa en un FabLab

En un FabLab se reciben archivos de muchas fuentes: estudiantes, repositorios, escaneos, software CAD, IA generativa y modelos modificados. No todos los archivos están listos para imprimir. Enseñar a revisar mallas evita desperdicio de material, tiempos muertos y frustración.

Una cultura responsable de impresión 3D no consiste en imprimir cualquier STL que se descarga. Consiste en entender el archivo, revisar su geometría y tomar decisiones antes de ocupar la máquina.

## Referencias

[1] 3MF Consortium, “The File Format for 3D Printing.”  
[2] Library of Congress, “3D Manufacturing Format (3MF).”  
[3] Tinkercad Help Center, “Export filetypes.”

## Siguiente sección

[Modelado CAD: paramétrico y orgánico](modelado-cad.md)
