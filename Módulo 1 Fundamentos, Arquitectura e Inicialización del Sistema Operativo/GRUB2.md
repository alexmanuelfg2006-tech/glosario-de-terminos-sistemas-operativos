>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Gestor de Arranque Unificado 2 / Grand Unified Bootloader 2

Según Shotts (2019), GRUB2 (_Grand Unified Bootloader 2_) es un gestor de arranque modular y flexible utilizado principalmente en distribuciones GNU/Linux para inspeccionar los sistemas de archivos, presentar un menú de selección al usuario y cargar el kernel con sus correspondientes parámetros en memoria. Es lo que toma el control tras la carga de la bios


```
 ┌─────────────────────────────────────────────────────────┐
 │                Arranque Inicial (core.img)              │
 └────────────────────────────┬────────────────────────────┘
                              │ (Carga módulos y entorno de comandos)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Menú Interactivo de GRUB2                 │
 │     (Lee archivo de configuración /boot/grub/grub.cfg)  │
 └────────────────────────────┬────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼ (Selección de Entrada)                  ▼ (Carga de Módulos FS)
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │    Carga de Imagen Linux     │          │ Soporte Ext4, Btrfs, NTFS,   │
 │   (kernel /initrd en RAM)    │          │         FAT32                │
 └──────────────────────────────┘          └──────────────────────────────┘
```


### Referencia
Shotts, W. (2019). _The Linux Command Line: A Complete Introduction_ (2.ª ed.). No Starch Press. Capítulo 1