---
Semestre: "[[a. I Semestre]]"
---
---
# Esquema Conceptual 
- Convierte necesidades abstractas en un modelo lógico de datos, asegura que no existan conflictos de información y evita errores mediante una visión global.
# Instancia vs Entidad
- Entidad: Un objeto distinguible.
- Instancia: Una ocurrencia física de esa entidad. 
# Relaciones 
Establecen un vínculo entre entidades. EL rombo es el símbolo universal de la relación.
## Grados de la Relación
- **Grado 1 (reflexiva):** Una entidad relacionada consigo misma.
- **Grado 2(binaria):** Dos entidades relacionadas, las más típicas.
- **Grado 3(ternarias):** Tres entidades independientes unidas simultáneamente por un único conjunto de relaciones.
- **N-arias:** Superiores a grado 3, redes altamente complejas. 
# Cardinalidad de Asignación 
La flecha es como un tope que indica solo unos. 
![[Pasted image 20260316231047.png|573]]
# Participación y Límites (min, max)
![[Pasted image 20260316231232.png]]
Las líneas dobles indican una participación total, es decir, todas las instancias de esa entidad deben participar obligatoriamente en la relación. 
# La dependencia 
- Entidad fuerte: Existe por sí misma.
- Entidad débil: Depende completamente de la entidad propietaria. Su clave primaria se forma uniendo la Clave Primaria Fuerte + su propio discriminador. 
- Discriminador: Atributo con línea discontinua que distingue entidades fuertes de débiles. 
# Generalización y Herencia 
Al leer de arriaba hacia abajo, se dice que persona generaliza de empleado.
Pero de abajo hacia arriba, empleado hereda de persona. Se identifica la relación con un triangulo hacia abajo. 