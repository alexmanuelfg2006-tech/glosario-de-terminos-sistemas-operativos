>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Bloque de Control de Proceso / Process Control Block (PCB)

Según Silberschatz et al. (2018), el PCB es la estructura de datos clave en el núcleo que almacena toda la información descriptiva y de control asociada a un proceso específico, tal como su estado, PID, registros de la CPU, información de planificación y contabilidad de memoria. Es la estructura como se almacenan los datos de los procesos


```
 ┌─────────────────────────────────────────────────────────┐
 │               Bloque de Control de Proceso (PCB)        │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Identificación: PID, PPID, UID, Estado del proceso│  │  
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Contexto de CPU: Registros generales, PC, SP, SW  │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Gestión de Memoria: Tablas de páginas, límites    │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Información de E/S: Descriptores de archivos, IPC │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Apunta a la siguiente PCB en colas del kernel)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Estructuras de Planificación (Colas)         │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 3