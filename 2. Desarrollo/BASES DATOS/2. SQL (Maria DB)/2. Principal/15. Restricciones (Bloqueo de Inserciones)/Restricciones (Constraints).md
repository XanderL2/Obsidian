
---
## ¿Que son las Restricciones?
Son validaciones que se hacen para proteger la integridad de los registros, es decir, nos aseguramos que los datos ingresados sean validos. Por ejemplo, si queremos asegurarnos que en un campo DNI todos los valores sean unicos, podriamos usar un UNIQUE.
## Tipos de Restricciones:

- **UNIQUE (Valores unicos)**:
	 Sirve para especificar que todos los registros dentro de un campo seran unicos. Por ejemplo, si queremos almacenar DNIS del usuario podriamos usar esta restriccion para ver que todos los valores seran unicos y no habra otro repetido.  
	 
	 Esta validacion se suele hacer al momento de crear la tabla, sin embargo tambien podriamos hacerla al modificar una tabla, pero no es tan recomendable y es mejor planificar bien las cosas. Ademas, podemos darle un nombre a estas restricciones, para que cuando salte el error este nombre se vea en la pantalla.
	 
```sql
	
	--AL CREAR UNA TABLA
	 CREATE TABLE nombre_tabla(
		 columna1 TIPO_DATO,
		 columna2 TIPO_DATO, 

		 CONSTRAINT nombre_restriccion UNIQUE(columna1)
	 );

	 
	--MODIFICANDO TABLA
	ALTER TABLE nombre_tabla
	ADD CONSTRAINT nombre_restriccion UNIQUE (nombre_columna);
```

- **Check (Segun una Condicion)**:
	Sirven para poner una condicion y validar los datos que se van a guardar, por ejemplo, si estamos haciendo la BD de un banco tendriamos que validar este dato, ya que el prestamo no podria ser menor o igual a cero. Esto se veria asi.

```sql
	-- Si estamos creando una tabla:
	CREATE TABLE (
		nombre_cliente TIPO_DATO,
		prestamo  TIPO_DATO,     
		--Estamos validando que lo valores sean mayor a 0
		CONSTRAINT valor_menor_a_0 CHECK (prestamo >= 0)	
	);
	
	-- Si estamos editando una tabla:
	 ALTER TABLE
		 --Validamos que no se puedan hacer prestamos menores a 0
	 ADD CONSTRAINT valor_menor_a_0 CHECK (prestamo > 0);
```

- **NOT NULL (No registros Nulos)**:
	 Es la restriccion que aplicamos para cuando queremos que los registros sean obligatorios, osea no sean nulos. 

```sql
	--Cuando creemos una tabla
	 CREATE TABLE nombre_tabla(
		  nombre_columna TIPO_DATO NOT NULL;
	 
	 );

	
	--Cuando editemos una tabla
	ALTER TABLE nombre_tabla
	MODIFY nombre_columna TIPO_DATO NOT NULL; 
```

- **DEFAULT (Valores por defecto)**:
	 Es para añadirle un valor por defecto a los registros, haciendo que tengan un valor por defecto. Por ejemplo: 
```sql
	-- Al crear una tabla
	 CREATE TABLE nombre_tabla(
		 nombre_columna TIPO_DATO DEFAULT valor_defecto
		 
	 );
	-- Al modificar una tabla

	 ALTER TABLE nombre_tabla(
		 ALTER COLUMN nombre_columna SET DEFAULT valor_por_defecto
	 );

```
	 

Link Explicativo: https://www.youtube.com/watch?v=lMtdN5mMXK0













