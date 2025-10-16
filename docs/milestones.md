# Hitos del Proyecto

Este documento detalla los hitos clave para el desarrollo del proyecto
---
## [M0] Modelado del Dominio del Problema

*   **Objetivo:** Analizar las Historias de Usuario para crear un modelo del dominio. El propósito de este hito es traducir las necesidades del usuario en las estructuras y entidades de software fundamentales, siguiendo la metodología de Domain-Driven Design.
*   **Producto entregable** Código fuente inicial que establece las entidades clave del problema.
*   **HU Relacionadas:** [HU1] Pedro, [HU2] Paco
* **Será valido si:**
    *   [ ] El código entregado refleja los conceptos principales descritos en las HUs priorizadas.
    *   [ ] La estructura del código sigue las buenas prácticas del lenguaje y sirve como base para el siguiente hito.
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado esta documentación inicial como la base sólida para el proyecto.

---
## [M1] Datos Ambientales Diarios Disponibles en la Plataforma

*   **Objetivo:** Disponer de un sistema robusto que recopila y consolida automáticamente los datos ambientales diarios necesarios para el cálculo del DermaIndex.
*   **HU Relacionadas:** [HU1] Pedro, [HU2] Paco
*   **Será valido si:**
    *   [ ] Un sistema automático para la extracción diaria de datos ambientales de las fuentes designadas (ej. AEMET) está implementado y operativo.
    *   [ ] Los datos extraídos se fusionan, estandarizan y almacenan en la estructura de datos definida en M0 de forma consistente.
    *   [ ] La obtención de datos es fiable y se ejecuta según la frecuencia requerida (ej. diariamente).
    *   [ ] **Todas las pruebas automáticas para la extracción y fusión de datos han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado el flujo de datos y la coherencia de la estructura.
        
---
## [M2] Cálculo y Recomendaciones Diarias

*   **Objetivo:** Contar con un componente funcional capaz de calcular el DermaIndex **para un día concreto (tanto actual como futuro)** y generar recomendaciones cualitativas basadas en él, permitiendo a los usuarios obtener información actionable.
*   **HU Relacionadas:** [HU1] Pedro, [HU2] Paco
* Será valido si:
    *   [ ] La lógica completa para el cálculo del DermaIndex diario está implementada, siguiendo las especificaciones del algoritmo.
    *   [ ] El módulo de generación de recomendaciones cualitativas, basado en el DermaIndex, funciona correctamente y produce salidas coherentes.
    *   [ ] Los resultados del cálculo del DermaIndex y las recomendaciones generadas son consistentes y verificables con un conjunto de datos de prueba representativo.
    *   [ ] **Todas las pruebas unitarias y de integración para la lógica de cálculo han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado la funcionalidad y los resultados de este hito.

