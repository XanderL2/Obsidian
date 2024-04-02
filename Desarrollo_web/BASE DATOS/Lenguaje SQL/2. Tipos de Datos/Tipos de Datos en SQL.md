
---
## Importancia de los Tipos de Datos:

Es de gran importancia que los tipos de datos sean los adecuados segun eñ tamaño del dato a guardar, ya que asi aligeramos las consultas por tanto creamos una base de datos con un rendimiento superior.

## Tipos de Datos:

- **Cadena de Caraceteres:**
    
    Son campos que creados especificamente con el objetivo de aceptar solo un tipo de dato. Los mas usados son Varchar, Char y text,
    
    - CHAR:
        
        -Es de longitud Fija.
        -Ocupa el espacio justo de longitud especificado.
        -Se suele usar mas para datos que tienen una longitud especificada constante. Ademas si algun registro se guarda y supera la longitud esta se recortara.
		
	```sql
CREATE TABLE usuario(
    ID INT,
    Nombre CHAR(30) //Entre los parentesis va la logitud  especificada. 
);
```

	- VARCHAR:
        
		-Adecua su longitud a la palabra.
        
        -Ocupa el almacenamiento necesario solo para la palabra ingresada.
        
        -Es adecuado usarlo cuando hay palabras de longitud variable, como nombres.
        
        -Adecua su longitud dentro del limite que lo pongamos entre los parentesis.
		
        ```sql
CREATE TABLE usuario (
    id INT,
    nombre VARCHAR(255)
);
        ```
		
    - TEXT:
        
        -Almacena grandes cantidades de texto.
        
        -Adecua su longitud segun lo ingresado.
        
        ```sql
CREATE TABLE usuario (
    id INT,
    descripcion TEXT
);
```
        
    - BINARY:
        
        -Almacena datos en lenguaje binario.
        
        -Su longitud maxima es de 255.
        
        -El hecho de que los datos se almacenen en binario hace que sean adecuados para almacenar información codificada.
        
        ```sql
CREATE TABLE usuario (
    id INT,
    binario_data BINARY(255)
);
```
        
    - VARBINARY
        
        -Almacena datos en lenguaje binario.
        
        -Adecua su longitud a lo ingresado.
        
        -Util para almacenar valores que varian su longitud, como imagenes, archivos, Etc.
        
        ```sql
CREATE TABLE usuario (
    id INT,
    binario_data VARBINARY(255)
);
```
        
    - BLOB:
        
        -Utilizado mayormente para almacenar grandes volumenes de datos binarios.
        
        -Estos datos pueden ser imagenes, videos, Etc.
        
        -Los datos son manejados como objetos, lo que permite recuperar grandes cantidades de datos.
        
        ```sql
CREATE TABLE ejemplo (
    id INT,
    blob_data BLOB
);
```
        
    - ENUM:
        
        -Crea un conjunto de opciones predefinidas.
        
        -Se utiliza para representar opciones fijas.
        
        -Tiene que considerarse que las opciones seran fijas y nunca seran cambiadas, esto con el fin de crear una mejor organizacion.
        
        ```sql
CREATE TABLE ejemplo (
    id INT,
    estado ENUM('Muy Bueno', 'Bueno', 'Malo')
);
```
        
    - SET:
        
        El set es un conjunto de valores entre los que se permite elegir, algo asi como un input de seleccion en HTML. Dentro de esta opcion solo se puede elegir uno, Ejemplo:
		
```sql
CREATE TABLE preferencias (
    id INT,
    frutas_preferidas SET('Manzana', 'Plátano', 'Naranja', 'Uva')
);
```

- **Numericos:**
    
    - Enteros:
        
        Tipo de dato Entero|Rango de valores con Signo|Rango de Valores sin signo|Espacio en memoria|
        |---|---|---|---|
        |TINY INT|-128 a 127|255|1 Byte|
        |SMALL INT|-32,768 a 32,767|65,535|2 Bytes|
        |MEDIUM INT|-8,388,608 a 8,388,607|16,777,215|3 Bytes|
        |INT|-2,147,483,648 a 2,147,483,647|4,294,967,295|4 Bytes|
        |BIG INT|-9,223,372,036,854,775,808|18,446,744,073,709,551,615|8 Bytes|
        
        Ejemplo de Declaracion en codigo:
        
	```sql
CREATE TABLE ejemplo (
    Numeros INT, --Clave Primaria--
    ejemplo_tyny TINYINT --No llevan espacio-- 
    ejemplo_big_int BIGINT
);
```
        
    - Decimales:
        
        El mas usado es el Float:
        
	    ```sql
-- Ejemplo de declaración de FLOAT, REAL y DOUBLE PRECISION en una tabla
CREATE TABLE ejemplo_numerico (
	id INT,
    valor_float FLOAT,
    valor_real REAL,
    valor_double DOUBLE PRECISION
);
```
        
        - Float:
            
            -Te da valores no muy precisos, pero eficaces para numeros que no requieren precision extrema:
            
            -Pesa 4 bytes.
            
        - Real
            
            -Muy parecido al float, no tiene diferencias perceptibles:
            
            -Pesa 4bytes
            
        - Double Precision:
            
            -Da el dato mas preciso posible, muy poco usado por su alta precision y alto peso.
            
            -Pesa 8bytes.
            
    - Funciones Especiales de los tipos de datos numericos:
        
        Ejemplo:
        
        -Usamos el sin signo en el ID para decirle que no habran valores negativos.
        
        -Usamos el ZEROFILL para decirle que va a rellenar con ceros a la izquierda como en los IDS.
        
        -Y el autoincrement para decirle que autoincrementara:
		 ```sql
CREATE TABLE EjemploCompleto (
    id INT UNSIGNED ZEROFILL AUTO_INCREMENT,
    nombre VARCHAR(50),
    PRIMARY KEY (id)
);
```
        
        Manejo de Signos y Autoincremento: 
        - Unsigned (Sin signo):
            
            Nos permite manejar los valores sin signo, es decir numeros no negativos, por ende aumento su rango de valores.
            
        - ZeroFill (Agrega ceros)
            
            Agrega ceros a la izquierda que no modifican los numeros, pero se utilizan comúnmente en contextos donde se requiere una presentación uniforme de los datos, como números de identificación o códigos. Puede ser útil para mantener una longitud constante y mejorar la legibilidad de los datos.
            
        - Auto_Increment (Autoincremento)
            
            Autoincrementa por cada registro (Como pasa comunmente en los ids).
            
        
        Manejo de Decimales:
        
        - Decimal o Numeric:
            
            Tanto decimal como numeric se usan para lo mismo. En este caso el primer parametro de la funcion nos especifica la cantidad de digitos que tendra en total nuestro numero, mientras que el segundo nos dira la cantidad de decimales que tendra el numero.
            
```sql
CREATE TABLE EjemploDecimal (
    id INT,
    monto DECIMAL(10, 2) --Nos dice que monto tendra 10digitos, y que 2 de ellos sean decimalees. 
);
```

- **Datos de Tiempo (Fechas):**
    
    |TIPO DE DATO|¿QUE HACE?|
    |---|---|
    |DATE|ALMACENA FECHAS SIN INCLUIR HORA|
    |DATETIME|ALMACENA FECHA Y HORA|
    |TIMESTAMP|ALMACENA FECHA Y HORA ACTUALES|
    |TIME|SOLO PARA HORA|
    |YEAR|SOLO PARA AÑO|
    
    ```sql
    CREATE TABLE EjemploFechas (
        id INT,
        fecha DATE,
        fecha_hora DATETIME,
        marca_tiempo TIMESTAMP,
        hora TIME,
        año YEAR
    );
    ```
    
- **Otros tipos de datos:**
    
    - Booleano (BIT)
        
        Este tipo de dato almacena bits, pero es mas comun usarlo para representar valores booleanos, donde 1 es true y 0 false. Para que sea booleano limitaremos la longitud a 1, ya que solo de esta manera dara un 0 o un 1.
        
```sql
    CREATE TABLE EjemploBit (
        id INT,
        booleano BIT(1)
    );
    ```