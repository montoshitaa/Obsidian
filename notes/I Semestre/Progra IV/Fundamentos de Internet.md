---
tags:
  - Redes
  - Internet
  - WWW
---
https://caniuse.com/

### Analogía Básica 
- **Internet:** La infraestructura de las carreteras y rutas, para comunicarnos. Infraestructura que sostiene la red
- **La Web:** Servicio que utiliza esas carreteras para entregar paquetes de información. 
- **HTTP/HTTPS:** Las reglas de envío (qué se pide, como se responde). 
- **Navegador:** La persona mensajera (cliente) que hace pedidos. 
- **Servidor:** El centro que prepara y entrega la respuesta. 
### WWW
World Wide Web, nace en una universidad donde se conectan varias computadoras a través de un protocolo, de ahí va creciendo y se expande gracias a una inversión militar. Es una red informática que conecta dispositivos a través de todo el mundo. 
En sí es un sistema de distribución basado en hipertexto o hipermedios enlazados a través de internet. En sí eran archivos de texto con formato (como XML), donde cada archivo tenía una ruta. 
**Brinda:**
	- Portabilidad implícita en sistemas
	- Despreocipación de múltiples instalaciones 
	- Corrección inmediata de errores (fácil soporte y mantenimiento)
	- Fácil colaboración entre desarrolladores (sincronización)
	- Fácil manipulación de las interfaces gráficas y controles de usuario
	- Centralización de la información y estadística en tiempo real
**Usada en Sistemas:**
	-Transaccionales 
	-Informativos / Publicación
	-Edición de Contenido 
	-Desarrollo (software general, móvil, etc)
	-Entretenimiento
	-Comunicación instantánea / Colaboración / Redes Sociales
	-Ofimática / Educación
	-Almacenamiento 
	-Geolocalización /  Metereología
**Ventajas:** 
	Facilidad de manejo
	Accesibilidad
	Portabilidad
	Facilidad de Desarrollo 
	Comunicación instantánea
	Sincronización
	Estándares
	Soporte Mundial
	Alcance 

> [!NOTE]
> La W3C o World Wide Web Consortium es la encargada de crear los estándares de la web.
> Internet: Red global de redes. Con conectividad y enrutamiento 
> Web: Sistema de recursos identificados por URL, consumidos principalmente vía HTTP/HTTPS.
#### Request 
Es un mensaje que el cliente le envía a un servidor para solicitar algo. 
	Cliente → Request → Servidor → Response
Como viaja un request:
1. Ingresar URL 
		Uniform Resource Locator, la dirección que indica donde se encuentra un recurso en internet. 
			https://   www.google.com   /search   ?q=gatos
			- **https://** → protocolo (cómo conectarse)  
			- **www.google.com** → dominio (servidor)  
			- **/search** → ruta del recurso  
			- **?q=gatos** → parámetros (datos enviados)
2. Resolver DNS 
		Domain Name System, sistema que traduce de nombres a direcciones IP. 
		google.com  →  142.250.190.14
3. Abrir conexión 
4. Negociar TLS 
		Transport Layer Security, protocolo que cifra y protege la información que viaja entre el navegador y el servidor. HTTPS tiene S de secure. 
5. Enviar y recibir 
#### Navegadores 
Se debe procurar que las aplicaciones desarrolladas y sitios web funcionen de forma óptima en la mayoría de los navegadores modernos  (crossbrowsing) y dispositivos (resoluciones).
### Cliente vs Servidor 
**Cliente:** Software ejecutado en el navegador (Carritos de compra, mensajería, redes sociales)
	No es necesario instalar ningún software
	Se va a centrar en la interfaz de usuario e interacción, tiene parte lógica y validación de UX.

**Servidor**: Software que corre en el servidor, es el encargado de devolver la información de las páginas web. 
	Requiere acceso a internet, disponibilidad 24/7, seguridad, recursos y protocolos. 
	Reglas de servicio, persistencia, seguridad y validación definitiva. 
	La seguridad vive en el servidor, nunca hay que confiar en las validaciones del cliente. 
#### Conceptos
- Método: Intención (GET, POST, PUT...)
- URL: Recurso 
- Headers: Metadatos 
- Body: Datos
- Status Code: Resultado 
#### Métodos HTTP
- **GET:** Leer
- **POST:** Crear o ejecutar algo 
- **PUT**: Reemplazo completo 
- **PATCH:** Actualización parcial 
- **DELETE:** Eliminar 
#### Status Code 
**Éxito:** 
	200 OK
	201 Created
	204 No content 
**Redirecciones:** 
	301/302
**Errores cliente:** 
	400 (request mal formado)
	401 (sin autenticación válida)
	403 (sin permiso)
	404 (no existe)
	409 (conflicto)
	422 (validación)
**Errores servidor** 
	500/502/503 (fallo, getaway, indisponibilidad)
### Headers 
Es información adicional que acompaña un request o un response para indicar cómo deben manejarse los datos. 
Contiene: 
- Content-type: Cómo interpretar el body
- Accept: Qué formato espera el cliente 
- Authorization: Credenciales
- Cache-control /ETag: Rendimiento y costos
- CORS headers: Acceso entre orígenes 
	![[Pasted image 20260216202325.png]]

### Conceptos web
- **HTML:** HyperText Markup Languaje, lenguaje etiqueetado de hipertexto que conforma una codificación basada en etiquetas enfocaso en dar la estructura náscia de bloques de construcción de una página web y sus elementos 
- **CSS:** Cascade Style Sheet, hoja de estilo en cascada que conforman una codificación de diversas propiedades de los elementos HTML según su ID, Clase o Tipo para su respectivo diseño y apariencia. 
- **JavaScript**: Lenguaje interpretado para uso del lado del cliente en páginas dinámicas utilizado para el diseño de animaciones, eventos locales, alertas, validaciones, etc.
- **URL:** Un localizador de recursos uniforme, es una secuencia de caracteres, de acuerdo a un formato modélico y estándar, que se usa para nombrar recursos en Internet para su localización o identificación
- **Aplicación**: Software de funciones específicas creado en ambiente WEB/Mobile.
- **Sitio web**: Conforma un conjunto de elementos previamente diseñados bajo tecnología WEB con un propósito específico de desplegar información o brindar un servicio.
- **HTTPS (TLS):** TLS aporta confidencialidad, integridad y autenticidad. 
		 Errores típicos: 
	- Mixed content (HTTP dentro del HTTPS)
	- Certificado expirado o mal emitido
	- Configuración débil
#### Seguridad web 
- Credenciales seguras: Nunca  enviar credenciales por HTTP
- Cookies protegidas: Cookies con HttpOnly, Secure, SameSite
- Validar entrada: Sanitizar y validar siempre
- Tokens seguros: Evitar tokens en localStorage
- CSP: Content-Security-Policy si el stack lo permite
#### REST 
REST es un estilo arquitectónico para diseñar APIs sobre HTTP.
- Recursos: Identificados por URL
- Métodos HTTP: Expresan intención
- Representaciones: JSON, etc.
- Stateless: Sin estado entre requests
Errores comunes:
- Endpoints con verbos
- Responder 200 a todo
- No validar input
- No documentar
Checklist de calidad: 
- Consistencia en rutas y nombres
- Status codes correctos
- Validación y errores con forma estándar
- Paginación y filtros
- Idempotencia cuando aplica
- Observabilidad: logs, trazas, request-id
#### API "Stateless"
Cada request debe traer lo necesario para ser entendido, no significa que no haya un estado en la app. 
El estado se maneja mediante:
- Cookies
- Tokens (por ejemplo, JWT)
- Sesiones (session id → estado guardado en servidor)
Permite:
- Escalado horizontal
- Caché
- Balanceadores
#### WebSocket:
Protocolo de comunicación bidireccional y persistente que permite intercambio de datos en tiempo real entre cliente y servidor, usado en chat, dashboards en vivo, colaboración.
- **HTTP clásico:** Como "enviar cartas": cada interacción abre-cierra
		Ideal para CRUD
		Caché y tooling maduro
		Más simple de desplegar
- **WebSocket:** Como "una llamada": se abre un canal y ambas partes hablan cuando quieran
		Conexión persistente
		Baja latencia para eventos
		Más complejidad: estado, escalado, reconexión
#### PWA
Aplicación web que se comporta como una app nativa, pero se ejecuta desde el navegador.
	Service Workers
	Web App Manifest
	HTTPS
**Características:** 
- Funciona en cualquier navegador moderno
- Se puede instalar en el dispositivo (sin App Store)
-  Carga rápida y alto rendimiento
-  Puede funcionar offline o con baja conexión
- Soporta notificaciones push
**Beneficios:** 
- Menor costo de desarrollo (una sola base de código)
- Multiplataforma (web, móvil, desktop)
- Mejor experiencia de usuario
- No requiere descargas desde tiendas
#### La nube y sus servicios
- **Frontend:** Hosting estático + CDN (Vercel, Netlify, Cloudflare)
- **API:** Contenedores o serverless (AWS Lambda, Cloud Run)
- **Base de datos**: Administrada (RDS, Cloud SQL, Supabase)
- **Storage**: Objetos para archivos (S3, Cloud Storage)
- **Observabilidad:** Logs, métricas, alertas (Datadog, Sentry)

Buscar PDA de aplicaciones que usemos

