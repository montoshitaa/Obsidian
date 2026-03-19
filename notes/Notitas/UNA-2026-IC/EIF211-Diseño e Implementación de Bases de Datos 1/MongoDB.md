---
fecha: 2026-03-10
tipo: "[[Universidad]]"
tags:
  - UNA
---
--- 
## Crear contenedor 
Crear contenedor con credenciales 
	docker run -d \
	-p 27017:27017 \
	--name mongodb \
	-e MONGO_INITDB_ROOT_USERNAME=admin \
	-e MONGO_INITDB_ROOT_PASSWORD=admin \
	-v mongo_data:/data/db\
	mongo:7
### Comandos 
- Ver contenedores corriendo 
	docker ps
- Ver todos los contenedores 
	docker ps -a
- Detener el contenedor 
	docker stop mongodb
- Iniciarlo 
	docker start mongodb
- Reiniciarlo 
	docker restart mongodb
- Eliminarlo (solo si está detenido)
	docker rm mongodb
### Consultas 
- Estructura básica de una consulta
	db.coleccion.find(filtro, proyeccion)

#### Filtrar
Para establecer la condición que se necesita cumplir
	{ sede: "Coto" }

#### Proyectar 
Establece que elementos mostrar 
	{ nombre: 1, edad: 1, _id: 0 }
#### Operadores 
- Menor que
	edad: { $lt: 20 }
- Mayor que
	