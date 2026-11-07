>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 3| Volver al Módulo 3]]

---
Exclusión Mutua / Mutual Exclusion (Mutex)

Según Silberschatz et al. (2018), la exclusión mutua es el requisito fundamental de sincronización que establece que, si un proceso o hilo se encuentra ejecutando su sección crítica, ningún otro hilo puede estar ejecutándose dentro de esa misma sección crítica sobre los mismos datos. es la propiedad de la sincronizacion de procesos que no permite que mas de un proceso este en la seccion critica al mismo tiempo


```
 ┌─────────────────────────────────────────────────────────┐
 │               Hilos Intentando Acceder                  │
 │      [Hilo A]                  [Hilo B]                 │
 └───────────┬────────────────────────┬────────────────────┘
             │                        │
             ▼                        ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Mecanismo de Exclusión Mutua (Mutex)        │
 │  * Si está libre ➔ Concede el paso y bloquea el cerrojo │
 │  * Si está ocupado ➔ Pone al hilo en cola de espera     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Acceso exclusivo garantizado)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Ejecución Segura en la Sección Crítica            │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 6