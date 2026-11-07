>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---


Según Silberschatz et al. (2018), el quántum de tiempo es el intervalo de tiempo discreto asignado a cada proceso en un algoritmo de planificación como _Round Robin_, transcurrido el cual la CPU interrumpe el proceso y pasa a ejecutar la siguiente tarea en cola. Es un pequeño intervalo de tiempo que se le asigna a cada proceso para que use el CPU


```
 [ Algoritmo Round Robin ] ──> [ Definición de Quántum ] ──> [ Temporizador (Timer IRQ) ]
                                                                       │
                                                                       ▼
 [ Experiencia Interactiva ] <── [ Preempción / Cambio de Contexto ] <──┘
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 5