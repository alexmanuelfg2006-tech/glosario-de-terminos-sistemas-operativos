>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

***Sistema Básico de Entrada/Salida / Basic Input/Output System 

**Andrew S. Tanenbaum** y **Herbert Bos** (2015) La describen como un programa primitivo pero vital que toma el control de la CPU en el momento en que se presiona el botón de encendido (cuando el contador de programa del procesador apunta a una dirección de memoria fija en la ROM).La BIOS es la encargada de verificar todos los componentes del sistema antes de inicializarlo para comprobar que todo funciona correctamente



```
 [ Botón de Encendido / Reset Físico ]
                  │
                  ▼
 [ Firmware UEFI (Almacenado en Chip Flash SPI / Memoria No Volátil) ]
                  │
                  ├──► Ejecuta POST (Autodiagnóstico de RAM, CPU y GPU)
                  ├──► Configura SMM (System Management Mode - Ring -2)
                  │
                  ▼
 [ Lectura de Variables NVRAM (BootOrder, BootCurrent) ]
                  │
                  ▼
 [ Verificación Criptográfica de Integridad (Secure Boot) ]
                  │
        ┌─────────┴─────────┐
     (Válido)           (Inválido)
        │                   │
        ▼                   ▼
 [ Carga el Binario ]   [ Bloqueo de Arranque / ]
 [ .efi desde la    ]   [ Error de Firma Digital]
 [ Partición ESP    ]
        │
        ▼
 [ Transición a Servicios de Tiempo de Ejecución (UEFI Runtime Services) ]
                  │
                  ▼
 [ Carga del Kernel del Sistema Operativo en RAM y Salto a Ring 0 ]
```

### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. capitulo 1.