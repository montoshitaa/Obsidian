#### Huella
	sudo pacman -Syu fprintd libfprint
Registrar huella
	fprintd-enroll
Para revisar que se haya registrado bien
	fprintd-verify
##### Para sudo 
	sudo nano /etc/pam.d/sudo
Al inicio poner 
	auth sufficient pam_fprintd.so
##### Uso general 
	sudo nano /etc/pam.d/system-auth
	
Encima de las líneas `pam_unix.so` : 
`auth      sufficient pam_fprintd.so`

##### SDDM 
	sudo nano /etc/pam.d/sddm
Al inicio 
	auth sufficient pam_fprintd.so

#### Btrfs + snapshots + Snapper + GRUB
>Btrf: Sistema de archivos que congela el sistema
>Snapper: Gestor de snapshots
>Grub: Permite arrancar en un snapshot 
##### Implementación 
Confirmar que / es btrf:
	findmnt /
Ver subvolúmenes 
	sudo btrfs subvolume list /

Instalaciones
	sudo pacman -S snapper snap-pac grub-btrfs
	
Verificar si hay una configuración de snapper para / 
	snapper list-configs
	Si no hay, crearla
	sudo snapper -c root create-config /

Ajustar permisos
	sudo chmod 750 /.snapshots
	sudo chown :wheel /.snapshots

Activar snapshots automáticos
	sudo systemctl enable --now snapper-timeline.timer
	sudo systemctl enable --now snapper-cleanup.timer

Configurar snapper
	sudo nano /etc/snapper/configs/root
		Revisar valores:
			TIMELINE_CREATE="yes"
			TIMELINE_LIMIT_HOURLY="5"
			TIMELINE_LIMIT_DAILY="7"
			TIMELINE_LIMIT_WEEKLY="4"
			TIMELINE_LIMIT_MONTHLY="2"

**Integrar con grub**
Activar el servicio 
	sudo systemctl enable --now grub-btrfsd.service
		
Regenerar grub
	sudo grub-mkconfig -o /boot/grub/grub.cfg

**Probar que funcionó**
Crear snapshot manual 
	sudo snapper -c root create --description "snapshot de prueba"
Ver las snapshots
	snapper -c root list
Reiniciar y ver que esté ahí 
	reboot
