pg 1- 
### Sistema de Administrador de Bases de Datos (SABD)
Conjunto de programas que actúan como intermediario esencial. Un software complejo que gestiona el acceso, la seguridad y la consistencia. 
	A database-management system (DBMS) is a collection of interrelated data and a set
	of programs to access those data. The collection of data, usually referred to as the
	database, contains information relevant to an enterprise. The primary goal of a DBMS
	is to provide a way to store and retrieve database information that is both convenient
	and eﬃcient.
	 Management of data involves both deﬁning structures for storage of information and providing mechanisms for the manipulation of information. 
	Key to the management of complexity is the concept of abstraction. Abstraction allows a person to use a complex device or system without having to know the details of how that device or system is constructed.
#### Formas de uso de las BD:
- The ﬁrst mode is to support online transaction processing, where a large number of users use the database, with each user retrieving relatively small amounts of data, and performing small updates.
- The second mode is to support data analytics, that is, the processing of data to draw conclusions, and infer rules or decision procedures, which are then used to drive business decisions.
#### Problemas de los sistemas basados en archivos
This typical ﬁle-processing system is supported by a conventional operating system. The system stores permanent records in various ﬁles, and it needs diﬀerent application programs to extract records from, and add records to, the appropriate ﬁles.

| Problema | Descripción | Ejemplo del texto |
|----------|-------------|------------------|
| **Redundancia e inconsistencia** | La misma información se duplica en varios archivos, lo que puede generar versiones contradictorias y aumenta el costo de almacenamiento y acceso. | Un estudiante con doble especialidad (Música y Matemáticas) tiene su dirección y teléfono en dos archivos distintos. Si cambia su dirección en uno pero no en el otro, los datos quedan inconsistentes. |
| **Dificultad para acceder a datos** | Las consultas no previstas originalmente requieren desarrollar nuevos programas, lo que hace el proceso lento e ineficiente. | Un empleado necesita listar estudiantes por código postal. Como no existe un programa para eso, debe extraer manualmente la información de una lista general o solicitar un nuevo desarrollo. |
| **Aislamiento de datos** | Los datos están dispersos en archivos con diferentes formatos y estructuras, dificultando su integración en nuevas aplicaciones. | Escribir un programa que combine información de estudiantes, cursos y departamentos es complejo porque cada archivo tiene su propio formato y ubicación. |
| **Problemas de integridad** | Las restricciones de consistencia (ej: "saldo ≥ 0") se implementan dentro de cada programa, haciendo difícil añadir o modificar reglas globalmente. | Si la universidad añade una nueva regla de validación académica, hay que modificar todos los programas que manejan datos relacionados para que la respeten. |
| **Problemas de atomicidad** | Las operaciones que deben ejecutarse completamente o no ejecutarse en absoluto pueden quedar en estado inconsistente ante fallos del sistema. | En una transferencia de $500 de la cuenta A a la B, si el sistema falla después de debitar A pero antes de acreditar B, el dinero "desaparece". |
| **Anomalías por acceso concurrente** | Cuando múltiples usuarios actualizan los mismos datos simultáneamente sin coordinación, pueden generarse resultados incorrectos. | Dos estudiantes se registran al mismo tiempo en un curso con cupo 40 y contador en 39: ambos leen 39, ambos escriben 40, y el contador final es incorrecto (debería ser 41). |
| **Problemas de seguridad** | Es difícil controlar el acceso diferenciado a datos sensibles cuando los programas se desarrollan de forma independiente y ad hoc. | El personal de nómina debería ver solo información financiera, pero en un sistema de archivos es complejo restringir su acceso a registros académicos. |
#### 