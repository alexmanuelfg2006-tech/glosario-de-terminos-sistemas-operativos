>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Round Robin / Round Robin Scheduling

Según Silberschatz et al. (2018), el algoritmo _Round Robin_ (RR) es una técnica expropiativa diseñada para sistemas de tiempo compartido que asigna pequeñas porciones fijas de tiempo de CPU (quántums) a cada proceso en una cola circular, garantizando la atención uniforme de todos los programas. Es un algoritmo de planificación expropiativo diseñado especialmente para sistemas de tiempo compartido e interactivos. Asigna a cada proceso de la cola de listos una unidad fija de tiempo de procesador denominada quántum


```
 ┌─────────────────────────────────────────────────────────┐
 │               Cola Circular de Listos                   │
 │     [ P1 ] ──► [ P2 ] ──► [ P3 ] ──► (Regresa al final) │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación por Quántum de Tiempo / Timer Interrupt)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │                 Núcleo de la CPU                        │
 │  * Ejecución limitada estrictamente al Quántum (q)      │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Si agota el quántum)                   ▼ (Si finaliza antes)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │ Interrupción de reloj: Vuelve│          │  Libera la CPU y sale del    │
 │   al final de la cola        │          │       sistema                │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 5