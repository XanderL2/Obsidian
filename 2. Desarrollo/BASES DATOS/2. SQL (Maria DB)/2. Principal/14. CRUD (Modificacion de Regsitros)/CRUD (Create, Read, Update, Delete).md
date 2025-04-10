
---
## ¿Que es el CRUD?

![[Pasted image 20240201183325.png]]

**CREATE (Insert):**
Se refiere a la acción de agregar registros a la BD, Estos se hacen con la funcion Insert.

**READ (Select):**
Significa la acción de consultar o ver los datos de una base datos.

**UPDATE:**
Se refiere a la accion de editar los datos de la base de datos.

**DELETE:**
Es la accion de eliminar datos de una base de datos.

## Insert (Create):

- El Insert se hace para crear nuevos registros dentro de la entidad, en el CRUD hace referencia a CREATE.

```sql
INSERT INTO nombreEntidad (Campo1, Campo2, Campo3)
VALUES (Valor1, Valor2, Valor3),
		(Valor1, Valor2, Valor3),
		(Valor1, Valor2, Valor3);


//Estamos creando registros dando valor a cada campo
INSERT INTO Alumnos (Nombre, Apellido, Edad)
VALUES ("Paquito", "Mercedes", 23),
		("Luis", "Baza", 30),
		("Rodrigo", "Jimenez", 20);

```

## Select (Read):

- El comando "SELECT" en SQL es como pedirle a una base de datos que te muestre información específica que está guardada en ella. En el CRUD seria “Read”, que es la acción de consultar o ver los datos de una entidad o base de datos.

```sql
SELECT * FROM nombreEntidad;

//Ejemplo:
SELECT * FROM Alumnos;
//Le estamos diciendo, dejame ver todo lo que hay en la entidad Alumnos

//Tambien podemos decirle que nos muestre solo algunos campos de la entidad 
//de la siguiente manera:

SELECT campo1, campo FROM nombreEntidad;
```


## Delete:

- Sirve para borrar todos los registros de todos los campos.
    
```sql
/*Borrar algo en concreto*/

	DELETE FROM empleados WHERE id = 1;

/*Le estamos diciendo, BORRA todo lo que hay en la entidad Alumnos*/
    DELETE * FROM Alumnos;
    
/*Tambien podemos decirle que BORRE solo algunos campos de la entidad 
de la siguiente manera:*/
    
	SELECT campo1, campo2 FROM nombreEntidad;
```
    
- Para borrar solo un registro usaremos un where y algo que caracterice al registro que queremos borrar, lo mas recomendable es por ID.
    
```sql
DELETE FROM Alumnos //Le estamos diciendo que borre alumnos de la entidad
WHERE ID = 4;  //Pero que solo borre el que tiene el ID 4
```


## Update:

Sirve para actualizar datos, usamos la clausula UPDATE, en ayuda del SET, este nos pide el campo y el valor, si queremos actualizar mas datos tambien lo podemos hacer. Y con el Where simplemente le decimos a que valor queremos que se aplique, esto lo hacemos con una condicion.

```sql

UPDATE nombreEntidad SET valor = "nuevo_valor" WHERE ID = 1;

#Ejemplo: Cambiando el nombre de un registro

UPDATE Alumnos SET Nombre = "Christian" WHERE ID = 3;

```

