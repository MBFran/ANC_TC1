# ANC_TC1
Este trabajo busca recrear y experimentar con los sistemas ANC (Active Noice Control/Cancelation), para fines academicos
de la materia Teoria de Circuitos 1 de la UTN FRBA a cargo de:
* Ing. Andrés Di Donato
* Ing. César Fuoco
* Ing. Christian Korec
# Sinopsis
* Un ANC es un sistema de control popularizado en el ambito del audio para aislar los sonidos del entorno. Estos sistemas constan de 3 partes principales que constituyen al final un unico camino hacia una salida analogica, y particularmente trabajan muy bien en baja frecuencia (en el rango audible).
* Estas etapas son:
  1. Region Acustica:
     * Esta parte es donde se encuentran los receptores (microfonos), y el parlante de salida. En esta etapa, si la describimos "modularmente", principalmente tenemos una entrada que capta el sonido del exterior, y otra que se usa como correccion dentro de los propios equipos a modo de realimentacion.  
  2. Region Analogica:
     * En esta etapa esta toda la electrónica analógica, mayoritariamente conformada por filtros, amplificadores, y conversores ADC y DAC que actuan de intermediarios entre la siguiente region y la region acustica
  3. Region Digital:
     * Aqui yacen los algoritmos y procesadores digitales para el trabajo más complejo del tratamiento de la señal para su cancelacion.
<img width="403" height="422" alt="Captura de pantalla 2026-05-21 151242" src="https://github.com/user-attachments/assets/747537d1-d43f-4010-8b44-c04babf28555" />
___
* Nuestro trabajo constará en poder llevar a la practica uno de estos sistemas, mezclando tanto electronica digital como analógica. Teniendo en cuenta las problematicas que se destacan en la mayoria de investigaciones como el retardo que puede haber entre la llegada del audio y la salida de la señal procesada, y la potencia de cancelacion que podamos alcanzar.

# Avances
### 20/05/26
* Simulacion del circuito encontrado mediante LTSPICE. Reemplazando los amplificadores operacionales por Op07, se llega a apreciar que a medida que el "ruido ambiente" aumenta en intensidad, empieza a generar distorciones en la salida (Hay que revisar que el circuito no tenga errores por las modificaciones).
