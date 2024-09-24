
---
## ¿Que es una Transaccion?
Es una operacion que modifica valores en una BD, osea que puede ser desde un UPDATE, un ALTER TABLE, o cualquier otra cosa que modifique algo en una BD. 
Una transaccion hace referencia a que la operacion se debe realizar completamente o no se ejecuta en absoluto. Por ejemplo:

Imagina que deseas transferir dinero de una cuenta a otra. La transacción debe ser atómica, lo que significa que ocurrirá de manera completa o no ocurrirá en absoluto. Y si alguna parte de la transacción falla (por ejemplo, debido a un error de conexión o cualquier otro problema), ambas partes se deshacen automáticamente, y tu dinero no se perderá ni se quedará en un estado intermedio. Esto asegura que tu cuenta este en buen estado.

## ¿Para que sirven?:

- **Atomicidad:**
	 Significa que no deben haber puntos medios, osea que se hace el proceso o no se hace en lo absoluto. 
	 
- **Consistencia:**
	 Es practicamente verificar el estado de la BD despues de haber hecho un cambio en la Base de Datos (Transaccion), si es que los cambios estan bien hechos podemos confirmar los cambios con un "COMMIT", caso contrario la operacion ha perjudicado a la BD, haremos un "ROLLBACK" para tirar atras los cambios. 
- **Aislamiento:**
	 Esta propiedad dice que el comportamiento de una transaccion no se ve afectada por el comportamiento de otra. 


## Tipos de Transacciones: 
- **Transaccion Simple:**
	 Es aquella que si existe un problema a la mitad de la transaccion esta se borra dejando sus cambios estado anterior, es decir no se efectua. 
	![[Pasted image 20240218103312.png]] 
	
## Codigo: 

1. **Iniciar la Transaccion:** 
	 Para iniciar la transaccion usamos la clausula "BEGIN TRANSACTION", haciendo referencia a que iniciaremos una transaccion. 
	 
```sql
BEGIN 
```

2. **Realizar la Transaccion (Modificacion en la BD):**
	 Aqui ya realizaremos la transaccion, normalmente el paso 1 y 2 se hacen al mismo tiempo :
```sql
UPDATE Alumno SET Nombre = "pipe" WHERE ID = 3;
```

3. **Revisar los cambios en la BD con un SELECT:**
	 Revisaremos los cambios con un SELECT hacia la tabla o tablas que modificamos.
```sql
SELECT * FROM nombre_tabla;
```

4. **Commit o Rollback:**
	 Confirmamos o Deshacemos los cambios de una transaccion segun si ha perjudicado o ha salido bien el cambio en la BD.

```sql
-- Si ha salido bien usamos un COMMIT
COMMIT;

-- Si queremos revertir los cambios usamos un ROLLBACK
ROLLBACK;
```



















