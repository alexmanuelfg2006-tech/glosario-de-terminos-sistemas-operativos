>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
***Contador de programa / Program Counter

Para **Andrew S. Tanenbaum** y **Herbert Bos** (2015) el PC es el elemento más crítico del **estado de ejecución** de un programa. Enfocan el PC en escenarios de interrupciones o cambios de contexto (_context switch_). Explican que cuando el sistema operativo decide pausar un proceso para darle tiempo de CPU a otro, debe guardar obligatoriamente el valor exacto del PC de ese proceso en su Bloque de Control de Procesos (PCB). el contador de programa guarda el valor del pc mientras se ejecuta otro proceso y cuando termina de ejecutarse carga el valor guardado.


```
 [ Inicio del Ciclo ]
          │
          ▼
 ┌────────────────────────────────────────────────────────┐
 │ 1. BÚSQUEDA (Fetch)                                    │
 │ • La CPU toma la dirección almacenada en el PC.        │
 │ • Lee la instrucción de la memoria RAM a través del bus.│
 └────────────────────────┬───────────────────────────────┘
                          │
                          ▼
 ┌────────────────────────────────────────────────────────┐
 │ 2. INCREMENTO DEL PC                                   │
 │ • El hardware suma automáticamente el tamaño de la     │
 │   instrucción al PC (ej. PC = PC + 4 bytes).           │
 └────────────────────────┬───────────────────────────────┘
                          │
                          ▼
 ┌────────────────────────────────────────────────────────┐
 │ 3. DECODIFICACIÓN (Decode)                             │
 │ • La Unidad de Control interpreta el código de operación.│
 └────────────────────────┬───────────────────────────────┘
                          │
                          ▼
 ┌────────────────────────────────────────────────────────┐
 │ 4. EJECUCIÓN (Execute)                                 │
 │ • Se ejecuta la operación (ALU, acceso a datos).       │
 │ • (Si hay un salto / *Jump*, el PC es sobrescrito con  │
 │   la nueva dirección de destino).                      │
 └────────────────────────┬───────────────────────────────┘
                          │
                          └──────► [ Siguiente Ciclo ]
```

### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. capitulo 1 y 2