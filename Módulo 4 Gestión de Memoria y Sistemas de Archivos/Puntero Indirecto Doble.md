>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Puntero Indirecto Doble / Puntero Indirección Nivel 2

Silberschatz et al. (2018) describen cómo este puntero accede a un bloque cargado de punteros indirectos simples dentro del inodo, incrementando sustancialmente el tamaño de archivo direccionable. El inodo guarda la dirección de un bloque de disco que contiene a su vez direcciones de otros bloques repletos de punteros a datos reales. Este segundo nivel de indirección permite a los sistemas de archivos tradicionales respaldar archivos de varios gigabytes de extensión. Forma parte de la jerarquía de bloques clásica en sistemas POSIX.


```
 ┌─────────────────────────────────────────────────────────┐
 │                     Estructura del Inodo                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta al Bloque Índice de Nivel 1)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │           Bloque Puntero Indirecto Doble                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a múltiples Bloques de Punteros Simples)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │           Bloques de Punteros Simples                   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a los bloques de datos reales)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Bloques de Datos del Archivo                │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
