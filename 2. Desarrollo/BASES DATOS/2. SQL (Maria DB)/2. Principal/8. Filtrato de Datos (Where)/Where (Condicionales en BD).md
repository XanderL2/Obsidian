
---
## Condiciones (Where - Donde):

- **¿Para que sirve?**
    
    Sirven para filtrar datos segun una condicion, sirven como un IF sino que muestran los datos recibidos.
    
- **¿Como se hace un Where?**
    
    Deberemos usar la Clausula Where, y asignar una condicion. A su vez se pueden mezclar con todos los operadores para construir condiciones.
    
    Ejemplo 1:
    
    ```sql
//Le estamos diciendo que nos muestre todos los campos y registros de la entidad alumno
    SELECT * FROM Alumnos
	
//Le estamos diciendo que nos muestre solo los registros en los que edad sea menor a 20
    WHERE Edad < 20;
	
//Es decir le estamos diciendo que nos muestre a los alumnos que son menores a 20
```
    
    Ejemplo 2:
    
```sql
//Le estamos diciendo que nos muestre todos los campos y registros de la entidad alumno
    SELECT * FROM Alumnos
    
//Le estamos diciendo que nos muestre todos los registros que tengan como nombre "Luis"
	WHERE Nombre = "Luis";
    
//Le estamos aplicando una condicion para que nos filtre los precios menor a 10
    WHERE precio < 10
    
```