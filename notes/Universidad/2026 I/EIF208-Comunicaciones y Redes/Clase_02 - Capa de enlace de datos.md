---
fecha: 2026-03-05
Semestre: "[[a. I Semestre]]"
---
---
## Capa de Enlace de Datos
Prepara los datos para la red física. Convierte de bits a tramas y de tramas a bits.
Se encarga de: 
- Permite a las capas superiores acceder a los medios usando técnicas como tramas.
- Controla cómo se ubican los datos en los medios y cómo se reciben desde los medios usando técnicas como el control de acceso a los medios y la detección de errores.
En resumen, se encarga de:
- Encapsula los datos en tramas
- Detecta errores 
- Controla accesos
Estándares:
- ISO: HDLC (Control de enlace de datos de alto nivel)
- IEEE: 
	- 802.2 (LLC)
	- 802.3 (Ethernet)
	- 802.5 (Token ring)
	- 802.11 (Wireless LAN), cambió a wifi 6A
- ITU: 
	- Q.922 (Estándar de frame relay)
	- Q.921 (Estándar de enlace de datos ISDN)
	- HDLC (Control de datos de alto nivel)
- ANSI:
- 
### Trama

### Un encabezado tiene
- Inicio de trama:
- Dirección:
- Tipo: 
- Control:
### Topología 
Como se muestra la conexión entre los nodos a la capa de enlaces. 
- Física: La conexión física de dispositivos a través de elementos físicos. (capa 1 y 2)
- Lógica: No le importa las conexiones internas mientras funcione (capa 3)
De que tamaño es el espacio de la trama en el sector del encabezado: 48 bits