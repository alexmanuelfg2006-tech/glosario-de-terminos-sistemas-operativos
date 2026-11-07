>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Spooling / Simultaneous peripheral operations on-line

Según Silberschatz et al. (2018), _Spooling_ (_Simultaneous Peripheral Operations On-Line_) es una técnica que intercepta los datos destinados a dispositivos lentos de entrada/salida (como impresoras) almacenándolos temporalmente en un búfer en disco para permitir que el proceso emisor continúe ejecutándose. es cuando se almacenan trabajos en el buffer para que un dispositivo lo use cuando este listo



```
 [ Solicitud Rápida ] ──> [ Almacenamiento en Disco (Spool) ] ──> [ Demonio de Fondo ] ──> [ Dispositivo Lento ]
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 13