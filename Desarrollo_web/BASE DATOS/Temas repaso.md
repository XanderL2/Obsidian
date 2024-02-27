 ---
## Union
|
## Group By y Having Siempre juntos:
Si queremos filtrar lo dado por un GROUP BY usaremos el HAVING, asi que es algo a considerar.

```sql
SELECT ciudad, COUNT(id) AS cantidad 
FROM usuarios 
GROUP BY ciudad
HAVING COUNT(id) > 2;
```


## HAVING PARA COMPARAR CON FUNCIONES Y ALIAS DIRECTAMENTE:

El where no tiene la capacidad para comparar con funciones ni con alias directamente, por lo que podemos usar el HAVING para comparar con funciones directamente.  Ejemplo:

Si queremos devolver precios menores a la media

```sql
###  ERRONEO ##
SELECT * FROM productos WHERE precio < AVG(precio) ### DARIA ERRORR###


###  CORRECTO ##

SELECT * FROM productos HAVING precio < AVG(precio) ### DARIA ERRORR###
```



## Comparar fechas:
Las Fechas son tratadas como strings, pero se pueden operar con ellas. Ejemplo:

Seleccionar los pedidos realizados después del 2023-01-15.
```sql
SELECT * FROM pedidos WHERE fecha_pedido > '2023-01-15';
```


## Ver si los valores de una columna estan o no en otra:
Usaremos una especie de subconsulta para esto, haciendo un SELECT doble:

```sql
SELECT * FROM usuarios WHERE usuarios.id NOT IN (SELECT usuario_id FROM pedidos)

```







## Doble Join:
Los Joins dobles van sin comas, y siguiendo la estructura del join.

```sql
SELECT usuarios.nombre, productos.precio * pedidos.cantidad FROM usuarios 

INNER JOIN pedidos ON usuarios.id = pedidos.id
INNER JOIN productos ON	pedidos.producto_id = productos.id;
```





