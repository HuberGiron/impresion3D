---
layout: default
title: Escaneo 3D
nav_exclude: true
---

# Escaneo 3D

El escaneo 3D permite capturar la forma de un objeto físico y convertirla en información digital. Es una tecnología complementaria a la impresión 3D porque permite invertir el flujo habitual: en lugar de diseñar primero en la computadora, se parte de un objeto existente y se obtiene un modelo que puede medirse, editarse, modificar o imprimir.

En un FabLab, el escaneo 3D es útil para documentación, reproducción, adaptación, ergonomía, restauración, investigación y enseñanza. Sin embargo, escanear un objeto no significa obtener automáticamente un archivo listo para imprimir. Entre la captura y la impresión suele existir una etapa de limpieza, reconstrucción y reparación de malla.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> flujo de escaneo 3D a impresión: objeto físico → captura → nube de puntos → malla → reparación → slicer. Archivo sugerido: <code>assets/img/escaneo/flujo-escaneo-3d.png</code>.
</div>

## 1. Qué es escanear en 3D

Escanear en 3D consiste en medir la geometría de una superficie desde distintos puntos de vista. El resultado inicial puede ser una nube de puntos, una malla o una combinación de geometría y textura.

Dependiendo de la tecnología, el sistema puede capturar:

- forma;
- color;
- textura;
- escala;
- profundidad;
- detalles superficiales.

El archivo resultante normalmente requiere procesamiento antes de ser útil para impresión.

## 2. Nube de puntos

Una nube de puntos es un conjunto de coordenadas en el espacio que representan muestras de la superficie del objeto. Cada punto indica una posición medida, pero por sí solo no forma una superficie continua.

Para imprimir, la nube de puntos debe convertirse en una malla. Este proceso se llama reconstrucción.

## 3. Malla reconstruida

La malla reconstruida conecta los puntos para formar caras. En esta etapa pueden aparecer errores:

- huecos;
- superficies rugosas;
- ruido;
- zonas deformadas;
- geometría duplicada;
- partes flotantes;
- detalles falsos.

Una buena reconstrucción depende de la calidad de la captura, iluminación, textura del objeto, número de vistas y algoritmo usado.

## 4. Métodos de escaneo 3D

### 4.1 Fotogrametría

La fotogrametría reconstruye geometría a partir de muchas fotografías tomadas alrededor del objeto. El software identifica puntos comunes entre imágenes y calcula la forma tridimensional.

Ventajas:

- puede realizarse con cámara o teléfono;
- bajo costo de entrada;
- útil para objetos grandes;
- puede capturar textura visual.

Limitaciones:

- requiere buena iluminación;
- falla con objetos brillantes, transparentes o poco texturizados;
- puede tener baja precisión dimensional;
- necesita muchas fotografías;
- requiere procesamiento posterior.

### 4.2 Luz estructurada

Los escáneres de luz estructurada proyectan patrones sobre el objeto y analizan cómo se deforman esos patrones sobre la superficie.

Ventajas:

- buena precisión;
- captura rápida;
- adecuado para objetos medianos y pequeños;
- útil para ergonomía y digitalización.

Limitaciones:

- puede fallar con superficies brillantes o transparentes;
- requiere calibración;
- el equipo puede ser costoso;
- el objeto debe estar estable.

### 4.3 LiDAR

LiDAR mide distancia mediante luz láser o sensores de profundidad. Algunos teléfonos y tabletas modernos incluyen sensores de profundidad que permiten capturas rápidas.

Ventajas:

- útil para espacios, objetos grandes y geometría general;
- captura rápida;
- buena integración móvil.

Limitaciones:

- menor detalle fino que otros métodos;
- no siempre es adecuado para piezas pequeñas;
- puede requerir limpieza significativa.

### 4.4 Escáneres de escritorio

Son equipos diseñados para capturar objetos pequeños o medianos, a veces con plataforma giratoria.

Ventajas:

- flujo más controlado;
- buena repetibilidad;
- útiles para educación y laboratorio.

Limitaciones:

- tamaño limitado de objeto;
- costo variable;
- todavía requieren limpieza de malla.

## 5. Flujo de escaneo a impresión

```text
Objeto físico → Captura → Alineación → Nube de puntos → Malla → Limpieza → Reparación → Escala → Laminado → Impresión
```

### 5.1 Captura

Se toman fotografías, mediciones o vistas 3D desde distintos ángulos. Es importante cubrir toda la superficie.

### 5.2 Alineación

El software alinea las distintas capturas para formar un modelo coherente.

### 5.3 Reconstrucción

Los datos se convierten en una malla continua.

### 5.4 Limpieza

Se eliminan elementos no deseados: mesa, fondo, ruido, partes flotantes o geometría duplicada.

### 5.5 Reparación

Se cierran agujeros, se corrigen normales, se reduce ruido y se verifica que la malla sea imprimible.

### 5.6 Escalado

Se confirma que el modelo tenga dimensiones reales correctas.

### 5.7 Laminado

El modelo se abre en el slicer y se prepara como cualquier otro archivo de impresión.

## 6. Limitaciones prácticas

El escaneo 3D no es una copiadora perfecta. Algunas superficies son difíciles de capturar:

- objetos transparentes;
- objetos brillantes;
- superficies negras o muy oscuras;
- piezas con cavidades internas;
- objetos muy delgados;
- superficies repetitivas sin textura;
- objetos en movimiento.

Para mejorar la captura se puede usar luz difusa, marcadores, spray matizante o fondos contrastantes, siempre considerando seguridad y conservación del objeto.

## 7. Escaneo 3D para reparación y adaptación

Uno de los usos más interesantes del escaneo en un FabLab es adaptar piezas a objetos existentes. Por ejemplo:

- diseñar una carcasa que se ajuste a una forma irregular;
- crear un soporte para un objeto ya fabricado;
- documentar una pieza rota;
- capturar una geometría ergonómica;
- generar una base para rediseñar una pieza en CAD.

En estos casos, el escaneo no necesariamente produce la pieza final. Puede servir como referencia geométrica para diseñar una pieza nueva.

## 8. Escaneo 3D e impresión: criterio técnico

Antes de imprimir un modelo escaneado debe revisarse:

- ¿tiene escala correcta?
- ¿la malla está cerrada?
- ¿hay detalles demasiado finos?
- ¿la base es imprimible?
- ¿hay zonas flotantes?
- ¿se requiere cortar el modelo?
- ¿necesita soportes?
- ¿el archivo es demasiado pesado?
- ¿el modelo representa una superficie o un volumen?

## 9. Uso educativo

El escaneo 3D es excelente para discutir la relación entre mundo físico y mundo digital. Permite mostrar que digitalizar no es simplemente tomar una foto en 3D: implica medir, interpretar, reconstruir y corregir.

En una clase tipo lecture, este tema permite conectar impresión 3D con visión computacional, geometría, diseño, patrimonio, medicina, ingeniería inversa y realidad aumentada.

## Referencias

[1] NIH 3D, “Open community-driven portal for bioscientific and medical 3D models.”  
[2] MeshLab Documentation, “Mesh processing system.”  
[3] Blender Manual, “Mesh editing.”

## Siguiente sección

[Inteligencia artificial y modelos 3D](inteligencia-artificial-3d.md)
