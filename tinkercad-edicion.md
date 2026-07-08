---
layout: default
title: Tinkercad y edición básica
nav_exclude: true
---

# Tinkercad y edición básica

Tinkercad es una herramienta web de diseño 3D desarrollada por Autodesk. Es especialmente útil para introducir a nuevos usuarios al modelado tridimensional porque funciona desde el navegador y utiliza una lógica visual basada en formas simples.

Aunque Tinkercad no sustituye a un CAD paramétrico avanzado, es muy valioso en un FabLab porque permite crear y modificar piezas rápidamente. Para usuarios principiantes, ofrece una entrada directa al diseño 3D sin instalar software pesado ni aprender interfaces industriales complejas.

<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> captura de la interfaz de Tinkercad con plano de trabajo y figuras básicas. Archivo sugerido: <code>assets/img/tinkercad/interfaz-tinkercad.png</code>.
</div>

## 1. Qué tipo de herramienta es Tinkercad

Tinkercad trabaja principalmente con sólidos básicos. El usuario arrastra formas al plano de trabajo, las escala, rota, alinea, agrupa y combina.

La lógica central es la **geometría sólida constructiva**:

- sumar formas;
- restar huecos;
- agrupar objetos;
- alinear geometrías;
- modificar dimensiones.

Esto permite crear muchas piezas útiles sin dominar CAD avanzado.

## 2. Operaciones principales

### 2.1 Crear sólidos

Tinkercad incluye formas básicas como cubos, cilindros, esferas, conos, textos y figuras predefinidas. A partir de estas formas se pueden construir objetos más complejos.

### 2.2 Escalar

Cada objeto puede cambiar de tamaño en X, Y y Z. Es importante revisar unidades y dimensiones reales antes de exportar.

### 2.3 Rotar

La rotación permite orientar objetos en el espacio. Es útil para crear ángulos, inclinaciones o acomodar piezas antes de exportar.

### 2.4 Alinear

La herramienta de alineación es fundamental para centrar agujeros, posicionar textos, distribuir formas y crear piezas simétricas.

### 2.5 Agrupar

Agrupar convierte varias formas en un solo objeto compuesto. Si algunas formas están definidas como huecos, al agrupar se restan del sólido principal.

### 2.6 Huecos

Un hueco es una forma que elimina material. Es útil para perforaciones, cavidades, ranuras y cortes.

## 3. Importar archivos STL

Tinkercad permite importar archivos STL para modificarlos. Esto es útil cuando se descarga una pieza de un repositorio y se desea agregar texto, hacer un agujero, cortar una zona o combinarla con otra geometría.

Limitaciones importantes:

- archivos muy pesados pueden no importarse bien;
- la malla puede simplificarse;
- no se recupera el historial paramétrico;
- modificar detalles finos puede ser difícil;
- no todos los STL son adecuados para edición.

## 4. Exportar para impresión 3D

La documentación de Tinkercad recomienda usar STL cuando se exporta para impresión 3D. STL es ampliamente usado en prototipado rápido, impresión 3D y manufactura asistida por computadora.

Flujo típico:

```text
Diseño en Tinkercad → Exportar STL → Abrir en slicer → Laminar → Imprimir
```

También puede exportarse OBJ o SVG según el tipo de trabajo, pero para impresión 3D básica STL es la opción más común.

## 5. Qué se puede hacer bien en Tinkercad

Tinkercad es adecuado para:

- llaveros;
- placas con texto;
- soportes simples;
- cajas básicas;
- adaptadores sencillos;
- bases;
- figuras educativas;
- modificaciones rápidas de STL;
- modelos didácticos;
- primeras experiencias de diseño 3D.

## 6. Qué no conviene hacer en Tinkercad

Para piezas complejas puede quedarse corto. No es ideal para:

- ensambles mecánicos avanzados;
- historial paramétrico detallado;
- superficies orgánicas complejas;
- tolerancias de ingeniería exigentes;
- piezas con muchas relaciones entre dimensiones;
- dibujos técnicos formales;
- diseño de mecanismos complejos.

En esos casos conviene migrar a FreeCAD, Fusion, Onshape, SolidWorks u otro entorno CAD.

## 7. Tinkercad como herramienta de entrada al FabLab

Tinkercad es excelente para iniciar a usuarios nuevos porque reduce la distancia entre una idea y un archivo imprimible. Permite que una persona comprenda rápidamente conceptos como escala, volumen, agujero, alineación y exportación.

Su valor no está en ser el software más poderoso, sino en hacer que el diseño 3D sea accesible.

## 8. Buenas prácticas al usar Tinkercad

- Trabajar siempre con dimensiones reales.
- Usar la regla para medir.
- Agrupar cuidadosamente.
- Revisar que los huecos atraviesen completamente si se busca perforar.
- Evitar detalles más pequeños que la boquilla.
- Revisar la escala después de importar STL.
- Exportar versiones con nombres claros.
- Guardar una copia editable del diseño.

## 9. De Tinkercad a CAD avanzado

Tinkercad puede ser el primer escalón. Después de comprender sólidos, huecos y escala, el usuario puede pasar a CAD paramétrico. La transición natural consiste en aprender:

- bocetos 2D;
- restricciones;
- cotas;
- extrusión;
- revolución;
- ensambles;
- exportación STEP/STL.

En un FabLab, esta progresión permite acompañar a usuarios desde modelos simples hasta piezas técnicas.

## Referencias

[1] Autodesk Tinkercad, “Tinkercad.”  
[2] Tinkercad Help Center, “Export filetypes.”

## Siguiente sección

[Slicers y laminado](slicers-laminado.md)
