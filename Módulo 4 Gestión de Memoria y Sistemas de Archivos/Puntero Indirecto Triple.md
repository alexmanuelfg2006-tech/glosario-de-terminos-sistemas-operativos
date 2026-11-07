>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Puntero Indirecto Triple / Puntero Indirección Nivel 3

Silberschatz et al. (2018) explican este tercer nivel de abstracción de punteros en un inodo para gestionar archivos de tamaño masivo que alcanzan la escala de los terabytes. El inodo almacena la dirección de un bloque maestro que apunta a bloques de indirección doble, los cuales referencian a bloques simples de direcciones físicas de datos. Aunque añade latencia adicional al requerir múltiples lecturas para acceder a un bloque, permite soportar archivos gigantescos en arquitecturas como ext3.


```
 ┌─────────────────────────────────────────────────────────┐
 │                     Estructura del Inodo                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta al Índice Raíz Triple)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Bloque Puntero Indirecto Triple                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a Dobles Índices)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │          Bloques de Indirección Intermedia              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a Bloques de Datos Finales)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Bloques de Datos del Archivo Masivo         │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.
