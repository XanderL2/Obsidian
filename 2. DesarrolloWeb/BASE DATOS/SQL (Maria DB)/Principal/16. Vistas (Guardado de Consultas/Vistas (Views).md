
---
## ¿Que es una Vista?
Una vista no es mas que la tabla devuelta por una consulta transformada en una tabla virtual. Es importante saber que esta consulta sera interpretada cada que llamemos o hagamos referencia a la vista, por lo que tendra un alto impacto en el rendimiento. 

## Ejemplo de una Vista:
Aqui estamos creando una vista, es decir una nueva tabla virtualizada a partir de una consulta.

![[Pasted image 20240209181659.png]]

Y esta es la tabla que crearemos, cada que hagamos referencia a esa vista se ejecutara toda esa consulta, ademas debemos tener en cuenta que si los datos originales cambian en la vista tambien cambiaran:

![[Pasted image 20240209181808.png]]

