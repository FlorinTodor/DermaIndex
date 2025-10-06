# Hitos del Proyecto

Este documento detalla los hitos clave para el desarrollo del proyecto
---
## [M0] Diseño de Módulos de Datos y Estructura del Proyecto

*   **Objetivo:** Diseñar y establecer la estructura del proyecto y los modelos de datos para la adquisición y gestión inicial de la información ambiental.
* Será valido si:

    *   [ ] La arquitectura modular del proyecto ha sido definida y documentada
    *   [ ] El entorno de desarrollo está configurado y es funcional para el equipo.
    *   [ ] Los modelos de datos iniciales para la información ambiental han sido definidos y aprobados.
    *   [ ] Los esquemas de base de datos o estructuras de almacenamiento están creados.
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado la propuesta de arquitectura y los modelos de datos iniciales.


---
## [M1] Recopilación y Fusión de Datos Diarios

*   **Objetivo:** Implementar la extracción de datos ambientales diarios de AEMET y su fusión en una estructura de datos coherente para el cálculo del DermalIndex.
* Será valido si:
    *   [ ] Se ha implementado un sistema para la extracción automática de datos ambientales diarios de las distintas fuentes.
    *   [ ] Los datos extraídos se fusionan y almacenan en la estructura de datos definida en M0.
    *   [ ] Se han establecido mecanismos de validación y limpieza básica para los datos.
    *   [ ] La obtención de datos es fiable y se ejecuta según la frecuencia requerida (ej. diariamente).
    *   [ ] **Todas las pruebas automáticas para la extracción y fusión de datos han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado el flujo de datos y la coherencia de la estructura.
        
---
## [M2] Cálculo y Recomendaciones Diarias

*   **Objetivo:** Desarrollar la lógica para calcular el DermalIndex diario y generar recomendaciones cualitativas para un día específico.
* Será valido si:
    *   [ ] Toda la lógica para el cálculo del DermalIndex diario está implementada.
    *   [ ] La generación de recomendaciones cualitativas funciona correctamente.
    *   [ ] Los resultados del cálculo y las recomendaciones son consistentes con las especificaciones y datos de prueba.
    *   [ ] **Todas las pruebas unitarias y de integración para la lógica de cálculo han pasado exitosamente.**
    *   [ ] Aprobación del Product Manager (JJ): El Product Manager ha revisado y aprobado la funcionalidad y los resultados de este hito.

