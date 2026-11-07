>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Puntero Indirecto Simple / Puntero Indirección Nivel 1

Tanenbaum y Bos (2015) identifican esta abstracción con un bloque de disco dedicado exclusivamente a contener las direcciones físicas de los bloques de datos del archivo en la unidad. Se utiliza cuando el número de bloques de datos directos soportados en la estructura principal del inodo ha sido superado por el tamaño del archivo. El inodo almacena la dirección de este bloque de indirección, el cual referencia a decenas o cientos de bloques de contenido. Expande la capacidad de almacenamiento inicial del inodo sin alterar su tamaño fijo.


```
 ┌─────────────────────────────────────────────────────────┐
 │                     Estructura del Inodo                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta al bloque de indirección)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │            Bloque Puntero Indirecto Simple              │
 │  * Contiene una tabla con múltiples referencias físicas │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a múltiples bloques de datos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Bloques de Datos Extendido del Archivo            │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
