---
fecha: 2026-03-12
tipo: "[[Universidad]]"
Pages:
Cap: 3-4
---
--- 
## Proceso
Representa un programa que está siendo ejecutado por el sistema.
Incluye:
- **Contador del programa:**
- **Registros del CPU:**
- **Stack:**
- **Heap:**
- **Variables Globales:**
### Estado del Proceso 
La condición del proceso dentro del sistema operativo, gracias a esto el SO puede controlar qué procesos usan la CPU. 
Estados principales:
- **Nuevo:** Está siendo creado por el SO.
- **En ejecución:** Está utilizado actualmente el procesador. 
- **En espera:**
- **Preparado:**
- **Terminado:** 

### Propiedades del Sistema de Estados 
- **Solo un proceso puede ejecutarse por CPU:**
- **Pueden existir muchos procesos preparados o en espera:**
- **Los estados pueden variar según el SO:** 
### Bloque de Control de Proceso
Contiene toda la información necesaria para que el SO pueda gestionar, controlar y reanudar la ejecución de un proceso. El PCB actúa como registro o ficha del proceso para FALTA
Información almacenada en el PCB:
- Estado del proceso:
- Número de proceso
- 
- Registros de la CPU:
- Información de planificación de la CPU:
- Información de gestión de memoria:
- Información contable:
- Información del estado de entrada/salida: 

> [!NOTE]
> Programa pasivo / Proceso activo

## Hilo
### Hilo de ejecución
En un modelo básico de procesos, se asume que un proceso tiene un solo hilo de ejecución, o sea una única secuencia de instrucciones que se ejecuta paso a paso en el procesador, o sea que el programa solo puede ejecutar un 

## Planificación de Procesos
El planificador de procesos es el encargado de selecciona uno de los procesos disponibles y asignarle la CPU. El plani
### Objetivos de la Planificación
- Multiprogramación:
- Sistemas de tiempo compartido: 
e### Colas de Planificación 
Estructura donde los procesos esperan su turno para asignar algún recurso del sistema como la CPU o un dispositivo de E/S
### Cola de Procesos Preparados (Ready Queue)
Los procesos que se encuentran en memoria principal y están listos para ejecutarse se colocan en una lista llamada cola de procesos preparados. El planificador selecciona un proceso 
### Colas de Dispositivos 
Cuando un proceso solicita una operación de E/S 
### Tipos de Planificadores
### Cambio de Contexto 

### Razones para la cooperación entre procesos

## Modelos de comunicación entre procesos 
## Comuncación en Sistemas Cliente-Servidor

modelos principales de comunicación entre procesos 