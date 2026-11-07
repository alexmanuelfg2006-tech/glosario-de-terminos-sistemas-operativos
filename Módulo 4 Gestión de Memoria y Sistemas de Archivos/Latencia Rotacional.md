>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Latencia Rotacional / Retardo por Rotación de Disco

Tanenbaum y Bos (2015) definen este parámetro como el tiempo requerido por los platos de un disco magnético para posicionar el sector de memoria deseado bajo la cabeza lectora. Es inversamente proporcional a la velocidad de rotación del disco medida en revoluciones por minuto (RPM). En discos estándar de 7200 RPM, la latencia rotacional promedio oscila alrededor de los 4.16 milisegundos por cada operación de acceso. Este retardo físico impulsa el uso de algoritmos de reordenamiento de peticiones y la migración hacia unidades de estado sólido.


```
 ┌─────────────────────────────────────────────────────────┐
 │     Cabezal Posicionado en la Pista Correcta            │
 └────────────────────────────┬────────────────────────────┘
                              │ (El plato continúa girando a velocidad constante)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Latencia Rotacional (Espera por Giro)           │
 │  * Tiempo hasta que el sector deseado rota y pasa bajo   │
 │    el cabezal estático                                  │
 └────────────────────────────┬────────────────────────────┘
                              │ (Alineación angular completada)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Sector Físico Bajo el Cabezal (Lectura Lista)     │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
