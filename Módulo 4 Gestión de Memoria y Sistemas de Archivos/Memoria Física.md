>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Memoria Física / Physical Memory

Según Silberschatz et al. (2018), la memoria física constituye el hardware real de almacenamiento principal de la computadora, compuesto por un arreglo masivo de celdas de almacenamiento de bytes referenciadas directamente mediante direcciones físicas en el bus. Hace referencia al espacio de almacenamiento primario real constituido por los módulos de hardware de memoria RAM instalados físicamente en la computadora.

```
 ┌─────────────────────────────────────────────────────────┐
 │               Unidad Central de Procesamiento (CPU)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Bus de direcciones físicas)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Bancos de Memoria Física (RAM Hardware)         │
 │  * Celdas de almacenamiento basadas en condensadores    │
 │  * Direccionamiento absoluto directo                    │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Ejecución de Instrucciones y Datos Reales         │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 9