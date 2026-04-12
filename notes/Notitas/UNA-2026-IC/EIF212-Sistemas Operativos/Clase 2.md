---
fecha: 2026-02-26
tipo: "[[Universidad]]"
tags:
  - UNA
---
## Tipos de Sistemas Operativos
### Básicos 
También llamados de propósito general, diseñados para brindar un entorno completo de trabajo al usuario. Permitir el uso de la computadora para realizar diferentes actividades como trabajar, jugar, programar. Están preparados para ejecutar múltiples programas al mismo tiempo, administrar los recursos y facilitar la interacción al usuario. 
- Windows 
### Distribuidos 
Conjunto de computadoras que se encuentran en distintos lugares, pero están conectadas por una red y trabajan juntas para ofrecer servicios o recursos, comparten información, programas y capacidad de procesamiento, permite una mayor tolerancia por si alguna falla. 
El protocolo más utilizado es TCP/IP. 
	Sistema operativo distribuido de red cada dispositivo es autónomo, mientras que en el operativo distribuido el trabajo se reparte.
### Tiempo Real y Embebidos 
### Embebidos en tiempo real 
Pequeñas computadoras que vienen incorporadas FALTA
	Circuitos ASIC los cuales realizan una tarea simple sin la necesidad de un SO. 
### Sistemas Multimedia 
Son aquellos que permiten a los sistemas operativos manejar datos como audio y video, los cuales se diferencias de los datos tradicionales porque 
### Sistemas de mano 
Dispositivos electrónicos pequeños y portátiles
Una de sus principales limitaciones es la memoria, por lo que las aplicaciones deben ir liberando memoria y administrar mejor el consumo de batería.  Otra dificultad es la entrada y salida de información por su teclado pequeño y pantallas táctiles. 
- Celulares
- Asistentes personales PDA

### Estructura del Sistema Operativo 
Un SO debe hacerse 
#### La estructura simple 
Se refiere a SO que no están organizados en partes o módulos bien definidos. Suelen comenzar pequeños y con funciones limitadas, pero van creciendo sin una planificación clara, lo que lo hace mezclado. No existe una separación entre funciones, por lo que los programas pueden acceder FALTA
#### Estructura en Niveles 
Forma de organizar dividiéndolo en partes más pequeñas y manejables (capas o niveles). Surge gracias al soporte del hardware moderno. 
En la parte inferior va el hardware (nivel 0) y en el nivel más alto va la interfaz de usuario. Cada nivel solo puede usar los servicios proporcionados por los niveles inferiores, imponiendo una jerarquía. Esta estructura brinda simplicidad en construcción y FALTA 
Cada nivel oculta sus detalles internos a los niveles superiores, permitiendo mejorar un nivel sin afectar al resto. 
Su principal reto es el definir correctamente que funciones pertenecen a cada nivel, también suele ser menos eficiente, pues cuando una aplicación solitica una 
#### Microkernels 
Modulariza el kernel para mantener dentro del kernel únicamente las funciones esenciales y mover todo lo demás 
Ofrecen una gestión mínima de memoria y procesos, pero con un mecanismo de comunicación eficiente.
#### Modulos 
El sistema se organiza en partes con responsabilidades bien definidas, en lugar de que el kernel sea solo un bloque, se crea un kernel central pequeño, con funciones esenciales y 
#### Máquina Virtual
Permite que una computadora se "divida" en varias computadoras virtuales, creando entornos de trabajo separados, de forma que cada uno parezca un dispositivo independiente. 
El problema es el manejo de discos 
	Implementación: Para ello se usa un mo
	Beneficios: Ofrece protección entre entornos, pocr lo que un error no afecta directamente a otras, pero tampoco pueden compartir recursos directamente. 