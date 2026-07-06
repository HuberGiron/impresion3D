---
layout: default
title: Fallas y calidad
nav_order: 18
---

# Fallas, calidad y diagnóstico

Las fallas de impresión 3D son parte normal del aprendizaje. Una pieza fallida no debe verse solamente como desperdicio, sino como evidencia del proceso. Cada defecto comunica algo sobre material, máquina, archivo, parámetros u orientación.

En un FabLab, enseñar a diagnosticar fallas es tan importante como enseñar a imprimir. Un usuario que reconoce una mala primera capa, humedad en filamento o falta de soporte puede corregir antes de consumir horas de máquina y material.

<div class="placeholder">
<strong>Espacio sugerido para collage:</strong> ejemplos de warping, stringing, layer shift, subextrusión y mala primera capa. Archivo sugerido: <code>assets/img/fallas/collage-fallas-impresion.png</code>.
</div>

## 1. Calidad de impresión

La calidad puede evaluarse desde varios puntos de vista:

- apariencia superficial;
- precisión dimensional;
- resistencia mecánica;
- adhesión entre capas;
- ajuste con otras piezas;
- estabilidad geométrica;
- facilidad de postprocesado;
- repetibilidad.

Una pieza puede verse bien y fallar mecánicamente. También puede verse poco estética y funcionar correctamente. Por eso la calidad debe evaluarse de acuerdo con el propósito de la pieza.

## 2. Mala adhesión a la cama

La pieza no se pega correctamente o se despega durante la impresión.

Causas posibles:

- cama sucia;
- temperatura baja;
- primera capa demasiado alta;
- superficie inadecuada;
- pieza con poca base;
- material con alta contracción;
- ventilación excesiva al inicio.

Soluciones posibles:

- limpiar cama;
- revisar nivelación o calibración;
- usar brim;
- aumentar temperatura de cama dentro de rango seguro;
- reducir velocidad de primera capa;
- revisar orientación de la pieza.

## 3. Warping

El warping ocurre cuando las esquinas o bordes de la pieza se levantan por contracción térmica.

Causas posibles:

- contracción del material;
- enfriamiento desigual;
- cama insuficientemente caliente;
- corrientes de aire;
- pieza larga o con esquinas agudas;
- falta de adhesión.

Soluciones posibles:

- usar brim;
- redondear esquinas;
- mejorar adhesión;
- controlar temperatura ambiente;
- usar gabinete en materiales técnicos;
- seleccionar material con menor contracción.

## 4. Stringing

El stringing aparece como hilos delgados entre partes de la pieza.

Causas posibles:

- temperatura demasiado alta;
- retracción insuficiente;
- filamento húmedo;
- velocidad de viaje baja;
- material propenso a hilar, como PETG.

Soluciones posibles:

- ajustar retracción;
- reducir temperatura;
- secar filamento;
- aumentar velocidad de viaje;
- revisar configuración específica de material.

## 5. Subextrusión

La subextrusión ocurre cuando sale menos material del esperado. Se observan huecos, líneas delgadas o capas incompletas.

Causas posibles:

- boquilla parcialmente tapada;
- temperatura baja;
- filamento atorado;
- engrane del extrusor sucio;
- flujo mal configurado;
- velocidad demasiado alta para el hotend.

Soluciones posibles:

- limpiar boquilla;
- revisar extrusor;
- aumentar temperatura dentro del rango;
- reducir velocidad;
- revisar diámetro de filamento;
- calibrar flujo.

## 6. Sobreextrusión

La sobreextrusión ocurre cuando se deposita demasiado material. La pieza puede verse abultada, con esquinas gruesas o superficies rugosas.

Causas posibles:

- flujo excesivo;
- temperatura alta;
- diámetro de filamento mal configurado;
- perfil de material incorrecto;
- calibración deficiente.

Soluciones posibles:

- reducir flujo;
- verificar perfil;
- revisar diámetro;
- ajustar temperatura;
- calibrar extrusión.

## 7. Layer shift

El desplazamiento de capas ocurre cuando una capa aparece corrida respecto a las anteriores.

Causas posibles:

- golpe o atasco;
- bandas flojas;
- aceleración excesiva;
- motor perdiendo pasos;
- obstrucción en movimiento;
- pieza despegada parcialmente.

Soluciones posibles:

- revisar tensiones;
- reducir velocidad/aceleración;
- verificar guías;
- confirmar que no haya cables interfiriendo;
- revisar adhesión.

## 8. Boquilla tapada

Una boquilla tapada impide el flujo correcto de material.

Causas posibles:

- filamento contaminado;
- polvo;
- temperatura incorrecta;
- material degradado;
- cambio de material mal realizado;
- boquilla demasiado pequeña para material compuesto.

Soluciones posibles:

- limpieza en frío;
- cambio de boquilla;
- filtrar o limpiar filamento;
- evitar materiales abrasivos sin boquilla adecuada;
- purgar correctamente al cambiar material.

## 9. Elephant foot

El elephant foot es un ensanchamiento en las primeras capas de la pieza.

Causas posibles:

- cama demasiado caliente;
- boquilla demasiado cerca;
- exceso de flujo en primera capa;
- peso de la pieza sobre capas inferiores aún blandas.

Soluciones posibles:

- ajustar distancia inicial;
- reducir temperatura de cama;
- compensar elephant foot en slicer;
- usar chaflán en la base del diseño.

## 10. Ghosting o ringing

El ghosting aparece como ondas repetidas cerca de esquinas o cambios bruscos de dirección.

Causas posibles:

- vibración;
- aceleración alta;
- estructura poco rígida;
- correas mal tensadas;
- velocidad excesiva.

Soluciones posibles:

- reducir aceleración;
- revisar estructura;
- ajustar tensión de correas;
- usar calibración de vibración si la impresora la soporta.

## 11. Mala superficie superior

La superficie superior puede verse abierta, rugosa o con huecos.

Causas posibles:

- pocas capas superiores;
- relleno insuficiente;
- flujo bajo;
- temperatura inadecuada;
- enfriamiento deficiente.

Soluciones posibles:

- aumentar capas superiores;
- aumentar infill;
- ajustar flujo;
- revisar temperatura;
- usar ironing si es apropiado.

## 12. Piezas frágiles

Una pieza puede romperse fácilmente por:

- mala adhesión entre capas;
- material inadecuado;
- orientación incorrecta;
- pocos perímetros;
- temperatura baja;
- humedad;
- diseño con concentraciones de esfuerzo.

Soluciones posibles:

- orientar según carga;
- aumentar perímetros;
- elegir material adecuado;
- aumentar temperatura moderadamente;
- agregar radios o refuerzos;
- secar filamento;
- evitar esquinas internas agudas.

## 13. Calidad dimensional

Las piezas impresas pueden no coincidir exactamente con el modelo. Las causas incluyen contracción, calibración, flujo, temperatura, orientación y comportamiento del material.

Aspectos críticos:

- agujeros tienden a salir más pequeños;
- ejes y pernos requieren holgura;
- piezas que encajan necesitan tolerancia;
- materiales distintos se contraen diferente;
- la orientación afecta precisión de detalles.

## 14. Tabla de diagnóstico rápido

| Síntoma | Causa probable | Acción inicial |
|---|---|---|
| La pieza se despega | Mala adhesión | Limpiar cama, revisar primera capa, usar brim |
| Hilos entre partes | Stringing | Ajustar retracción, bajar temperatura, secar filamento |
| Huecos en líneas | Subextrusión | Revisar boquilla, temperatura y flujo |
| Esquinas levantadas | Warping | Mejorar adhesión y controlar enfriamiento |
| Capas corridas | Layer shift | Revisar bandas, velocidad y obstrucciones |
| Base ensanchada | Elephant foot | Ajustar cama, primera capa y compensación |
| Superficie rugosa | Temperatura/flujo | Ajustar perfil y revisar humedad |
| Pieza quebradiza | Mala adhesión/material | Cambiar orientación, material o temperatura |

## 15. La falla como fuente de aprendizaje

En impresión 3D, diagnosticar es aprender a leer la pieza. Cada falla deja evidencia visual y física. Un usuario con experiencia no solo ve una pieza defectuosa; interpreta síntomas.

Esta capacidad es fundamental en un FabLab porque permite que la comunidad use mejor los equipos, desperdicie menos material y documente soluciones.

## Referencias

[1] Prusa Research, “Filament Material Guide.”  
[2] Prusa Research, “Layers and perimeters.”  
[3] UltiMaker, “Cura infill settings.”  
[4] Bambu Lab Wiki, “Printer Calibration Guide.”

## Fin del manual

[Volver al inicio](index.md)
