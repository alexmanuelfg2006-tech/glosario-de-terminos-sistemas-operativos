>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Bit de Presencia / Present Bit

Según Silberschatz et al. (2018), el bit de presencia/validez es un indicador dentro de la PTE que especifica si la página asociada está actualmente residente en la memoria RAM o si su acceso desencadenará una trampa por fallo de página. Es una bandera binaria almacenada dentro de cada entrada de la tabla de páginas (PTE). Si su valor es 1, indica que la página virtual correspondiente se encuentra cargada en un marco de la memoria RAM.


```
 ┌─────────────────────────────────────────────────────────┐
 │               MMU Consulta la PTE                       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Verifica el Bit de Presencia)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Evaluación del Bit de Presencia                 │
 ├────────────────────────────┬────────────────────────────┤
 │ Si Bit Presencia == 1      │ Si Bit Presencia == 0      │
 │ ▼                          │ ▼                          │
 │ Página en RAM: Acceso OK   │ Página ausente: Dispara    │
 │                            │ Fallo de Página (Page Fault)│
 └────────────────────────────┴────────────────────────────┘
```
### Referencia 
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 10