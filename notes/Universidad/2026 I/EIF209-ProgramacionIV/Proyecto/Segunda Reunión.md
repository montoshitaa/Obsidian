---
fecha: 2026-03-15
tipo: "[[Universidad]]"
Semestre: "[[a. I Semestre]]"
---
---
# Prisma 
Es un gestor de bd con ORM que se encarga de mapear y realizar queries en código más sencillo, monta la bd, la llen de datos, valida...
Hace que cambiar de script para la bd sea mucho más sencillo, permite migrar usando un sistema de tracking de cambios como el de git. Toma una "foto" del estado actual del sript y cuando haya uno nuevo, solo le agrega o modifica los cambios nuevos. 
Funciones como: 
- `prisma migrate deploy` = actualiza la base de datos usando las migraciones que ya existen en el proyecto. 
- `npx prisma db seed` = agrega datos de prueba o datos básicos automáticamente
- `npx prisma db pull` = “Mira mi base de datos y crea los modelos automáticamente.”
- `prisma generate`  = Genera el **Prisma Client**, que es el código que usas para consultar la base de datos.

- prisma.config es el archivo base de la configuración de prisma, no se debería tocar
- schema.prisma es un sql un poco diferente
## ORM (object relational mapper)
Mapea un objeto hacia la base de datos. Relaciona un objeto con una bd.  
Permite métodos como *ORM.usuario.crear(string)*. Esto para evitar usar queries para manipular la base de datos. 

Toda la información está documentada en el readme y la carpeta de documentación. 