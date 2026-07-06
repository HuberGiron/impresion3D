---
layout: default
title: Tecnología FDM / FFF
nav_order: 5
---

# Tecnología FDM / FFF

La tecnología **FDM / FFF** es la forma de impresión 3D más común en entornos educativos, FabLabs, makerspaces y prototipado de escritorio. Su principio general es sencillo de observar: una impresora toma un filamento termoplástico, lo calienta hasta volverlo fluido y lo deposita sobre una superficie siguiendo trayectorias calculadas por software.

La aparente sencillez del proceso es una de sus fortalezas. Una persona puede ver cómo la máquina fabrica capa por capa y relacionar directamente las decisiones de diseño con el resultado físico. Al mismo tiempo, detrás de una impresión correcta intervienen fenómenos de temperatura, flujo, adhesión, contracción, movimiento, enfriamiento y geometría.

<div class="placeholder">
<strong>Espacio sugerido para imagen:</strong> esquema general de una impresora FDM con sus partes principales. Archivo sugerido: <code>assets/img/fdm/partes-impresora-fdm.png</code>.
</div>

## 1. Principio de funcionamiento

Una impresora FDM construye la pieza depositando material fundido. El material llega a la máquina en forma de filamento, normalmente de 1.75 mm de diámetro. El extrusor empuja el filamento hacia el hotend, donde se calienta. El material fundido sale por una boquilla y se deposita sobre la cama de impresión.

La pieza se genera en capas. Después de completar una capa, la máquina avanza en el eje Z y deposita la siguiente. El proceso se repite hasta completar el objeto.

```text
Filamento → Extrusor → Hotend → Boquilla → Capa depositada → Pieza completa
```

## 2. Partes principales de una impresora FDM

### 2.1 Chasis o estructura

El chasis sostiene todos los componentes. Debe ser rígido para evitar vibraciones, desalineaciones y errores de movimiento. Una estructura flexible o mal ensamblada puede producir superficies con ondas, capas desplazadas o baja repetibilidad.

### 2.2 Sistema de movimiento

El sistema de movimiento posiciona la boquilla y la cama. Puede usar bandas, poleas, motores paso a paso, husillos, guías lineales, ruedas, rieles o varillas.

Las arquitecturas más comunes son:

- **Cartesiana tipo cama móvil:** la cama se mueve en un eje y el cabezal en otros.
- **CoreXY:** el cabezal se mueve en X/Y mediante una combinación de bandas.
- **Delta:** tres torres coordinan el movimiento del efector.
- **Cantilever:** estructura ligera, común en algunas impresoras compactas.

Cada arquitectura tiene ventajas y compromisos. En impresoras de escritorio modernas, la estabilidad mecánica, el control de vibración y la calibración automática han mejorado mucho la experiencia del usuario.

### 2.3 Extrusor

El extrusor es el mecanismo que empuja el filamento. Usa engranes o ruedas moleteadas para sujetar el material y moverlo con precisión.

Existen dos configuraciones comunes:

- **Extrusor directo:** el motor del extrusor está cerca del hotend. Suele funcionar mejor con materiales flexibles porque el recorrido del filamento es corto.
- **Bowden:** el extrusor está separado del hotend y empuja el filamento a través de un tubo. Reduce masa en el cabezal, pero puede complicar materiales flexibles y ajustes de retracción.

### 2.4 Hotend

El hotend es la zona donde el filamento se calienta y funde. Incluye elementos como bloque calefactor, cartucho calefactor, termistor, disipador, garganta térmica y boquilla.

Un buen hotend debe fundir el material de forma estable sin permitir que el calor suba demasiado hacia la zona fría. Si el calor se propaga de manera inadecuada, puede aparecer un atasco por ablandamiento prematuro del filamento.

### 2.5 Boquilla

La boquilla define el diámetro de salida del material. La medida más común en impresoras de escritorio es 0.4 mm, aunque existen boquillas de 0.2, 0.6, 0.8 mm y otras medidas.

Una boquilla pequeña permite más detalle, pero aumenta el tiempo de impresión y puede obstruirse con más facilidad. Una boquilla grande imprime más rápido y produce piezas robustas, pero reduce detalle fino.

### 2.6 Cama de impresión

La cama es la superficie sobre la que se deposita la primera capa. Puede estar caliente para mejorar la adhesión y reducir deformaciones. La primera capa es crítica: si no se adhiere bien, la impresión puede fallar aunque el resto de los parámetros sean correctos.

### 2.7 Ventiladores

Los ventiladores cumplen dos funciones principales:

- enfriar el disipador del hotend;
- enfriar la pieza recién depositada.

El enfriamiento de pieza es especialmente importante en PLA y en geometrías pequeñas. Sin embargo, demasiado enfriamiento puede afectar la adhesión entre capas en materiales técnicos.

### 2.8 Sensores y electrónica

Las impresoras modernas pueden incluir:

- sensores de fin de carrera;
- sensores de nivelación;
- sensores de filamento;
- sensores de temperatura;
- acelerómetros para compensación de vibración;
- cámaras;
- detección de fallas.

Estos sistemas facilitan el uso, pero no sustituyen la comprensión del proceso.

## 3. Anatomía de una pieza FDM

Una pieza impresa por FDM no es un sólido macizo uniforme, salvo que se configure así. Normalmente se compone de regiones internas y externas con funciones distintas.

<div class="placeholder">
<strong>Espacio sugerido para diagrama:</strong> corte de una pieza FDM mostrando paredes, top, bottom, infill, soportes y costura Z. Archivo sugerido: <code>assets/img/fdm/anatomia-pieza-fdm.png</code>.
</div>

### 3.1 Perímetros o paredes

Los perímetros forman el contorno externo de la pieza. Aumentar el número de perímetros suele mejorar la resistencia más que aumentar solamente el porcentaje de relleno, especialmente en piezas sometidas a carga.

### 3.2 Capas superiores e inferiores

Las capas superiores cierran la pieza por arriba; las inferiores forman la base. Si son insuficientes, pueden aparecer huecos, superficies débiles o patrones de relleno visibles.

### 3.3 Relleno o infill

El infill es la estructura interna. Puede ser rectilíneo, triangular, cúbico, gyroid, panal u otros patrones. Su función es aportar soporte interno, rigidez y resistencia, sin llenar todo el volumen con material.

### 3.4 Soportes

Los soportes son estructuras temporales generadas para sostener zonas que no pueden imprimirse en el aire. Después se retiran. Son útiles, pero consumen material, aumentan tiempo y pueden dejar marcas en la pieza.

### 3.5 Costura Z

La costura Z es la zona donde inicia o termina una trayectoria de perímetro. Puede verse como una línea vertical o puntos repetidos. No siempre puede eliminarse, pero puede ubicarse estratégicamente en zonas menos visibles.

## 4. Variables físicas del proceso

### 4.1 Temperatura de boquilla

La temperatura debe permitir que el material fluya correctamente. Si es demasiado baja, puede haber subextrusión, mala adhesión entre capas o boquilla tapada. Si es demasiado alta, puede aparecer stringing, deformación, pérdida de detalle o degradación del material.

### 4.2 Temperatura de cama

La cama caliente mejora la adhesión y reduce contracción. PLA puede imprimirse con cama moderada; ABS y ASA requieren mayor control térmico. Una cama demasiado caliente puede producir deformaciones en la base, conocidas como elephant foot.

### 4.3 Velocidad

La velocidad afecta tiempo, calidad y confiabilidad. Imprimir más rápido no siempre significa imprimir mejor. A velocidades altas pueden aparecer vibraciones, capas inconsistentes, pérdida de detalle o mala adhesión.

### 4.4 Flujo

El flujo indica cuánto material se extruye respecto a lo esperado. Un flujo incorrecto produce paredes demasiado delgadas, exceso de material, superficies rugosas o dimensiones inexactas.

### 4.5 Enfriamiento

El enfriamiento controla qué tan rápido solidifica el plástico. En PLA suele ser útil usar bastante ventilación. En materiales como ABS, demasiado enfriamiento puede aumentar deformaciones y separación entre capas.

### 4.6 Adhesión a la cama

La adhesión depende de la superficie, limpieza, temperatura, distancia inicial de boquilla, material y geometría de la pieza. Una mala primera capa es una de las causas más comunes de falla.

### 4.7 Humedad del filamento

Muchos filamentos absorben humedad. Cuando un filamento húmedo pasa por el hotend, el agua puede vaporizarse y generar burbujas, sonido de chisporroteo, superficies rugosas, hilos y pérdida de resistencia.

## 5. Parámetros visibles en el resultado

| Parámetro | Efecto principal | Si se configura mal |
|---|---|---|
| Altura de capa | Resolución vertical y tiempo | Superficie escalonada o tiempo excesivo |
| Temperatura | Flujo y adhesión entre capas | Stringing, subextrusión, degradación |
| Velocidad | Tiempo y calidad dinámica | Vibración, pérdida de detalle |
| Infill | Rigidez interna | Pieza débil o uso excesivo de material |
| Perímetros | Resistencia externa | Paredes frágiles |
| Soportes | Imprimibilidad de voladizos | Marcas, exceso de material |
| Orientación | Resistencia, acabado y soportes | Fallas mecánicas o mala superficie |

## 6. Fortalezas de FDM en un FabLab

FDM es especialmente útil porque permite fabricar objetos reales con materiales económicos y máquinas relativamente accesibles. No requiere moldes, no requiere herramientas de corte y permite que usuarios nuevos observen el proceso de construcción.

En un FabLab, FDM destaca para:

- carcasas de electrónica;
- soportes para sensores;
- piezas de robótica;
- maquetas de mecanismos;
- modelos anatómicos o didácticos;
- adaptadores personalizados;
- organizadores y herramientas auxiliares;
- validación de volumen y ergonomía;
- prototipos de producto.

## 7. Limitaciones de FDM

FDM también tiene restricciones importantes:

- Las piezas pueden romperse entre capas.
- Los detalles muy pequeños pueden no salir bien.
- Las superficies inclinadas muestran escalones.
- Las piezas largas pueden deformarse por contracción.
- Los soportes pueden dejar marcas.
- La precisión de agujeros y ensambles requiere compensaciones.
- Algunas piezas necesitan rediseñarse para ser imprimibles.

Una buena impresión FDM no depende solo de tener una buena máquina. Depende de entender la relación entre diseño, orientación, material y configuración.

## 8. FDM como tecnología didáctica

Una de las razones por las que FDM es tan valiosa en educación es que hace visible el proceso de fabricación. El usuario puede observar cómo una trayectoria se convierte en pared, cómo el relleno sostiene la parte superior, cómo un voladizo necesita soporte o cómo una mala primera capa arruina la pieza.

La tecnología invita a aprender de manera directa. Cada impresión es una conversación entre el modelo digital y el comportamiento físico del material.

## Referencias

[1] Stratasys, “FDM 3D Printing – Fused Deposition Modeling.”  
[2] Prusa Research, “Layers and perimeters.”  
[3] UltiMaker, “Cura infill settings.”

## Siguiente sección

[Materiales para impresión 3D](materiales.md)
