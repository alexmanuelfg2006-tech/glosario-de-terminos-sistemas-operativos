>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Gestor de arranque systemd-boot / systemd-boot

Según Shotts (2019), systemd-boot es un gestor de arranque ligero y minimalista exclusivo para firmware UEFI que lee directamente las entradas del menú desde la partición del sistema EFI sin ejecutar scripts complejos en tiempo de arranque, simplificando el proceso de carga del núcleo en sistemas Linux modernos. Es un gestor de arranque para dispositivos que usen UEFI


```
 ┌─────────────────────────────────────────────────────────┐
 │               Firmware UEFI de la Placa Base            │
 └────────────────────────────┬────────────────────────────┘
                              │ (Ejecuta el binario EFI: /EFI/systemd/systemd-bootx64.efi)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                   systemd-boot (UEFI)                   │
 │   * Lee entradas de menú directamente desde carpetas    │
 │     montadas en /EFI/loader/entries/ (*.conf)           │
 └────────────────────────────┬────────────────────────────┘
                              │ (Carga directa de imágenes vmlinuz e initrd a RAM)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Núcleo del Sistema Operativo (Kernel)         │
 └─────────────────────────────────────────────────────────┘
```

### Referencia
Shotts, W. (2019). _The Linux Command Line: A Complete Introduction_ (2.ª ed.). No Starch Press.Capítulo 1