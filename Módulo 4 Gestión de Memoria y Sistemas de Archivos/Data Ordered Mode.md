>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Data Ordered Mode / Modo de Ordenamiento de Datos

Silberschatz et al. (2018) definen este modo de journaling en ext4 como la modalidad que garantiza la escritura previa de los datos del archivo en el medio físico antes de registrar el commit de los metadatos. Al forzar esta secuencia estricta de ordenamiento, impide que el sistema de archivos registre referencias en el diario hacia bloques que contienen basura o datos antiguos tras un apagado repentino. Equilibra de forma idónea el rendimiento del almacenamiento masivo con la integridad de los datos de usuario frente a modos de journaling más lentos.


```
 ┌─────────────────────────────────────────────────────────┐
 │             Solicitud de Escritura de Archivo           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Paso 1: Escribe primero los bloques de datos)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │       Escritura de Datos Reales en el Disco Principal   │
 └────────────────────────────┬────────────────────────────┘
                              │ (Paso 2: Una vez escritos, realiza el Commit de Metadatos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Commit de Metadatos en el Diario (Journal)       │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
