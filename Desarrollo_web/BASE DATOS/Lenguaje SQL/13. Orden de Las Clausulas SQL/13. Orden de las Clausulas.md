
---
## Orden:
Para una buena consulta, sobre todo evitando datos erroneos o invalidos debemos tener muy en cuenta el orden en que ponemos las clausulas, estas suelen seguir el siguiente orden: 
1. **SELECT**: 
	 Primero se da la orden de recuperacion de datos con un select, especificando las columnas que queremos consultar:
```sql
	 SELECT columna1, columna2  
```
2. **FROM**: 
     Luego a esta se le complementa el uso de del FROM, en el cual indicaremos la tabla con de los datos que queremos recuperar.
```sql
     SELECT columna1, columna 2 FROM tabla_1	
```
3. **JOINS**: 
	 Luego siguen las consultas multitabla, para asi obtener los datos sobre los cuales operar correctamente.
```sql
	 SELECT columna1, columna2 FROM tabla1 INNER JOIN tabla2 ON tabla1.columna = tabla2. columna  
```
4. **WHERE**: 
	 Luego empezamos a operar con los datos, de tal manera que se filtren por la condicion antes de aplicar algun filtro: 
```sql
	 WHERE condicion
```
5. **GROUP BY**: 
	  Luego empezariamos a Agropar datos, esto con el objetivo de reducir los datos en caso requiramos
```sql
	  GROUP BY Campo1  
```
6. **HAVING**:
	 En este caso el HAVING se usa para filtrar los datos de una consulta GROUP By, esta es como un condicional, esto se hace para aplicar una condicion segun sea necesario.
```sql
	 GROUP BY campo1 HAVING CONDICION
```
7. **ORDER BY**: 
	 Finalmente estos resultados se ordenan, esto siempre va al final para obtener el resultado esperado.
```sql
	 ORDER BY COLUMNA BY ASC
```
