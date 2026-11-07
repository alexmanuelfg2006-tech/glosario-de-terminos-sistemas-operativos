>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Registro de Arranque Principal / Master Boot Record (MBR)

Según Tanenbaum y Bos (2015), el MBR es el primer sector de un disco duro tradicional (sector 0, de 512 bytes) que contiene el código ejecutable del gestor de arranque primario junto con la tabla de particiones clásica del sistema, limitando la estructura a un máximo de cuatro particiones primarias. Es la parte del disco donde se almacena el bootloader.



```
 ┌─────────────────────────────────────────────────────────┐
 │              Sector de Arranque MBR (512 Bytes)         │
 │  ┌───────────────────────────────────────────────────┐  │
 │  │ Código de Arranque Primario (Bootstrap) - 446 Bytes│  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Tabla de Particiones Clásicas (4 Entradas) - 64 B │  │
 │  ├───────────────────────────────────────────────────┤  │
 │  │ Firma de Arranque Mágico (0xAA55) - 2 Bytes       │  │
 │  └───────────────────────────────────────────────────┘  │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Particiones Principales / 1-4)         ▼ (Límite Técnico)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Sistemas Operativos /     │          │ Máximo 2 TB por disco y      │
 │     Volúmenes Lógicos        │          │   vulnerabilidad a corrupción │
 └──────────────────────────────┘          └──────────────────────────────┘
```

### Referencia
Tanenbaum, A. S., & Bos, H. (2015). _Modern Operating Systems_ (4.ª ed.). Pearson.Capítulo 5