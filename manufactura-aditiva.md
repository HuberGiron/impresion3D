---
layout: default
title: Manufactura aditiva
nav_order: 2
---

# Manufactura aditiva e impresión 3D

La impresión 3D es el nombre popular de una familia de procesos de fabricación que construyen objetos físicos a partir de información digital. Estos procesos pertenecen a la **manufactura aditiva**, porque la pieza se forma agregando material en lugar de retirarlo de un bloque inicial.

**La impresión 3D cambió la manera de prototipar**. En la fabricación sustractiva, como el maquinado CNC, se parte de un bloque y se remueve material hasta obtener la forma deseada. En el moldeo por inyección, se fabrica primero un molde y después se producen muchas piezas iguales. En la manufactura aditiva, en cambio, se parte de un modelo digital y la máquina deposita, cura, solidifica o fusiona material solamente donde se necesita construir la pieza.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> comparación entre fabricación sustractiva, moldeo e impresión 3D. Archivo sugerido: <code>assets/img/intro/aditiva-sustractiva-moldeo.png</code>.
</div>

En su forma más común, una pieza impresa en 3D se construye por capas. El software divide el modelo en secciones horizontales muy delgadas y la máquina ejecuta esas secciones una por una. La acumulación de capas produce el volumen completo:

- La pieza queda condicionada por la dirección en la que se fabrican las capas.
- La resistencia no siempre es igual en todas las direcciones.
- La calidad superficial depende de la altura de capa, la orientación y el material.
- Algunas geometrías necesitan soportes temporales.
- La precisión final depende de la máquina, el material, la temperatura y el archivo digital.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> imagen de impresora 3d imprimiendo por capas y sus propiedades. Archivo sugerido: <code>assets/img/intro/capas.png</code>.
</div>

## 2. Impresión 3D como herramienta de democratización tecnológica

La palabra “democratización” no significa que la tecnología sea trivial. Significa que más personas pueden acceder a procesos que antes estaban reservados para laboratorios industriales o empresas con maquinaria especializada.

Una impresora 3D de escritorio permite que un estudiante fabrique una carcasa para electrónica, que un profesor produzca modelos didácticos, que un diseñador valide una forma ergonómica, que un equipo de robótica fabrique soportes para sensores o que una persona adapte un objeto a una necesidad específica.

El valor de la impresión 3D en un FabLab está en cinco aspectos:

1. **Acceso:** permite fabricar sin depender siempre de proveedores externos.
2. **Velocidad de iteración:** facilita probar muchas versiones de una idea.
3. **Personalización:** permite producir piezas ajustadas a una necesidad concreta.
4. **Aprendizaje:** hace visible la relación entre diseño, material, proceso y resultado.
5. **Cultura de colaboración:** se apoya en repositorios, comunidades y documentación abierta.

La impresión 3D no elimina la necesidad de conocimiento técnico. Al contrario, lo hace más visible. Cuando una pieza falla, el problema puede estar en el diseño, la orientación, el material, la temperatura, la humedad del filamento, el laminado o el estado mecánico de la impresora. Aprender impresión 3D es aprender a leer esa cadena completa.

## 3. Flujo general de trabajo

Aunque existen diferentes tecnologías de impresión 3D, el flujo general suele mantener una estructura común:

```text
Idea → Modelo 3D → Archivo imprimible → Laminado → Impresión → Postprocesado → Evaluación
```

### 3.1 Idea o necesidad

Todo inicia con una intención: fabricar una pieza, representar una geometría, resolver una necesidad, reparar un objeto, crear un prototipo o producir un modelo didáctico.

En un contexto de FabLab, muchas impresiones nacen de necesidades pequeñas pero valiosas: un soporte para cámara, una carcasa para ESP32, una pieza de ajuste, una cubierta, una perilla, un adaptador, una guía, un organizador o un prototipo de mecanismo.

### 3.2 Modelo digital

La pieza debe existir como modelo tridimensional. Puede diseñarse en CAD, descargarse de un repositorio, obtenerse por escaneo 3D o generarse con apoyo de inteligencia artificial.

El modelo digital debe tener forma, escala y volumen. Para impresión 3D no basta que un objeto se vea bien en pantalla: debe poder interpretarse como un sólido fabricable.

### 3.3 Archivo imprimible

El modelo se exporta normalmente como STL, OBJ o 3MF. Estos formatos describen la geometría de la pieza, generalmente como una malla formada por triángulos.

### 3.4 Laminado

El software laminador, también llamado slicer, divide el modelo en capas y genera las trayectorias que la impresora debe seguir. En este paso se definen parámetros como altura de capa, porcentaje de relleno, temperatura, soportes, velocidad y orientación.

### 3.5 Impresión

La máquina ejecuta las instrucciones. En FDM, deposita filamento fundido. En resina, solidifica un fotopolímero. En SLS, fusiona polvo. Aunque la lógica de control varía, todas las tecnologías comparten la idea de construir la pieza a partir de información digital.

### 3.6 Postprocesado

Después de imprimir, puede ser necesario retirar soportes, lijar, curar, lavar, ensamblar, insertar tornillos, pintar o verificar dimensiones.

### 3.7 Evaluación

La pieza se revisa de acuerdo con su propósito: apariencia, dimensiones, ajuste, resistencia, flexibilidad, ergonomía o función mecánica.

## 4. Diferencia con otros procesos de fabricación

| Proceso | Cómo fabrica | Ventaja principal | Limitación principal |
|---|---|---|---|
| Impresión 3D | Agrega material capa por capa | Prototipos y personalización | Tiempo por pieza y anisotropía |
| CNC | Retira material de un bloque | Precisión y materiales sólidos | Desperdicio y necesidad de herramienta |
| Inyección de plástico | Llena un molde con polímero fundido | Producción masiva | Alto costo inicial de molde |
| Corte láser | Corta o graba material plano | Rapidez en 2D | Limitado a láminas |
| Termoformado | Deforma lámina caliente sobre molde | Bajo costo para formas simples | Geometría limitada |

Esta comparación ayuda a ubicar la impresión 3D en su lugar correcto. No es la mejor tecnología para todo, pero es extraordinaria cuando el objetivo es explorar, iterar, personalizar o fabricar pocas piezas con geometrías específicas.

## 5. Ventajas técnicas y educativas

La impresión 3D tiene valor técnico porque conecta distintas áreas del conocimiento:

- diseño geométrico;
- ciencia de materiales;
- control de movimiento;
- transferencia de calor;
- electrónica;
- software;
- mecánica;
- manufactura;
- documentación técnica.

También tiene valor educativo porque transforma conceptos abstractos en objetos manipulables. Una superficie matemática, una molécula, una pieza mecánica, un robot, una prótesis didáctica o una estructura arquitectónica pueden imprimirse y discutirse físicamente.

## 6. Limitaciones que conviene conocer desde el inicio

Invitar a usar la tecnología no significa ocultar sus límites. La impresión 3D tiene restricciones reales:

- Las piezas FDM suelen mostrar líneas de capa.
- La resistencia entre capas puede ser menor que dentro de una misma capa.
- La calidad depende mucho de la orientación de impresión.
- No todas las geometrías se imprimen sin soportes.
- Los materiales tienen comportamiento térmico y mecánico diferente.
- La humedad puede degradar el filamento.
- La repetibilidad requiere mantenimiento y perfiles bien configurados.
- La producción masiva sigue favoreciendo procesos como inyección de plástico.

Conocer estos límites mejora el uso de la tecnología. Una persona que entiende las restricciones de impresión diseña mejores piezas, desperdicia menos material y obtiene resultados más consistentes.

## 7. La impresión 3D dentro del ecosistema FabLab

Un FabLab no es solamente un espacio con máquinas. Es un entorno donde se combinan diseño, fabricación, documentación y aprendizaje colaborativo. En ese contexto, la impresora 3D cumple una función especial: es una puerta de entrada rápida a la fabricación digital.

A diferencia de una CNC o una cortadora láser, la impresora 3D suele requerir menos preparación inicial para fabricar una primera pieza. Esto la hace atractiva para nuevos usuarios. Sin embargo, su aparente facilidad puede ocultar la complejidad del proceso. Por eso es importante que el curso explique no solo “qué botón presionar”, sino qué decisiones técnicas están detrás de una buena impresión.

## Referencias

[1] ISO, “ISO/ASTM 52900: Additive manufacturing — General principles — Fundamentals and vocabulary.”  
[2] Stratasys, “FDM 3D Printing – Fused Deposition Modeling.”  
[3] NIOSH, “3D Printing with Filaments: Health and Safety Questions to Ask.”

## Siguiente sección

[Historia y popularización](historia-popularizacion.md)
