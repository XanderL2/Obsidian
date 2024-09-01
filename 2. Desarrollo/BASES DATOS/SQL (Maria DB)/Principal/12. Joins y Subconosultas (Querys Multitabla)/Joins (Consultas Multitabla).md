
---
## ¿Que son y para que sirven?

- **¿Para que sirven?**
    
    Sirve para fusionar tablas, es decir combinar los campos entre tablas. 
    
    Por ejemplo, si tenemos una tabla de clientes y una tabla de pedidos, podemos usar un join para obtener una lista de todos los clientes que han realizado un pedido y de esta manera combinar ambas tablas.
- **Aspectos importantes a tener en cuenta:**
    - Los joins no te dan la columna directamente con la salida por consola, sino que lo especificas en el Select, simplemente los joins te dan la entrada de esos valores.
    - Los campos ambiguos, es decir campos que existen con el mismo nombre en ambas tablas deben especificarse. Por ejemplo, si tenemos 2 tablas y cada una tiene un campo llamado “nombre” en el select deberemos especificar a que tabla pertenece de la siguiente manera: tabla.nombre.
    - El where va despues del JOIN

## Tipos de JOINS:

- **Inner Join (Datos coincidentes):**
    
    Nos devuelven la relacion que existe las filas de 2 tablas, por ejemplo, si tenemos 2 tablas relacionadas mediante clave foranea esta nos devolvera los registros que esten relacionados mediante esta clave. Ademas buscara coincidencias, es decir registros iguales entre tablas.
	![[Pasted image 20240201185410.png]]
```sql
LA CONSULTA SE HACE DESDE LA TABLA QUE TIENE LA MAYORIA DE DATOS RELEVANTES

SELECT columnas
FROM tabla1
INNER JOIN tabla2 ON tabla1.columna = tabla2.columna;
```

- **Left Join (Datos de la tabla Izquierda):**
    
    Nos devuelve todos los datos de la tabla izquierda mas la interseccion de ambas tablas.
	 ![[Pasted image 20240201191237.png]]

```sql
//En este caso la tabla uno es la principal, osea la de la izquierda

SELECT columnas
FROM tabla1
					#Tabla Izquierda  Tabla derecha
LEFT JOIN tabla2 ON tabla1.columna = tabla2.columna;
```

- **Right Outer Join (Datos Tabla Derecha):**
    Devuelve todos los datos de la tabla derecha mas la interseccion entre ambas.
	 ![[Pasted image 20240201192008.png]]
```sql
	--La consulta se hace desde la tabla que tiene mas datos relevantes
	SELECT columnas
		FROM tabla1
	RIGHT JOIN tabla2 ON tabla1.columna = tabla2.columna;

```

- **Full Outer Join (Junta Datos de ambas Tablas):**
    
    En MySQL no tenemos como tal una sintaxis para el full join, sin embargo podemos emularlo con la clausula “UNION” la cual unira consultas, entonces simplemente deberiamos unir una consulta de un LEFT JOIN mas un RIGHT JOIN.
	 ![[Pasted image 20240201192152.png]]
	 
- **Join a la misma tabla o Join iterativo:**
    
    Para hacer un Join recursivo o iterativo debemos tener en cuenta que deben existen 2 claves relacionadas en la misma tabla, o interrelacion recursiva.
    
    ```sql
    #Con t1 y t2 simplemente le otorgamos un alias simulando haber 2 tablas
    #
    
    SELECT t1.columna AS columna_tabla1, t2.columna AS columna_tabla2
    FROM tu_tabla t1
    
    INNER JOIN tu_tabla t2 ON t1.columna_relacionada = t2.columna_relacionada;
    ```











