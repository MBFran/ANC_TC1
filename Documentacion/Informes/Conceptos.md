# Conceptos Clave
* Descripcion de conceptos basicos necesarios para el desarrollo del tema.
1. Anti-Aliasing filter:
   1. Idea/Concepto:
      * Un filtro Anti-Aliasing es un metodo que se utiliza principalmente en las entradas de los ADC para eliminar las frecuencias indeseadas (mayormente altas frecuencias) que se encuentran dentro de la banda que uno intenta analizar.
   3. Referencias:
      * https://la.mathworks.com/help/sps/ug/analog-anti-aliasing-filter.html
      * https://www.analog.com/en/resources/technical-articles/guide-to-antialiasing-filter-basics.html
2. Pre-Amplificador:
   1. Idea/Concepto:
      * El preamp sirve principalmente para elevar señales muy debiles provenientes de microfonos u otros inyectores de señar que hay que trabajar en niveles más altos.
   2. Circuitos:
      * La mayoria de circuitos que se encuentran de preamps utilizan como componente principal TBJ's. Aún así, se pueden utilizar amplificadores operacionales para reducir el consumo y una buena alternativa son los TL082/72 (principalmente por su alta impedancia y la implementación de JFET), o algunos OPA para mayor calidad.
   3. Referencias:
      * https://www.ti.com/lit/ug/tidu765/tidu765.pdf?ts=1780469447522
3. ADC:
   1. Que buscamos en un ADC para este proyecto?
      * Como uno de los principales problemas que tenemos en nuestro sistema es la velocidad de procesamiento y las señales que vamos a trabajar, no podemos conformarnos con los ADC que vienen integrados en los microcontroladores ya que suelen ser lentos y meten mucho ruido a la señal si luego se quiere exportar de nuevo como señal analogica. Es por eso que una de las mejores opciones que tenemos son los SAR ADC, ya que trabajan entre los Kilosamples per second (Ksps), y los 10Msps, además que se los puede encontrar con resoluciones desde los 8bits hasta los 20bits, lo que nos da un rango de seleccion bastante amplio para poder "jugar" con el presupuesto.
   2. Referencias:
      * https://www.analog.com/en/resources/technical-articles/selecting-the-right-adc-for-your-application.html
4. Reconstruction filter:
   1. Idea/Concepto:
      * Estos filtros son utilizados para reconstruir la señal una vez salen del DAC, ya que si uno mide a la salida se encuentra que la señal esta "semi-discretizada" debido a que el DAC trabaja a una cierta frecuencia de muestreo y esto termina afectando al resultado final. Para ello se utilizan filtros que buscan eliminar las frecuencias paracitas que surgen de la conversion, dichas frecuencias se "dividen" en regiones del dominio de la frecuencia, y se las denomina "Nyquist zones" o "Zonas de Nyquist" que equivalen a Fs/2, siendo Fs la "Frecuencia de muestreo".
      En funcion de qué regiones de Nyquist quieran conservar se pueden aplicar unos filtros u otros:
         1. Zero-Order Hold (ZOH) o Non-Return-to-Zero (NRZ): 1er Nyquist
         2. Return-to-Zero (RTZ): 1er y 2do Nyquist
         3. Return-to-Complement (RTC)/Mixed Mode: 2do y 3er Nyquist
   2. Referencias:
      * https://www.ti.com/content/dam/videos/external-videos/en-us/2/3816841626001/5577272810001.mp4/subassets/TIPL4705-DAC-Output-Response.pdf
# Conceptos Complementarios
* Conceptos que permiten una mejor comprension del tema pero no son estrictamente necesarios.
1. Adaptive lattice filter:
   1. Idea/Concepto:
      * A specialized, modular, and highly stable digital signal processing structure used to analyze, model, or filter signals through repeated "stages" (lattice sections).
   3. Referencias:
      * https://www.youtube.com/watch?v=KGTVT83MdKM
1. Zero-Order Hold (ZOH) o Non-Return-to-Zero (NRZ):
   * 
2. Return-to-Zero (RTZ):
   * 
3. Return-to-Complement (RTC)/Mixed Mode:
   * 
