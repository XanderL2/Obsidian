
---
## Clausula AS (COMO):

- **¿Que es?**
    
    El AS o “Como” en español, es una propiedad del Select que sirve para crear un nuevo campo con un Nombre nuevo o simplemente para cambiar de nombre a un campo. Es importante saber que este campo solo se mostrara y podremos operar con el en la misma consulta.
    
- **¿Como se hace?**
    
    Para hacer esto tenemos que hacer un Select, y escribir al lado el nombre del campo que queremos cambiar de manera temporal, seguido de un AS y el nombre nuevo que le queremos dar al campo, despues un FROM y el nombre de la entidad al que pertenece ese campo.
    
```sql
    SELECT Nombre AS PrimerNombre FROM Alumnos;
    
//Le estamos diciendo, muestrame el campos"Nombre" como si se llamaraa "PrimerNombre" de la tabla Alumnnos 
    
//Le estamos diciendo que multiplicaremos el precio por 2 y que en la consulta Muestre un campo que se llame precios_por_2
    
    SELECT PRECIO * 2 AS Precios_por_2 FROM NOMBRETABLA
    ```
    