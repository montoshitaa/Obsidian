## VirtualBox
### Descarga y configuración
- Instalar: 
	sudo pacman -S distrobox podman
	Descargar crun como runtimeOCI 
- Luego inicia el servicio de podman para tu usuario:
	systemctl --user enable --now podman.socket
- Verificar la descarga:
	distrobox --version
- Crear el contenedor 
	distrobox create --name node-web --image ubuntu:24.04
- Entrar
	distrobox enter node-web
- Actualizar el sistema
	sudo apt update
- Instalar Node
	sudo apt install nodejs npm
- Verificar la instalación
	node -v
	npm -v
- Para saber si estoy dentro, debe devolver podman:
	echo $container

## Starship
Para hacer que la terminal se vea bonita
- Instalar 
	sudo pacman -S starship
- Activarlo
	nano ~/.zshrc
	Agregar al final: eval "$(starship init zsh)"
- Configurarlo
	mkdir -p ~/.config
	nano ~/.config/starship.toml
- Pegar:
	add_newline = false
	
	[container]
	symbol = "📦 "
	format = "[$symbol$name]($style) "
	
	[git_branch]
	symbol = "🌱 "
	
	[nodejs]
	symbol = "⬢ "
- Descargar la fuente correcta
	sudo pacman -S ttf-jetbrains-mono-nerd
## Docker 
- Instalar 
	sudo pacman -S docker
- Arrancar el servidor 
	sudo systemctl enable --now docker
- Agregar el usuario 
	sudo usermod -aG docker $USER
- Crear contenedor con credenciales 
	docker run -d \
	-p 27017:27017 \
	--name mongodb \
	-e MONGO_INITDB_ROOT_USERNAME=admin \
	-e MONGO_INITDB_ROOT_PASSWORD=admin \
	-v mongo_data:/data/db\
	mongo:7
- Para poner mongodb sin credenciales 
	docker run -d -p 27017:27017 --name mongodb mongo
	sin asignarle puerto: docker run -d -P --name mongodb4 mongo
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
	- Luego de eliminarlo se debe eliminar el volumen
		docker volume rm mongo_data
## Latex
- Descargarlo
	sudo pacman -S texlive
- Agregar en visual la extensión
	LaTeX Workshop
