>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Punteros Directos / Direct Pointers

Tanenbaum y Bos (2015) detallan el rol de estos punteros que apuntan sin intermediarios a las ubicaciones físicas exactas donde yacen los datos del archivo en el medio no volátil. Las estructuras tradicionales de inodo reservan los primeros 12 punteros para almacenamiento directo de bloques. Ofrecen la máxima velocidad de lectura y escritura al eliminar los tiempos de latencia asociados a la lectura previa de bloques de indirección. Permiten acceder instantáneamente al contenido de archivos de tamaño pequeño o mediano.


```
 ┌─────────────────────────────────────────────────────────┐
 │                     Estructura del Inodo                │
 └────────────────────────────┬────────────────────────────┘
                              │ (Lectura de punteros directos)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Punteros Directos (Ej. Punteros 0 a 11)         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta directamente al bloque físico)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │      Bloques de Datos Reales en el Almacenamiento       │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
