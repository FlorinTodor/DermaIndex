# DermaIndex
Proyecto de Infraestructura Virtual 2025-26 UGR.

## Problema a resolver

El problema se encuentra en que las personas (principalmente las que conozco que son de Andalucía) con psoriasis/dermatitis (yo incluido) notamos que los brotes empeoran en climas **secos/fríos** (p. ej., Granada) y mejoran en ambientes **más húmedos** (p. ej., Motril). Hoy no existe un **indicador con un horario sencillo** que integre en una sola señal los factores ambientales más relevantes (sequedad del aire, calor/sudor, radiación UV y contaminación) para decidir **a qué hora** conviene salir o hacer recados. Por lo que convendría tener un índice el cual refleje según los diferentes factores ambientales saber a qué franjas horarias convendría realizar las distintas actividades.

Por lo que el principal problema es obtener información de distintas fuentes que están poco estructuradas, para posteriormente fusionarlas e implementar dicho Indice que refleje las mejores franjas horarias para realizar las distintas actividades.

[Impacto del problema](https://onlinelibrary.wiley.com/doi/10.1111/all.16007)

## Información y Fuentes del Proyecto

Este proyecto no va a consumir APIs externas en tiempo real. Los datos se obtienen de distintas fuentes web y documentos textuales, dichas fuentes son:

### Fuentes de datos (3)

---

#### AEMET – Radiación Ultravioleta (UVI) – Observación diaria por horas (día anterior)

*   **URL base (tabla HTML):**
    [`https://www.aemet.es/es/eltiempo/observacion/radiacion/ultravioleta?datos=tabla`](https://www.aemet.es/es/eltiempo/observacion/radiacion/ultravioleta?datos=tabla)
*   **Qué se extrae:** Índice UV horario del día anterior para distintas ciudades de España (filtrado a ciudades andaluzas).

---

#### IFAPA – Índice de Temperatura y Humedad por estación

*   **URL patrón (HTML):**
    `https://www.juntadeandalucia.es/agriculturaypesca/ifapa/riaweb/web/estacion/{provincia}/{id_estación}`
    *   **Ejemplo Almería estación 1:** [`https://www.juntadeandalucia.es/agriculturaypesca/ifapa/riaweb/web/estacion/4/1`](https://www.juntadeandalucia.es/agriculturaypesca/ifapa/riaweb/web/estacion/4/1)
*   **Códigos provincia (Andalucía):**
    *   Almería: `4`
    *   Cádiz: `11`
    *   Córdoba: `14`
    *   Granada: `18`
    *   Huelva: `21`
    *   Jaén: `23`
    *   Málaga: `29`
    *   Sevilla: `41`
*   **Qué se extrae:** Temperatura y Humedad Relativa diaria.

---

#### Junta de Andalucía – SIVA – Índice de Calidad del Aire (PM2.5) – Datos cuantitativos diarios (CSV)

*   **URL índice cuantitativo (CSV, por día):**
    `https://www.juntadeandalucia.es/medioambiente/atmosfera/informes_siva/cuantitativo/YYYY/PP_YYYYMMDD.csv`
    *   **PP (provincia):** `AL`, `CA`, `CO`, `GR`, `HU`, `JA`, `MA`, `SE`
    *   **YYYY:** año
    *   **MM:** mes
    *   **DD:** día
    *   **Ejemplo (Granada, 2025-09-24):** [`https://www.juntadeandalucia.es/medioambiente/atmosfera/informes_siva/cuantitativo/2025/GR_20250924.csv`](https://www.juntadeandalucia.es/medioambiente/atmosfera/informes_siva/cuantitativo/2025/GR_20250924.csv)
*   **Qué se extrae:** Métrica cuantitativa diaria de calidad del aire con foco en PM2.5 por estación/zona.

#### AEMET - Predicciones tanto semanales como por horas para cada Provincia de Andalucía:

---

**Predicción semanal (7 días) - Formato XML:**

*   **Granada:** [`https://www.aemet.es/xml/municipios/localidad_18087.xml`](https://www.aemet.es/xml/municipios/localidad_18087.xml)
*   **Almería:** [`https://www.aemet.es/xml/municipios/localidad_04013.xml`](https://www.aemet.es/xml/municipios/localidad_04013.xml)
*   **Cádiz:** [`https://www.aemet.es/xml/municipios/localidad_11012.xml`](https://www.aemet.es/xml/municipios/localidad_11012.xml)
*   **Córdoba:** [`https://www.aemet.es/xml/municipios/localidad_14021.xml`](https://www.aemet.es/xml/municipios/localidad_14021.xml)
*   **Huelva:** [`https://www.aemet.es/xml/municipios/localidad_21041.xml`](https://www.aemet.es/xml/municipios/localidad_21041.xml)
*   **Jaén:** [`https://www.aemet.es/xml/municipios/localidad_23050.xml`](https://www.aemet.es/xml/municipios/localidad_23050.xml)
*   **Málaga:** [`https://www.aemet.es/xml/municipios/localidad_29067.xml`](https://www.aemet.es/xml/municipios/localidad_29067.xml)
*   **Sevilla:** [`https://www.aemet.es/xml/municipios/localidad_41091.xml`](https://www.aemet.es/xml/municipios/localidad_41091.xml)

---

**Predicción horaria por ciudades andaluzas - Formato XML:**

*   **Granada:** [`https://www.aemet.es/xml/municipios_h/localidad_h_18087.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_18087.xml)
*   **Almería:** [`https://www.aemet.es/xml/municipios_h/localidad_h_04013.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_04013.xml)
*   **Cádiz:** [`https://www.aemet.es/xml/municipios_h/localidad_h_11012.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_11012.xml)
*   **Córdoba:** [`https://www.aemet.es/xml/municipios_h/localidad_h_14021.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_14021.xml)
*   **Huelva:** [`https://www.aemet.es/xml/municipios_h/localidad_h_21041.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_21041.xml)
*   **Jaén:** [`https://www.aemet.es/xml/municipios_h/localidad_h_23050.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_23050.xml)
*   **Málaga:** [`https://www.aemet.es/xml/municipios_h/localidad_h_29067.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_29067.xml)
*   **Sevilla:** [`https://www.aemet.es/xml/municipios_h/localidad_h_41091.xml`](https://www.aemet.es/xml/municipios_h/localidad_h_41091.xml)

## Historias de usuarios
[HUs](docs/user-stories.md)

## Milestones
[Milestones](docs/milestones.md)

## Usuarios
[Users](docs/users.mds)

## Glosario
[Glosario](docs/glossary.md)

## [Configuración inicial (git and ssh)](evidencias/configuracion_inicial.md)
