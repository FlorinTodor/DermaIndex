# Hitos del Proyecto

Este documento detalla los hitos clave para el desarrollo del proyecto
---
## [M0] Base Arquitectónica y Modelos de Datos Iniciales

*   **Objetivo:** Establecer la estructura técnica fundamental del proyecto y los modelos de datos esenciales para la gestión inicial de la información ambiental. Este hito sienta las bases para futuras funcionalidades.
*   **HU Relacionadas:** Indirectamente soporta todas las HU, proporcionando la infraestructura.
*   **Será valido si:**

    *   [ ] La arquitectura modular del proyecto ha sido definida y documentada, incluyendo decisiones clave de diseño.
    *   [ ] El entorno de desarrollo para el equipo está configurado, versionado y es completamente funcional
    *   [ ] Los modelos de datos iniciales para la información ambiental están definidos, aprobados y documentados.
    *   [ ] Los esquemas de base de datos o estructuras de almacenamiento persistente están creados.
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado la propuesta de arquitectura y los modelos de datos iniciales como la base sólida para el proyecto.


---
## [M1] Sistema de Recopilación y Consolidación de Datos Ambientales

*   **Objetivo:** Disponer de un sistema robusto que recopila y consolida automáticamente los datos ambientales diarios necesarios para el cálculo del DermaIndex.
*   **HU Relacionadas:** [HU1] Pedro, [HU2] Paco, [HU3] Sara, [HU4] María 
*   **Será valido si:**
    *   [ ] Un sistema automático para la extracción diaria de datos ambientales de las fuentes designadas (ej. AEMET) está implementado y operativo.
    *   [ ] Los datos extraídos se fusionan, estandarizan y almacenan en la estructura de datos definida en M0 de forma consistente.
    *   [ ] Se han implementado mecanismos de validación y limpieza básica para asegurar la calidad de los datos ingresados.
    *   [ ] La obtención de datos es fiable y se ejecuta según la frecuencia requerida (ej. diariamente).
    *   [ ] **Todas las pruebas automáticas para la extracción y fusión de datos han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado el flujo de datos y la coherencia de la estructura.
        
---
## [M2] Cálculo y Recomendaciones Diarias

*   **Objetivo:** Contar con un componente funcional capaz de calcular el DermaIndex diario y generar recomendaciones cualitativas basadas en él, permitiendo a los usuarios obtener información actionable.
*   **HU Relacionadas:** [HU1] Pedro, [HU2] Paco, [HU3] Sara
* Será valido si:
    *   [ ] La lógica completa para el cálculo del DermaIndex diario está implementada, siguiendo las especificaciones del algoritmo.
    *   [ ] El módulo de generación de recomendaciones cualitativas, basado en el DermaIndex, funciona correctamente y produce salidas coherentes.
    *   [ ] Los resultados del cálculo del DermaIndex y las recomendaciones generadas son consistentes y verificables con un conjunto de datos de prueba representativo.
    *   [ ] **Todas las pruebas unitarias y de integración para la lógica de cálculo han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado la funcionalidad y los resultados de este hito.

