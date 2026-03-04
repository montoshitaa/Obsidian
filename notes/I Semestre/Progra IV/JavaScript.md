NodeJS es un entorno que permite ejecutar java script fuera del navegador. 
JavaScript es el lenguaje que permite la lógica e interacción en aplicaciones web, trabajando junto con HTML y CSS en el frontend y usando HTTP para comunicarse con servidores.

Generalmente hay un patrón que se sigue en un código .js:
1. Importaciones (si se usan módulos)
		`const express = require("express");`
2. Configuración inicial
		`const app = express();`
3. Punto de arranque
		`app.listen(3000);`
Se usa en:
- En el navegador (frontend):
	- responder a clics (agregar un producto a un carro)
	- validar formularios
	- actualizar contenido sin recargar
	- crear interfaces dinámicas
- En el servidor (backend):
	-  crear APIs
	- manejar usuarios
	- conectar bases de datos
	- autenticar sesiones