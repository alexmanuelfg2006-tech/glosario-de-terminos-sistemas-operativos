>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Algoritmo SCAN (Algoritmo del Ascensor) / SCAN Algorithm (Elevator Algorithm)

Silberschatz et al. (2018) estructuran el movimiento de los cabezales del disco duro imitando fielmente el comportamiento de un ascensor en un edificio. El cabezal avanza de manera continua en un sentido resolviendo las peticiones encontradas a su paso hasta llegar al último sector o borde del disco. Una vez alcanzado el límite, invierte automáticamente su dirección de desplazamiento para atender las órdenes en sentido contrario. Gracias a este esquema dinámico, se optimiza significativamente el tiempo de búsqueda mecánico y se evita que ciertas peticiones queden postergadas indefinidamente.


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

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.