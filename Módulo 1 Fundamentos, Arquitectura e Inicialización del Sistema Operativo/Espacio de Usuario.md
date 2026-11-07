>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
***espacio de usuario / user space

**Andrew S. Tanenbaum** y **Herbert Bos** (2015) Es la porción de memoria donde el software se ejecuta con el **nivel de privilegios más bajo del hardware** (Anillo 3 o _User Mode_) el espacio de usuario es el entorno asignado a todo software en el que "no se confía". En el espacio de usuario es donde se ejecuta todas las aplicaciones como navegadores y juegos y no se puede interactuar directamente con componentes directos de la computadora 

```
 [ Aplicación / Proceso en Ring 3 ]
                  │
                  ▼ (Ejecuta función de biblioteca ej. printf / write)
 [ Biblioteca Estándar / API (ej. glibc) ]
                  │
                  ▼ (Prepara registros e invoca instrucción de interrupción / syscall)
 [ Cambio de Contexto de Hardware (Ring 3 ──► Ring 0) ]
                  │
                  ▼
 [ Núcleo del Sistema Operativo procesa la solicitud en Espacio de Kernel ]
```

Bash

```
top -u $USER

# Lista en tiempo real los procesos que corren bajo el usuario actual en espacio de usuario y su consumo de CPU/RAM.
```
### Referencia
Tanenbaum, A. S., y Bos, H. (2015). _Modern operating systems_ (4.ª ed.). Pearson. capitulo 1