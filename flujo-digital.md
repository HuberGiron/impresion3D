---
layout: default
title: Flujo digital
nav_order: 8
---

# Flujo digital de impresión 3D

La impresión 3D no inicia cuando la máquina comienza a moverse. Inicia mucho antes, en el modelo digital y en las decisiones que se toman para convertir una geometría en una pieza fabricable.

El flujo digital conecta tres mundos: el diseño, el software de preparación y la máquina física. Comprender este flujo evita muchos errores comunes. Una pieza puede fallar no porque la impresora sea mala, sino porque el archivo tiene problemas, la orientación no es adecuada, los soportes están mal configurados o el material seleccionado no corresponde a la aplicación.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> flujo completo desde idea hasta pieza impresa. Archivo sugerido: <code>assets/img/flujo/flujo-digital-impresion-3d.png</code>.
</div>

## 1. De la idea al archivo

El proceso inicia con una necesidad. Esta necesidad puede resolverse de varias formas:

- diseñando una pieza desde cero;
- modificando un archivo existente;
- descargando un modelo de un repositorio;
- escaneando un objeto físico;
- generando una propuesta con inteligencia artificial;
- combinando varias fuentes.

La fuente del modelo importa porque determina qué tan editable, preciso y confiable será el archivo.

## 2. Modelo nativo

El modelo nativo es el archivo original del software de diseño. Puede ser un archivo de Fusion, SolidWorks, FreeCAD, Blender, Tinkercad, Onshape u otro entorno.

Este archivo suele conservar información editable, como operaciones paramétricas, bocetos, sólidos, historial o modificadores. Es el archivo más valioso cuando se necesita modificar una pieza de manera controlada.

## 3. Exportación

Para imprimir, el modelo se exporta a un formato que el laminador pueda interpretar. Los formatos más comunes son:

- STL;
- OBJ;
- 3MF.

En algunos flujos se trabaja también con STEP cuando se desea conservar geometría CAD para edición, aunque no todos los slicers lo aceptan de la misma forma.

Exportar no es un paso menor. Durante la exportación se define cómo se aproxima la geometría, cuántos triángulos tendrá la malla, qué unidades se usarán y qué información se conservará.

## 4. Revisión del archivo

Antes de laminar conviene revisar:

- escala;
- orientación;
- unidades;
- si la pieza está cerrada;
- si hay errores de malla;
- si existen detalles demasiado pequeños;
- si las paredes tienen espesor suficiente;
- si el objeto realmente toca la cama;
- si hay partes flotantes;
- si la geometría está duplicada.

Un error frecuente es asumir que “si se ve bien, se imprime bien”. En impresión 3D eso no siempre es cierto. Un modelo puede verse correcto en pantalla y aun así tener geometría no imprimible.

## 5. Laminado

El laminador o slicer convierte el modelo 3D en instrucciones para la impresora. Hace mucho más que “cortar” el objeto. Calcula trayectorias, velocidades, temperaturas, ventilación, retracciones, soportes, relleno y tiempos.

El slicer responde preguntas como:

- ¿Cuántas capas tendrá la pieza?
- ¿Dónde empieza cada perímetro?
- ¿Qué zonas llevan relleno?
- ¿Qué partes necesitan soporte?
- ¿A qué temperatura se imprime?
- ¿Qué velocidad debe usarse?
- ¿Cuánto material se consumirá?
- ¿Cuánto tiempo tomará?

## 6. Vista previa

La vista previa del slicer es una de las herramientas más importantes. Permite ver la impresión por capas antes de gastar tiempo y material.

En la vista previa deben revisarse:

- primera capa;
- soportes;
- trayectorias de perímetro;
- relleno;
- puentes;
- zonas delgadas;
- tiempo por capa;
- cambios de material;
- costura Z;
- movimientos de viaje.

Muchas fallas pueden detectarse antes de imprimir si se revisa cuidadosamente la vista previa.

## 7. Generación de instrucciones

Después del laminado, el software genera instrucciones para la impresora. En muchas impresoras FDM estas instrucciones se expresan como **G-code**, un lenguaje de comandos que indica movimientos, temperaturas y acciones de máquina.

En ecosistemas modernos, el archivo puede empaquetarse con información adicional del proyecto, perfiles, miniaturas, metadatos o instrucciones específicas del fabricante.

## 8. Transferencia a la impresora

La transferencia puede hacerse por:

- tarjeta SD;
- memoria USB;
- red local;
- nube del fabricante;
- conexión directa;
- aplicación móvil;
- software de control.

Cada opción tiene implicaciones de comodidad, control y privacidad. En un entorno académico conviene documentar qué flujo se usará para evitar confusión entre usuarios.

## 9. Impresión y observación

Durante la impresión, la primera capa merece atención especial. Si la primera capa está mal adherida, la impresión completa está en riesgo.

También conviene observar:

- flujo de material;
- sonidos inusuales;
- vibración;
- deformaciones;
- acumulación de material en boquilla;
- desprendimiento;
- fallas de soporte;
- comportamiento del filamento.

## 10. Postprocesado

El postprocesado depende de la tecnología y la pieza:

- retirar soportes;
- cortar rebabas;
- lijar;
- perforar;
- insertar tornillos;
- instalar insertos térmicos;
- pegar piezas;
- pintar;
- lavar y curar, en resina;
- limpiar polvo, en SLS.

## 11. Evaluación

Una impresión no se evalúa solo por verse bonita. Debe evaluarse según su propósito.

Criterios posibles:

- dimensiones;
- ajuste;
- resistencia;
- acabado;
- estabilidad;
- ergonomía;
- peso;
- rigidez;
- facilidad de ensamble;
- fidelidad al diseño.

## 12. Flujo resumido

```text
1. Definir necesidad
2. Obtener o diseñar modelo 3D
3. Exportar STL / OBJ / 3MF
4. Revisar malla y escala
5. Abrir en slicer
6. Configurar material, impresora y parámetros
7. Revisar vista previa por capas
8. Generar instrucciones
9. Enviar a impresora
10. Supervisar primera capa
11. Retirar y postprocesar
12. Evaluar resultado
```

## 13. Dónde se cometen más errores

Los errores más comunes del flujo no ocurren en un solo punto. Pueden aparecer en distintas etapas:

| Etapa | Error frecuente | Consecuencia |
|---|---|---|
| Modelado | Paredes sin espesor | Pieza no imprimible |
| Exportación | Escala incorrecta | Pieza demasiado grande o pequeña |
| Malla | Normales invertidas | Superficies mal interpretadas |
| Laminado | Soportes mal configurados | Colapso o marcas excesivas |
| Material | Temperatura incorrecta | Mala adhesión o stringing |
| Impresión | Primera capa deficiente | Desprendimiento |
| Postprocesado | Retiro brusco de soportes | Pieza rota o marcada |

## Referencias

[1] Bambu Lab, “Bambu Studio.”  
[2] 3MF Consortium, “The File Format for 3D Printing.”  
[3] Marlin Firmware, “G-code.”

## Siguiente sección

[Archivos 3D y mallas](archivos-mallas.md)
