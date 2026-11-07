>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---

***cambio de modo / Mode switch


**William Stallings** (2018) nos explica que un cambio de modo es una alteración temporal en los privilegios de ejecución de la CPU, pero que no implica necesariamente cambiar el proceso que se está ejecutando. El cambio de modo nos permite cambiar entre modo ususario y modo kernel para alguna llamada especifica y luego vuelve al modo ususario 

```
 [ Aplicación en Modo Usuario (Ring 3) ]
                   │
                   ├──► Ejecuta instrucción de interrupción / syscall (ej. INT 0x80 o SYSCALL)
                   ▼
 [ Cambio de Nivel de Privilegio en Hardware (CPU cambia CS.RPL a 0) ]
                   │
                   ▼
 [ Guardado de Contexto de Usuario (Registros, Pila, RIP/RSP) en la Pila del Kernel ]
                   │
                   ▼
 [ Ejecución del Manejador de Interrupciones / Syscall en Modo Kernel (Ring 0) ]
                   │
                   ▼
 [ Restauración de Contexto y Retorno mediante Instrucción Privilegiada (SYSRET / IRET) ]
                   │
                   ▼
 [ Retorno al Modo Usuario (Ring 3) ]
```

Bash
Permite ver cuántas veces el sistema operativo cambia de contexto entre procesos y modos por segundo:
```
vmstat 1 5

# La columna 'in' (interrupts) y 'cs' (context switches) muestran la frecuencia de transiciones de Ring 3 a Ring 0.
```
### Referencia
Stallings, W. (2018). _Operating systems: Internals and design principles_ (9.ª ed.). Pearson. capitulo 3

