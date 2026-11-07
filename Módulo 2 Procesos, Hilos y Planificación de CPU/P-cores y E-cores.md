>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 2| Volver al Módulo 2]]

---
Núcleos de rendimiento y de eficiencia / Performance and Efficiency Cores

Según Tanenbaum y Bos (2015), las arquitecturas compuestas por núcleos de rendimiento y de eficiencia representan una evolución hacia el procesamiento heterogéneo, exigiendo al sistema operativo una planificación consciente del contexto energético para asignar las cargas en función de la demanda del proceso. Es una arquitectura de procesamiento heterogénea implementada en procesadores modernos. Combina núcleos de alto rendimiento (P-cores) , y núcleos de alta eficiencia (E-cores).

```
 ┌─────────────────────────────────────────────────────────┐
 │              Planificador del Sistema Operativo         │
 └────────────────────────────┬────────────────────────────┘
                              │ (Clasificación de hilos según demanda de carga)
                              ▼
         ┌────────────────────┴────────────────────┐
         ▼ (Cargas pesadas / Juegos / Compilación) │ (Tareas de fondo / Daemons / Sistema)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    P-cores (Performance)     │          │     E-cores (Efficiency)     │
 │  * Alta velocidad y consumo  │          │  * Optimizado para energía   │
 └──────────────────────────────┘          └──────────────────────────────┘
```
### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson. Capítulo 2