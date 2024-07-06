
---
## SOLID:

- **SRP:** Una clase debe tener una razon, solo una razon para cambiar
- **OCP:** Una clase debe estar abierta para su extension pero cerrada para su modificacion.
- **LSP:** Nuestras clases derivadas deben conservar el comportamiento de las superclases solo extendiendo su funcionalidad.
- **ISP:** Las interfaces no deben depender de metodos que no utilizan y deben ser interfaces pequeñas y especificas, no grandes y genericas. 
- **DIP:**  Es preferible depender de Interfaces o Clases abstractas. Por ejemplo: Si queremos en un metodo recibir un dato de un objeto en concreto, debemos pedir como parametro su clase base (abstracta), no el objeto concreto.

## Principios para cada Estructura:

- **Funciones:**
	- Deben ser de no mas de 20 lineas, y tener maximo 3 parametros.
	
	- Es preferible lanzar errores, ya que estos hacen mas verboso pero entendible el codigo, en vez de retornar falso o null en caso de errores.
	
	- Propaga errores que no puedas manejar adecuadamente dentro de la función hacia el nivel superior, esto en la siguiente prioridad: 
		1. Validar con `ifs` los errores (Clausulas de Guarda).
		2. Usar un `try - catch` pero con  un mensaje mas informativo (Solo si no agranda la funcion)
		3. Simplemente no usar un `try-catch` dentro de la funcion.
	
	- Si un error puede ser tratado de forma sencilla dentro de la funcion y sin ocupar muchas lineas podemos controlarlo directamente dentro de ella.
		```csharp
		public void processInput(String input) {
		    try {
		        validateInput(input);
		        // Procesar la entrada
		    } catch (InvalidInputException e) {
		        System.out.println("Entrada inválida: " + e.getMessage());
		        // Corrige la entrada o toma una acción correctiva
		        input = "default";
		        // Procesar la entrada corregida
		    }
		}
	
		```

- **Manejo de Errores:**
	- El manejo de errores debe ir de mas especifico a mas general, es mala practica hacerlo de forma solo general
		```csharp
		try {
		    // Código que puede lanzar varias excepciones
		} catch (FileNotFoundException e) {
		    System.out.println("Archivo no encontrado: " + e.getMessage());

		} catch (IOException e) {
		    System.out.println("Error de entrada/salida: " + e.getMessage());
	
		} catch (Exception e) {   //La del final debe ser mas general
		    System.out.println("Ocurrió un error: " + e.getMessage());
		}
		```

	- Utiliza el bloque `finally` para asegurar que se liberen los recursos, como cerrar el socket.









## Uso de Cammel Case:

| **Tipo Estructura**     | Notacion   | Ejemplo:                  |
| ----------------------- | ---------- | ------------------------- |
| *Atributos (Variables)* | camelCase  | booolean isActive = true; |
| *Clases*                | PascalCase | public class Alumno       |
| *Metodos*               | camelCase  | public int suma           |
| *Constantes*            | UPPERCASE  | final int NUMERO;         |

## Orden de Estructura de las Clases:

1. **Constantes**
2. **Atributos**
3. **Constructores**
4. **Metodos**
5. **Getters y Setters**
