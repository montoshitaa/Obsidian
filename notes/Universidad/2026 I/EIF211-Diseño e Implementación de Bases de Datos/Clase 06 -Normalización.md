---
Semestre: "[[a. I Semestre]]"
tags:
  - UNA
fecha: 2026-03-17
---
---
Normalizar se hace para:
- Evitar redundancia 
- Prevenir anomalías
- Proteger identidad
- Facilitar acceso
# 3FN Dominios atómicos
No debe haber listas o valores múltiples en las celdas.
# 2FN Dependencia total
Todo atributo no clave debe depender de la clave primaria completa. 
![[Pasted image 20260317145905.png|472]]
# 3FN Cero transitividad
Eliminar dependencias en cadena
![[Pasted image 20260317150217.png|432]]
# BCNF - Forma Normal de Boyce Codd
**Super claves estrictas:** 
![[Pasted image 20260317150410.png|432]]
# 4FN Aislar Multivalores
Separar conjuntos independientes 1:N que artificialmente generan productos cartesianos. 
![[Pasted image 20260317150747.png|434]]
# 5FN Proyecciones puras
