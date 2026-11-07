>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Intercambio / Swap

egún Silberschatz et al. (2018), el _swapping_ es una técnica de gestión en la cual un proceso puede ser expulsado temporalmente de la memoria principal hacia un disco de almacenamiento secundario (_swap space_) y devuelto posteriormente para continuar su ejecución. Es un mecanismo de la memoria virtual mediante el cual el sistema operativo transfiere temporalmente un proceso completo (o parte de él) desde la memoria RAM principal hacia el espacio de intercambio en el disco duro secundario, y viceversa. 


```
 ┌─────────────────────────────────────────────────────────┐
 │              Memoria Física (RAM Saturada)              │
 └────────────────────────────┬────────────────────────────┘
                              │ (El kernel desaloja páginas inactivas)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Área de Swap (Disco / SSD)                   │
 │  * Almacenamiento secundario reservado para paginación  │
 │  * Alivia la presión de memoria en RAM                  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Carga de vuelta mediante fallo de página)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Recuperación hacia la Memoria Física            │
 └─────────────────────────────────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9
