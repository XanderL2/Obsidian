
---
## SOLID:

- **SRP:** Una clase debe tener una razon, solo una razon para cambiar. Para aplicarla nos podemos preguntar:
	- **¿Qué hace esta clase? - Si hace más de una cosa, no cumple SRP.**
	<br>
- **OCP:** Una clase debe estar abierta para su extension pero cerrada para su modificacion.
	- **¿Puedo añadir mas funcionalidad sin necesidad de modificar el codigo?**
	 <br>
- **LSP:** Las clases hijas deben poder reemplazar a las clases padre, es decir la clase hija debe implementar todos sus metodos y atributos de la clase padre, esto agregado lo propio de la clase hija. En otras palabras:
	- **Las clases hijas deben implementar correctamente todos los atributos y metodos de su clase padre. Si existen metodos o atributos que no se pueden implementar, abstraer y crear otra interfaz o clase mas concreta.** 
	- **Ejemplo:** Tienes una clase `Animal` con un método `hacerSonido()`. Si creas una subclase `Pato` que sobreescribe `hacerSonido()` para hacer "cuac", y otra subclase `Pez` que hace "burbuja", pero `Pez` no puede realmente hacer sonidos, entonces el código que espera un `Animal` podría fallar o comportarse de manera inesperada.
	 <br>

- **ISP:** Las interfaces no deben depender de metodos que no utilizan y deben ser interfaces pequeñas y especificas, no grandes y genericas. Para aplicarla nos podemos preguntar:
	-  **¿Esta interfaz tiene los metodos que necesito?**
	  <br>
- **DIP:**  Es preferible depender de Interfaces o Clases abstractas. Por ejemplo: Si queremos en un metodo recibir un dato de un objeto en concreto, debemos pedir como parametro su clase base (abstracta), no el objeto concreto.

## Principios para cada Estructura:

- **Funciones:**
	- Deben ser de no mas de 20 lineas, y tener maximo 3 parametros.
	
	- Es preferible lanzar errores, ya que estos hacen mas verboso pero entendible el codigo, en vez de retornar falso o null en caso de errores.
	
	- Propaga errores que no puedas manejar adecuadamente dentro de la función hacia el nivel superior, esto en la siguiente prioridad: 
		1. Validar con `ifs` los errores  y lanza excepciones (Clausulas de Guarda).
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

