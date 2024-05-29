
---
## Funciones de Agregacion:

- **¿Que son?**
    
    Son funciones que trae internamente de manera predeterminada SQL, Estas otorgan funcionalidades interesantes como calcular la suma de todos los registros, hallar el promedio de los registros, hacer calculos estadisticos, Etc.
    
- ¿**Cuales son las mas comunes?**
    
    - Matematicas:
        
        1. **COUNT():**
            
            - **`COUNT()`** Cuenta el número de filas o el número de valores no nulos en una columna.
            
            ```sql
		SELECT COUNT(*) AS total_registros FROM tabla;
            ```
            
        2. **SUM():**
            
            - **`SUM()`** Se utiliza para sumar los valores de una columna.
            
            ```sql
            SELECT SUM(columna) AS suma_total FROM tabla;
            ```
            
        3. **AVG():**
            
            - **`AVG()`** Calcula el promedio de los valores en una columna.
            
            ```sql
            SELECT AVG(columna) AS promedio FROM tabla;
            ```
            
        4. **ROUND():**
            
            - **`ROUND()`** Redondea un número al número entero más cercano o al número especificado de decimales.
            
            ```sql
            SELECT ROUND(columna, 2) AS redondeado FROM tabla;
            
            ---Esto redondearía los valores en la columna a 2 decimales.
            ```
            
        5. **MIN():**
            
            - **`MIN()`** Devuelve el valor mínimo en una columna.
            
            ```sql
            SELECT MIN(columna) AS valor_minimo FROM tabla;
            ```
            
        6. **MAX():**
            
            - **`MAX()`** devuelve el valor máximo en una columna.
            
            ```sql
            SELECT MAX(columna) AS valor_maximo FROM tabla;
            ```
            
        7. **Mod():**
            
            - **`Mod()`** Saca el modulo:
            
    - De Cadenas de Caracteres:
        
        1. **CONCAT():**
            - **`CONCAT()`** se utiliza para concatenar dos o más cadenas de caracteres.
        
        ```sql
        SELECT CONCAT(cadena1, cadena2) AS concatenado FROM tabla;
        ```
        
        1. **SUBSTRING():**
            
            - **`SUBSTRING()`** devuelve una parte de la cadena.
            
            ```sql
        SELECT SUBSTRING(cadena FROM 1 FOR 3) AS subcadena FROM tabla;
            ```
            
            Esto devolvería los primeros 3 caracteres de la cadena.
            
        2. **LENGTH() o LEN():**
            
            - **`LENGTH()`**  devuelve la longitud de la cadena.
            
            ```sql
            SELECT LENGTH(cadena) AS longitud FROM tabla;
            ```
            
        3. **UPPER():**
            
            - **`UPPER()`** convierte una cadena a mayúsculas.
            
            ```sql
            SELECT UPPER(cadena) AS en_mayusculas FROM tabla;
            ```
            
        4. **LOWER():**
            
            - **`LOWER()`** convierte una cadena a minúsculas.
            
            ```sql
            SELECT LOWER(cadena) AS en_minusculas FROM tabla;
            ```
            
        5. **TRIM():**
            
            - **`TRIM()`** elimina espacios en blanco al principio y al final de una cadena.
            
            ```sql
            SELECT TRIM(cadena) AS sin_espacios FROM tabla;
            ```

- **¿Como las usamos?**
    
    Las funciones de agregación en SQL, como SUM (suma), COUNT (conteo), AVG (promedio), MAX (máximo) y MIN (mínimo), se utilizan principalmente en la cláusula SELECT. Estas funciones realizan cálculos en grupos de datos de una columna y proporcionan un único valor resultante basado en esos datos.
    
    ```sql
    SELECT SUM(precio) AS suma_total FROM PRODUCTO;
    ```

## Comentarios:

```sql
--HOLA! SOY UN COMENTARIO
```




