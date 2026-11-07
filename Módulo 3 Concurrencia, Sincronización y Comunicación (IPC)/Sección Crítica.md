>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Sección Crítica / Critical Section

Según Silberschatz et al. (2018), la sección crítica es el segmento de código dentro de un programa donde se accede o modifica un recurso compartido (como variables o archivos), requiriendo un protocolo de acceso para evitar inconsistencias de datos. es una porcion de codigo dentro de un proceso  que no debe ser ejecutada por mas de un proceso al mismo tiempo 


```
 ┌─────────────────────────────────────────────────────────┐
 │               Código de la Aplicación                   │
 ├─────────────────────────────────────────────────────────┤
 │  [ Código de Entrada ] (Protocolo de adquisición)       │
 ├─────────────────────────────────────────────────────────┤
 │         SECCIÓN CRÍTICA (Acceso a Recurso Compartido)   │
 │   * Modificación de variables globales o archivos       │
 ├─────────────────────────────────────────────────────────┤
 │  [ Código de Salida ] (Liberación del recurso)          │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 6