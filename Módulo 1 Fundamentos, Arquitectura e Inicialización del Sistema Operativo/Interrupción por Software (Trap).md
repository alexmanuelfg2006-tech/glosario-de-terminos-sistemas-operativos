>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
interrupción por software / software interrupt

Según Silberschatz et al. (2018), una interrupción por software o _trap_ es un evento síncrono generado internamente por la CPU como respuesta a un error de ejecución (como una división por cero) o por la instrucción explícita de un programa que desea solicitar un servicio del núcleo. La interrupcion por software es cuando ocurre un error en el sistema y se queda congelado


Fragmento de código

```
sequenceDiagram
    autonumber
    actor Usuario as Proceso en Usuario (Ring 3)
    participant CPU as Unidad de Procesamiento (CPU)
    participant IDT as Vector de Excepciones / IDT
    participant Kernel as Manejador de Sistema / Kernel (Ring 0)

    Usuario->>CPU: Ejecuta instrucción de Trap / Syscall (ej. int 0x80, syscall, div /0)
    Note over Usuario, CPU: Interrupción estrictamente SÍNCRONA y controlada por el software
    CPU->>CPU: Cambia nivel de privilegio de Ring 3 a Ring 0
    CPU->>IDT: Busca el vector correspondiente a la llamada o excepción
    IDT->>Kernel: Transfiere el control al manejador del Kernel
    Kernel->>Kernel: Valida parámetros, ejecuta la acción (ej. E/S o excepción aritmética)
    Kernel-->>CPU: Prepara valores de retorno y ejecuta instrucción de salida
    CPU-->>Usuario: Restaura contexto y nivel Ring 3, continuando la ejecución
```



```
 [ Código de Aplicación (Espacio de Usuario / Ring 3) ]
                           │
                           ▼ (Instrucción de Syscall / Excepción síncrona)
             [ Generación de Interrupción por Software (Trap) ]
                           │
                           ▼
             [ Conmutación de Privilegios (Ring 3 ➔ Ring 0) ]
                           │
                           ▼
             [ Tabla de Descriptor de Interrupciones (IDT) ]
                           │
                           ▼
             [ Manejador Específico del Kernel (Syscall Dispatcher / Exception Handler) ]
                           │
        ┌──────────────────┴──────────────────┐
        ▼                                     ▼
 [ Ejecución del Servicio Solicitado ]   [ Manejo de Excepción / Fallo ]
        │                                     │
        └──────────────────┬──────────────────┘
                           ▼
             [ Retorno al Proceso de Usuario (Ring 3) ]
```
### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley.Capítulo 1

