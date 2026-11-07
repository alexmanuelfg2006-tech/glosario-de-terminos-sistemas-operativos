>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

***gestor de arranque / bootloader

**Andrew S. Tanenbaum** y **Herbert Bos** (2015) Explican que el Bootloader es el fragmento de código que reside en el primer sector de un disco duro o medio de almacenamiento (históricamente conocido como el _Master Boot Record_ o MBR). el Bootloader es un pequeño fragmento de código en el disco duro normalmente de menos de 512 bytes que es ejecutado por la BIOS para iniciar el sistema operativo




```
 [ Hardware / Encendido (Power-On) ]
                  │
                  ▼
 [ Firmware (BIOS Legacy o UEFI) ] ── Inicializa el sistema y busca el dispositivo primario
                  │
        ┌─────────┴─────────┐
    (Si es MBR)         (Si es UEFI)
        │                   │
        ▼                   ▼
 [ Sector MBR (512b) ]  [ Partición ESP (.efi) ]
        │                   │
        ▼                   ▼
 [ Bootloader Stage 1 / Core.img ] ── Lee el sistema de archivos del disco
                  │
                  ▼
 [ Gestor de Arranque Principal (Menú GRUB / Systemd-boot) ]
                  │
                  ▼
 [ Carga de Imagen del Kernel (vmlinuz) y Sistema de Archivos Temporal (initramfs) en RAM ]
                  │
                  ▼
 [ Salto de Control al Kernel en Ring 0 (Inicio del Sistema Operativo) ]
```

C

```
#include <stdio.h>

// Simulación de un sector de arranque MBR de 512 bytes en C
int main(void) {
    unsigned char mbr_sector[512] = {0};

    // --- Simulación de instrucciones de código máquina de bajo nivel (16-bit real mode) ---
    // En un bootloader real, aquí iría código en ensamblador x86 para limpiar registros,
    // configurar la pila (stack) y mostrar un mensaje en pantalla mediante la BIOS (INT 10h).
    
    char mensaje[] = "Cargando Gestor de Arranque (Bootloader Stage 1)...\r\n";
    int i = 0;
    while (mensaje[i] != '\0' && i < 500) {
        mbr_sector[i] = (unsigned char)mensaje[i];
        i++;
    }

    // --- FIRMA DE ARRANQUE OBLIGATORIA (Magic Number) ---
    // Los últimos dos bytes del sector de 512 bytes deben ser 0x55 y 0xAA (en little-endian: 0xAA55)
    mbr_sector[510] = 0x55;
    mbr_sector[511] = 0xAA;

    printf("[Simulador MBR] Sector de arranque de 512 bytes construido con éxito.\n");
    printf("Firma de arranque aplicada en offsets 510 y 511: 0x%02X 0x%02X\n", mbr_sector[510], mbr_sector[511]);

    return 0;
}
```

### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. capitulo 9.