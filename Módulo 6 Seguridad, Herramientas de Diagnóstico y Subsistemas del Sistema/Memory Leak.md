>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 6| Volver al Módulo 6]]

---
Memory Leak / Fuga de Memoria

Tanenbaum y Bos (2015) definen esta falla de software que ocurre cuando un programa asigna memoria en el heap y omite liberarla tras concluir su procesamiento. Con el paso del tiempo, la acumulación incesante de bloques de RAM no liberados degrada progresivamente la memoria disponible en el sistema. Esto termina forzando al kernel a utilizar memoria de intercambio en disco (swap) y finalmente desencadena la intervención del OOM Killer. Su detección precisa exige el uso de herramientas de análisis dinámico como Valgrind.


```
 ┌─────────────────────────────────────────────────────────┐
 │      Proceso Solicita Memoria Dinámica (malloc/new)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Asignación otorgada en el Heap)
                              ▼
 ┌─────────────────────────────────────────────────────────┤
 │         Memoria Dinámicamente Asignada en Uso           │
 │  * El puntero original se pierde o sobreescribe         │
 │  * Ausencia de liberación explícita (free/delete)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Fuga persistente: Memoria retenida sin control)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │        Degradación Gradual y Agotamiento de la RAM      │
 └─────────────────────────────────────────────────────────┘
```

---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
