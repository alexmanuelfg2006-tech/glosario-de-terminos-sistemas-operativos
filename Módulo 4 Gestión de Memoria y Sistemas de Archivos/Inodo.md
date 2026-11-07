>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Inodo / Nodo de Índice

Silberschatz et al. (2018) conceptualizan esta estructura interna de datos como el elemento del sistema de archivos que almacena los metadatos y ubicaciones físicas de los bloques de un archivo. No guarda el nombre del archivo ni sus datos directos, sino su tamaño, permisos de acceso, identificador de usuario, marcas de tiempo y punteros a disco. Cada archivo o directorio posee exactamente un número de inodo único dentro de la partición donde se encuentra alojado. Los sistemas de archivos POSIX basan toda su lógica de asignación e inspección en este nodo maestro.


```
 ┌─────────────────────────────────────────────────────────┐
 │               Directorio del Sistema                    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asocia Nombre de Archivo ➔ Número de Inodo)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                    Estructura del Inodo                 │
 │  * Metadatos: Permisos, Propietario, Tamaños, Fechas    │
 │  * Punteros Directos e Indirectos a Bloques en Disco    │
 └────────────────────────────┬────────────────────────────┘
                              │ (Localización de bloques físicos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Bloques de Datos Reales en el Disco           │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
