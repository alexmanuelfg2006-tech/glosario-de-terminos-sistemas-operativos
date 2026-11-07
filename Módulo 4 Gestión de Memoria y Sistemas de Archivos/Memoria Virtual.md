>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Memoria Virtual / Virtual Memory

Según Silberschatz et al. (2018), la memoria virtual es una abstracción ofrecida por el sistema operativo que separa el espacio de memoria lógica percibido por el programador de la memoria física disponible, posibilitando la ejecución de programas cuya dimensión excede la capacidad de la memoria RAM. Permite que un proceso se ejecute de manera continua asignándole una dirección lógica amplia aunque sus datos no se encuentren de forma completa ni contigua en la RAM física, recurriendo al almacenamiento secundario

```
 ┌─────────────────────────────────────────────────────────┐
 │            Espacio de Direcciones Virtuales             │
 └────────────────────────────┬────────────────────────────┘
                              │ (Traducción y paginación gestionada por la MMU)
                              ▼
         ┌────────────────────┴────────────────────┐
         ▼ (Si la página está en RAM)              ▼ (Si la página está inactiva)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │     Memoria Física (RAM)     │          │    Almacenamiento Secundario │
 │                              │          │         (Swap / Disco)       │
 └──────────────────────────────┘          └──────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10