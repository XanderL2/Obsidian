
---
## Clausula Limit (Limitar Registros):

- **¿Para que sirve?**
    
    Es una clausula que sirve para limitar los resultados que queremos recibir, ya que aveces al hacer una consulta podemos visualizar grandes cantidades de datos, entonces con el limit no aplicamos tanta carga y limitamos a cierta cantidad de resultados.
    
- **¿Como se hace?**
    
    Para hacer esto tenemos que hacer un Select, y escribir al lado el nombre del campo que queremos cambiar de manera temporal, seguido de un AS y el nombre nuevo que le queremos dar al campo, despues un FROM y el nombre de la entidad al que pertenece ese campo.
    
    ```sql
    SELECT * FROM Productos
    ORDER BY Precio ASC
    LIMIT 5;
    ```
    
    - **`SELECT * FROM Productos`** selecciona todos los registros de la tabla "Productos".
    - **`ORDER BY Precio ASC`** ordena los resultados por la columna "Precio" en orden ascendente (del más barato al más caro).
    - **`LIMIT 5`** limita los resultados a solo los primeros 5 registros que cumplan con las condiciones especificadas en la consulta.
## Clausula Offset (Limitar Registros y omitir algunos):

- **¿Para que sirve?**
    
    Sirve para omitir una cantidad de filas, por ejemplo:
    
    Tenemos una lista de productos, pero solo queremos usar 5 de ellos, para eso usaremos la clausula limit. Luego nos damos cuenta que no queremos que salgan los 2 primeros resultados, es ahi donde usamos el offset, para omitir esas filas que no queremos que salgan con el limit.
    
    ```sql
    SELECT * FROM productos LIMIT 5 OFFSET 2;
    ```
## Clausula Distinct:

- **¿Para que sirve?**
    
    Sirve para asegurarnos de que cada valor sea unico, es decir para eliminar los valores duplicados en una consulta, se le aplica a todo.
    
    Ejemplo:
    
    Supongamos que tienes una tabla llamada **`empleados`** con una columna llamada **`departamento`**. Puedes usar **`DISTINCT`** para obtener una lista de departamentos únicos:
    
    ```sql
    SELECT DISTINCT departamento FROM empleados;
    ```
    
    Tabla sin Distinct:
    
    ```sql
    | id_empleado | nombre    | departamento |
    |-------------|-----------|--------------|
    | 1           | Empleado1 | Ventas       |
    | 2           | Empleado2 | Marketing    |
    | 3           | Empleado3 | Ventas       |
    | 4           | Empleado4 | Recursos     |
    | 5           | Empleado5 | Marketing    |
    ```
    
    Tabla con Distinct:
    
    ```sql
    | departamento |
    |--------------|
    | Ventas       |
    | Marketing    |
    | Recursos     |
    ```