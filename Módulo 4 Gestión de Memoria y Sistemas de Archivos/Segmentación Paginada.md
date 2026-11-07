>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Segmentación Paginada / Paged Segmentation

Según Silberschatz et al. (2018), la segmentación paginada es una arquitectura combinada de gestión de memoria donde los segmentos lógicos de un proceso se subdividen internamente en páginas de tamaño fijo para eliminar la fragmentación externa y simplificar la asignación física. Es un modelo híbrido de administración de memoria que combina las ventajas de la segmentación y de la paginación para mitigar sus debilidades individuales.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Espacio de Direcciones Lógicas            │
 │       [ Segmento de Código ]  [ Segmento de Datos ]     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Cada segmento se divide en Páginas)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Tabla de Segmentos del Proceso                  │
 │  * Apunta a la Tabla de Páginas específica de cada segmento
 └────────────────────────────┬────────────────────────────┘
                              │ (Traducción por Tabla de Páginas)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │          Marcos de Página en Memoria Física (RAM)       │
 └─────────────────────────────────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9