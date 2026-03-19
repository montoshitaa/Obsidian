### Una aplicación no abre el navegador (inicio de sesión)

Verificar si el portal está corriendo:
	systemctl --user status xdg-desktop-portal
Si no está activo, instálalo:
	sudo pacman -S xdg-desktop-portal
Instala el backend compatible:
	sudo pacman -S xdg-desktop-portal-gtk
Darle permiso a Flatpak de abrir el navegador
	flatpak override --user --talk-name=org.freedesktop.portal.Desktop md.obsidian.Obsidian
Descargar las utils 
	sudo pacman -S xdg-utils