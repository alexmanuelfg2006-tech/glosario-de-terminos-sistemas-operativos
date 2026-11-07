>  **Navegación:** [[00 - Índice General (A-Z)| Índice A-Z]] | [[00 - Índice Módulo 1| Volver al Módulo 1]]

---
Puntero de pila / Stack Pointer

Según Silberschatz et al. (2018), el puntero de pila (_Stack Pointer_) es un registro interno que apunta a la dirección de memoria superior de la pila (_stack_) asociada al hilo activo, utilizada para guardar variables locales, parámetros y direcciones de retorno de funciones. El puntero de pila apunta la la ultima dirección de la memoria ram donde se guardo un registro


```
 [ Llamada a Función ] ──> [ Modificación de SP ] ──> [ Almacenamiento de Contexto/Variables ] ──> [ Retorno ]
```

# ANEXOS PARA EL TÉRMINO 6: Registro de Estado (Flags)

## Anexo A (Diagramas y Flujogramas) - Registro de Estado (Flags)

Fragmento de código

```
sequenceDiagram
    autonumber
    participant ALU as ALU (Unidad Aritmética)
    participant Flags as Registro FLAGS (RFLAGS)
    participant CPU as Lógica de Control de Salto

    ALU->>Flags: Resultado cero ➔ Activa Zero Flag (ZF = 1)
    ALU->>Flags: Resultado negativo ➔ Activa Sign Flag (SF = 1)
    ALU->>Flags: Desbordamiento ➔ Activa Overflow Flag (OF = 1)
    Flags->>CPU: Condiciona instrucciones de salto (JZ, JNE, JG)
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Flags

- **Trazas de Terminal (GNU/Linux - GDB):**
    
    Bash
    
    ```
    gdb -q ./mi_programa
    (gdb) info registers eflags
    ```
    
- **Código en C (Modificación y prueba de Flags mediante comparación):**
    
    C
    
    ```
    #include <stdio.h>
    
    int main() {
        int a = 5;
        int b = 5;
        if (a == b) { // Esta operación modifica el Zero Flag (ZF = 1) en el procesador
            printf("Los números son iguales (Zero Flag activado).\n");
        }
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Flags

Plaintext

```
 [ Operación ALU ] ──> [ Actualización de Flags (ZF, SF, CF) ] ──> [ Evaluación Condicional de Salto ]
```

# ANEXOS PARA EL TÉRMINO 7: Timer Interrupt

## Anexo A (Diagramas y Flujogramas) - Timer Interrupt

Fragmento de código

```
sequenceDiagram
    autonumber
    participant Clock as Reloj de Hardware (PIT / APIC Timer)
    participant CPU as Procesador (Ejecutando Proceso A)
    participant ISR as Manejador de Timer (Kernel)
    participant Sched as Planificador (Scheduler)

    Clock->>CPU: Envía pulso IRQ de Temporizador (Quantum agotado)
    CPU->>ISR: Salta a la rutina de interrupción del timer
    ISR->>Sched: Invoca al planificador de procesos
    Sched->>Sched: Selecciona Proceso B y realiza cambio de contexto
    Sched-->>CPU: Retorna al nuevo proceso
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Timer Interrupt

- **Trazas de Terminal (GNU/Linux):**
    
    Bash
    
    ```
    cat /proc/timer_list | head -n 25
    ```
    
- **Código en C (Simulación de interrupción periódica con alarmas):**
    
    C
    
    ```
    #include <stdio.h>
    #include <unistd.h>
    #include <signal.h>
    
    void manejador_timer(int sig) {
        printf("[Timer Interrupt] Quantum agotado. Cediendo CPU al planificador...\n");
        alarm(1); // Renueva la interrupción del temporizador cada 1 segundo
    }
    
    int main() {
        signal(SIGALRM, manejador_timer);
        alarm(1);
        printf("Sistema iniciado con multitiempos. Ejecutando procesos...\n");
        for(int i = 0; i < 3; i++) {
            sleep(2); // Simula carga de trabajo
        }
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Timer Interrupt

Plaintext

```
 [ Pulso de Reloj ] ──> [ IRQ de Timer ] ──> [ Interrupción al Kernel ] ──> [ Cambio de Contexto (Preempción) ]
```

# ANEXOS PARA EL TÉRMINO 8: Procesamiento por Lotes (Batch)

## Anexo A (Diagramas y Flujogramas) - Procesamiento por Lotes (Batch)

Fragmento de código

```
sequenceDiagram
    autonumber
    participant User as Usuario / Operador
    participant Queue as Cola de Trabajos (Job Queue)
    participant Monitor as Monitor Batch / Sistema
    participant Output as Dispositivos de Salida

    User->>Queue: Envía lote de tarjetas perforadas / trabajos secuenciales
    Queue->>Monitor: Carga trabajo sin intervención interactiva
    Monitor->>Monitor: Ejecuta programa A hasta finalizar (EOF)
    Monitor->>Output: Vuelca resultados a impresora / cinta
    Monitor->>Queue: Toma automáticamente el siguiente trabajo B
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Batch

- **Trazas de Terminal (GNU/Linux - Uso de la cola batch):**
    
    Bash
    
    ```
    # Enviar un comando a la cola de procesamiento por lotes del sistema
    echo "tar -czf backup.tar.gz /datos" | batch
    atq # Muestra los trabajos en lote pendientes
    ```
    
- **Código en C (Simulador de ejecución secuencial por lotes):**
    
    C
    
    ```
    #include <stdio.h>
    
    void ejecutar_trabajo(const char* nombre, int duracion) {
        printf("[Batch] Ejecutando trabajo: %s (Duracion estimada: %ds)\n", nombre, duracion);
    }
    
    int main() {
        const char* lote_trabajos[] = {"Compilacion_Job1", "Reporte_Job2", "Backup_Job3"};
        for(int i = 0; i < 3; i++) {
            ejecutar_trabajo(lote_trabajos[i], 2);
        }
        printf("[Batch] Lote de trabajos completado secuencialmente.\n");
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Batch

Plaintext

```
 [ Trabajos Agrupados ] ──> [ Cola Secuencial ] ──> [ Ejecución Sin Interacción ] ──> [ Salida Masiva ]
```

# ANEXOS PARA EL TÉRMINO 9: Monitor Residente

## Anexo A (Diagramas y Flujogramas) - Monitor Residente

Fragmento de código

```
sequenceDiagram
    autonumber
    participant RAM as Memoria RAM (Alta / Baja)
    participant Monitor as Monitor Residente (Kernel primitivo)
    participant Job as Programa de Usuario

    Note over RAM, Monitor: El monitor reside permanentemente en memoria protegida
    Monitor->>Job: Carga el primer trabajo desde cinta/lector
    Job->>Job: Ejecuta instrucciones de usuario
    Job->>Monitor: Encuentra macro de control (ej. $END / HALT)
    Monitor->>Monitor: Limpia registros, recupera control y carga siguiente trabajo
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Monitor Residente

- **Trazas de Terminal (Simulación de arranque de un sistema primitivo con monitor):**
    
    Plaintext
    
    ```
    BOOT MONITOR v1.0 - RESIDENT IN HIGH MEMORY
    READY FOR BATCH JOBS...
    LOAD JOB #1 -> OK
    EXECUTION COMPLETE. RETURNING CONTROL TO MONITOR.
    ```
    
- **Código en C (Estructura lógica de control del Monitor Residente):**
    
    C
    
    ```
    #include <stdio.h>
    
    void monitor_residente_loop() {
        int trabajos_pendientes = 2;
        while(trabajos_pendientes > 0) {
            printf("[Monitor Residente] Cargando siguiente trabajo en memoria...\n");
            // Simula ejecución del trabajo de usuario
            printf("[Monitor Residente] Trabajo ejecutado y finalizado con éxito.\n");
            trabajos_pendientes--;
        }
    }
    
    int main() {
        monitor_residente_loop();
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Monitor Residente

Plaintext

```
 [ Memoria Reservada ] ──> [ Control de Carga ] ──> [ Ejecución de Usuario ] ──> [ Retorno de Control ]
```

# ANEXOS PARA EL TÉRMINO 10: Spooling

## Anexo A (Diagramas y Flujogramas) - Spooling

Fragmento de código

```
sequenceDiagram
    autonumber
    participant App as Aplicación de Usuario
    participant Disk as Área de Spool (Disco / Buffer)
    participant Daemon as Demonio de Impresión / E/S
    participant Dev as Dispositivo Físico Lento (Impresora)

    App->>Disk: Escribe datos rápidamente al archivo de spool en disco
    App->>App: Continúa su ejecución inmediata sin esperar al hardware
    Disk->>Daemon: El demonio lee el spool en segundo plano de forma concurrente
    Daemon->>Dev: Envía los datos a velocidad nominal del periférico físico
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Spooling

- **Trazas de Terminal (GNU/Linux - Sistema de Spool de impresión CUPS):**
    
    Bash
    
    ```
    lpq # Consulta la cola de spool de impresión
    lp -d impresora_oficina documento.pdf # Envía al spool
    ```
    
- **Código en C (Simulación básica de escritura a buffer intermedio / Spool):**
    
    C
    
    ```
    #include <stdio.h>
    
    void enviar_a_spool(const char* datos) {
        FILE *spool_file = fopen("print_spool.tmp", "a");
        if (spool_file) {
            fprintf(spool_file, "%s\n", datos);
            fclose(spool_file);
            printf("[Spooling] Datos almacenados en disco temporal para procesamiento diferido.\n");
        }
    }
    
    int main() {
        enviar_a_spool("Documento de prueba para spooling de impresión.");
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Spooling

Plaintext

```
 [ Solicitud Rápida ] ──> [ Almacenamiento en Disco (Spool) ] ──> [ Demonio de Fondo ] ──> [ Dispositivo Lento ]
```

# ANEXOS PARA EL TÉRMINO 11: Multiprogramación

## Anexo A (Diagramas y Flujogramas) - Multiprogramación

Fragmento de código

```
sequenceDiagram
    autonumber
    participant JobA as Trabajo A (En RAM)
    participant JobB as Trabajo B (En RAM)
    participant CPU as Procesador
    participant IO as Operación de E/S

    JobA->>CPU: Ejecuta instrucciones
    JobA->>IO: Solicita operación de E/S (Bloqueo)
    Note over CPU, JobB: El CPU no queda inactivo; conmuta a Job B
    JobB->>CPU: Utiliza el procesador mientras A espera la E/S
    IO-->>JobA: E/S finalizada, Job A pasa a listo
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Multiprogramación

- **Trazas de Terminal (GNU/Linux - Ver procesos concurrentes en memoria):**
    
    Bash
    
    ```
    ps -ef --forest
    ```
    
- **Código en C (Simulación de concurrencia mediante procesos independientes - Multiprogramación):**
    
    C
    
    ```
    #include <stdio.h>
    #include <unistd.h>
    #include <sys/types.h>
    
    int main() {
        pid_t pid = fork(); // Crea un nuevo flujo de ejecución residente en memoria
        if (pid == 0) {
            printf("[Programa B en RAM] Ejecutando tareas secundarias concurrentes...\n");
        } else {
            printf("[Programa A en RAM] Ejecutando tareas principales concurrentes...\n");
        }
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Multiprogramación

Plaintext

```
 [ Múltiples Trabajos en RAM ] ──> [ Espera de E/S Oculta ] ──> [ Mayor Ocupación de CPU ] ──> [ Aumento de Throughput ]
```

# ANEXOS PARA EL TÉRMINO 12: Tiempo Compartido

## Anexo A (Diagramas y Flujogramas) - Tiempo Compartido

Fragmento de código

```
sequenceDiagram
    autonumber
    participant U1 as Usuario 1 (Terminal)
    participant U2 as Usuario 2 (Terminal)
    participant CPU as CPU (Conmutación por Quantum)
    participant Sched as Planificador Round Robin

    loop Reparto Equitativo de Tiempo
        Sched->>CPU: Asigna Quantum a Usuario 1
        U1->>CPU: Ejecuta proceso interactivo breve
        Sched->>CPU: Interrumpe por Timer e intercala Usuario 2
        U2->>CPU: Ejecuta proceso interactivo breve
    end
```

## Anexo B (Trazas de Terminal y Código de Ejemplo) - Tiempo Compartido

- **Trazas de Terminal (GNU/Linux - Estado de carga interactiva del sistema):**
    
    Bash
    
    ```
    uptime
    top -b -n 1 | head -n 10
    ```
    
- **Código en C (Estructura de Round Robin / Simulación de planificación por tiempo compartido):**
    
    C
    
    ```
    #include <stdio.h>
    
    struct Proceso {
        int id;
        int tiempo_restante;
    };
    
    int main() {
        struct Proceso p1 = {1, 5};
        struct Proceso p2 = {2, 3};
        int quantum = 2;
    
        printf("Simulando Tiempo Compartido con Quantum = %d\n", quantum);
        printf("Proceso %d ejecuta %d unidades de tiempo.\n", p1.id, quantum);
        printf("Proceso %d ejecuta %d unidades de tiempo.\n", p2.id, quantum);
        return 0;
    }
    ```
    

## Anexo C (Mapa de Relaciones) - Tiempo Compartido

Plaintext

```
 [ Múltiples Usuarios / Terminales ] ──> [ Asignación de Quantum (Timer) ] ──> [ Conmutación Rápida ] ──> [ Ilusión de CPU Dedicada ]
```

### Referencia
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). _Operating System Concepts_ (10.ª ed.). Wiley. Capítulo 3