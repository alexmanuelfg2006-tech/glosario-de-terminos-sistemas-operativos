>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
**interfaz de _firmware_ extensible unificada / Unified Extensible Firmware Interface

Según Silberschatz et al. (2018), UEFI (_Unified Extensible Firmware Interface_) es la especificación moderna de interfaz de firmware diseñada para reemplazar la BIOS tradicional, soportando tablas de particiones de disco GPT, interfaces independientes y capacidad de inicialización previa más avanzada. Fue lo que remplazo a la bios y lo usan los nuevos dispositivos modernos 



```
 [ Firmware Moderno ] ──> [ Modo Protegido 64-bit ] ──> [ Particionamiento GPT ] ──> [ Secure Boot ]
```


```
 ┌─────────────────────────────────────────────────────────┐
 │              Encendido del Equipo (UEFI Boot)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Inicialización de hardware avanzada en 64-bit)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │         Validación de Firma (Secure Boot / NVRAM)       │
 └────────────────────────────┬────────────────────────────┘
                              │ (Lectura de Partición del Sistema EFI - ESP)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Carga de Archivos Binarios del Sistema (.efi)     │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecución del gestor firmado, ej. grubx64.efi)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │       Transferencia al Núcleo del Sistema Operativo     │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 1