# DermaIndex
Proyecto de Infraestructura Virtual 2025-26 UGR.

## Problema a resolver


El problema se encuentra en que las personas con psoriasis/dermatitis (yo incluido) notamos que los brotes empeoran en climas **secos/fríos** (p. ej., Granada) y mejoran en ambientes **más húmedos** (p. ej., Motril). Hoy no existe un **indicador de horario sencillo** que integre en una sola señal los factores ambientales más relevantes (sequedad del aire, calor/sudor, radiación UV y contaminación) para decidir **a qué hora** conviene salir o hacer recados. Por lo que convendría tener un índice el cual refleje según los diferentes factores ambientales saber a qué franjas horarias convendría realizar las distintas actividades.

Por lo que el principal problema es obtener información de distintas fuentes que están poco estructuradas, para posteriormente fusionarlas e implementar dicho Indice que refleje las mejores franjas horarias para realizar las distintas actividades.

## Información y Fuentes del Proyecto

Este proyecto no va a consumir APIs externas en tiempo real. Los datos se obtienen de distintas fuentes web y documentos textuales, dichas fuentes son:

- [IFAPA (Estación 101 Purchil,Granada)](https://www.juntadeandalucia.es/agriculturaypesca/ifapa/riaweb/web/estacion/18/101)
    - Obtenemos las variables de Temperatura y humedad relativa
- [AEMET](https://www.aemet.es/es/eltiempo/prediccion/radiacionuv?w=0&zona=penyb&datos=det) 
    - Obtenemos el UVI máximo diario
- [Junta de Andalucia - REDIAM (calidad del aire)](https://www.juntadeandalucia.es/medioambiente/cas/autorizarAplicacionAnonima?codigo=PTHICA)
    - Obtenemos PM2.5
    
Estas tres fuentes nos permiten la reutilización de sus datos siempre y cuando se les cite.


## [Configuración inicial (git and ssh)](evidencias/configuracion_inicial.md)

