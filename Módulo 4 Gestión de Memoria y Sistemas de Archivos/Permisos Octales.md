>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 4| Volver al Módulo 4]]

---
Permisos Octales / Notación Octal de Permisos

Tanenbaum y Bos (2015) explican la asignación de permisos UNIX mediante valores numéricos en base 8 derivados de la suma ponderada de los bits de lectura (4), escritura (2) y ejecución (1). Un valor de 7 (4+2+1) otorga todos los permisos, mientras que 5 (4+1) concede lectura y ejecución. Los permisos finales se representan agrupando tres dígitos octales correspondientes al Propietario, Grupo y Otros (ejemplo: 755 para rwxr-xr-x). Permite establecer autorizaciones de seguridad de manera compacta en llamadas al sistema.


```
 ┌─────────────────────────────────────────────────────────┐
 │         Representación Numérica Octal (ej. 755)         │
 ├──────────────┬──────────────┬──────────────┬────────────┤
 │ Dígito Base  │ Propietario  │ Grupo        │ Otros      │
 │ (Bits Set)   │ (4+2+1 = 7)  │ (4+0+1 = 5)  │ (4+0+1 = 5)│
 └──────────────┴──────┬───────┴──────┬───────┴─────┬──────┘
                       │              │             │
                       ▼              ▼             ▼
 ┌─────────────────────────────────────────────────────────┐
 │     Traducción Directa a Máscaras de Bits del Sistema   │
 └─────────────────────────────────────────────────────────┘
```
---
**Referencia:**
> Tanenbaum, A. S., & Bos, H. (2015). Modern operating systems (4th ed.). Pearson.
