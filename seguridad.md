---
layout: default
title: Seguridad
nav_exclude: true
---

# Seguridad en impresión 3D

La impresión 3D de escritorio suele percibirse como una tecnología limpia y segura porque se usa en escuelas, hogares, bibliotecas, laboratorios y FabLabs. En general, puede operarse de forma segura si se entiende el proceso y se aplican buenas prácticas. Sin embargo, no debe tratarse como un dispositivo sin riesgos.

Una impresora 3D combina calor, movimiento, electricidad, materiales poliméricos, emisiones, residuos y, en algunas tecnologías, sustancias químicas. En un FabLab, donde varias personas comparten equipos, la seguridad forma parte de la cultura de uso responsable.

<div class="placeholder">
<strong>Espacio sugerido para infografía:</strong> principales riesgos: calor, movimiento, emisiones, resina, electricidad, incendio, residuos. Archivo sugerido: <code>assets/img/seguridad/riesgos-impresion-3d.png</code>.
</div>

## 1. Riesgos térmicos

Las impresoras FDM trabajan con temperaturas elevadas. La boquilla puede superar fácilmente los 200 °C y la cama caliente puede alcanzar temperaturas suficientes para causar quemaduras.

Buenas prácticas:

- no tocar boquilla ni bloque calefactor;
- esperar a que la cama enfríe antes de retirar piezas difíciles;
- usar herramientas adecuadas para retirar material;
- evitar manipular el hotend durante calentamiento;
- no retirar plástico acumulado con los dedos.

## 2. Riesgos mecánicos

Los ejes se mueven mediante motores. Aunque las fuerzas de una impresora de escritorio no suelen ser comparables con maquinaria industrial, pueden causar pellizcos, golpes o atrapamientos menores.

Buenas prácticas:

- no meter las manos durante movimientos automáticos;
- no intentar detener el cabezal manualmente;
- no dejar cables sueltos cerca de ejes;
- mantener el área de movimiento libre;
- pausar la máquina antes de intervenir.

## 3. Riesgos eléctricos

La impresora combina fuentes de alimentación, resistencias calefactoras, motores, sensores y electrónica de control. Una máquina dañada, modificada o mal conectada puede representar riesgo eléctrico.

Buenas prácticas:

- usar cables en buen estado;
- no operar equipos con conexiones flojas;
- no modificar la fuente sin conocimiento técnico;
- usar contactos adecuados;
- evitar extensiones sobrecargadas;
- apagar la máquina ante olor extraño, humo o comportamiento anormal.

## 4. Emisiones en FDM

La impresión con filamentos puede generar partículas ultrafinas y compuestos orgánicos volátiles. NIOSH ha documentado preocupaciones sobre emisiones asociadas a impresoras 3D en espacios no industriales como makerspaces, escuelas, bibliotecas y pequeños negocios.

El nivel de emisión depende de:

- material;
- temperatura;
- número de impresoras;
- ventilación;
- tiempo de operación;
- tipo de impresora;
- presencia de gabinete o filtros.

Materiales como ABS y ASA tienden a requerir más atención por olor, temperatura y emisiones. PLA suele ser más amigable para espacios educativos, pero esto no significa que deba imprimirse sin ventilación.

## 5. Ventilación

Un FabLab debe considerar ventilación adecuada. No todas las impresoras necesitan la misma infraestructura, pero es recomendable evitar impresiones prolongadas en espacios cerrados sin renovación de aire.

Buenas prácticas:

- ubicar impresoras en zonas ventiladas;
- evitar saturar un cuarto con muchas impresoras activas;
- considerar extracción o filtración si se usan materiales técnicos;
- no imprimir ABS/ASA en espacios pequeños sin control;
- documentar qué materiales están permitidos.

## 6. Seguridad con resinas

Las impresoras de resina requieren mayor cuidado químico. La resina líquida puede irritar piel y ojos, y el proceso incluye lavado y curado.

Buenas prácticas:

- usar guantes adecuados;
- usar protección ocular;
- evitar contacto directo con resina líquida;
- trabajar en zona ventilada;
- no verter resina o solventes al drenaje;
- curar residuos antes de desecharlos, siguiendo lineamientos locales;
- almacenar resinas cerradas y etiquetadas;
- mantener alcohol isopropílico lejos de fuentes de ignición.

## 7. Seguridad con polvos

Tecnologías como SLS usan polvo polimérico. El manejo de polvo requiere control de inhalación, limpieza y equipo adecuado. Aunque SLS no sea común en un FabLab básico, conviene mencionar que no todos los procesos de impresión 3D tienen el mismo perfil de riesgo.

## 8. Supervisión de impresión

No todas las impresiones requieren observarse durante todo el proceso, pero la primera capa siempre debe revisarse. Muchos fallos graves inician como una mala adhesión, acumulación de material en la boquilla o desplazamiento de pieza.

Buenas prácticas:

- revisar primera capa;
- no iniciar impresiones largas sin verificar condiciones;
- evitar dejar piezas críticas sin seguimiento;
- usar cámara o monitoreo si está disponible;
- detener impresión ante ruido, humo, olor o acumulación anormal.

## 9. Orden y limpieza

Un área limpia reduce fallas y accidentes.

Buenas prácticas:

- retirar restos de filamento;
- guardar herramientas;
- etiquetar materiales;
- limpiar cama después de uso;
- desechar soportes y purgas;
- no dejar espátulas o pinzas sobre la cama;
- mantener cables organizados.

## 10. Uso compartido en FabLab

En un espacio compartido conviene establecer reglas claras:

- materiales permitidos;
- tiempos máximos;
- procedimiento de carga y descarga de filamento;
- limpieza posterior;
- reporte de fallas;
- restricciones para impresiones nocturnas;
- procedimiento ante emergencia;
- bitácora de mantenimiento.

La seguridad no debe presentarse como una barrera para usar la tecnología, sino como parte de su apropiación responsable.

## 11. Seguridad y cultura maker

La cultura maker invita a experimentar, modificar y aprender. Esa actitud es valiosa, pero debe acompañarse de criterio. Una máquina modificada sin documentación, un material desconocido o un perfil copiado sin entender puede generar riesgos o fallas.

En un FabLab, usar una impresora 3D implica cuidar la máquina, el espacio y a los demás usuarios.

## Referencias

[1] NIOSH, “A Guide for Makerspace Users, Schools, Libraries and Small Businesses.”  
[2] NIOSH, “Characterizing 3D Printing Emissions and Controls.”  
[3] Bambu Lab Wiki, “A1.”

## Siguiente sección

[Fallas, calidad y diagnóstico](fallas-calidad.md)
