>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Hilo / Thread

Según Silberschatz et al. (2018), un hilo es la unidad básica de utilización de la CPU, compuesta por un identificador de hilo, un contador de programa, un conjunto de registros y una pila, la cual comparte el espacio de direcciones y los recursos con otros hilos pertenecientes al mismo proceso. Un hilo es la unidad más pequeña de trabajo que un sistema operativo puede planificar y ejecutar de forma independiente dentro de un programa.

```
 [ Proceso Contenedor ] ──> [ Compartición de Recursos (Memoria) ] ──> [ Hilos de Ejecución Independientes ]
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 4