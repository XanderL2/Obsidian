
---
## ¿Que es una Clase?
Es una especie de estructura que se usa como plantilla para crear instancion de objetos.

## ¿Que es un constructor?
En terminos simples es una funcion que su principal trabajo es servir como metodos de entrada de datos al la clase, ademas cuando es instanciada requerira que los parametros para poder ser creada. El self se usaria para hacer referencia al objeto, osea con el self estariamos definiendo un atributo y lo estariamos igualando a lo recibido por los parametros,

```python
class nombreClase:
    #Ni bien creamos el objeto el metodo constructor se ejecuta.
	
    def __init__(self, atributo1, atributo2):
		#Con el self estamos haciendo referencia a la clase. 
		
        self.atributo1 = atributo1;
        self.atributo2 = atributo2;
		
```

## Creacion de Clases:
- *Self* hace referencia a la instancia de la propia clase.

```python
#Creamos la clase

class Rectangulo:

    #Ni bien creamos el objeto el metodo constructor se ejecuta.
	
    def __init__(self, ancho, alto):
        self.ancho = ancho;
        self.alto = alto;
    
    # Los metodos deberan llevar si o si la palabra reservada Self
    
    def areaRectangulo(self):
        area = self.ancho * self.alto;
        return area;
		
    def multiplicarAncho(self, numero):
        ancho = self.ancho * numero;
        return ancho;


#Instancia de la clase:
rectangulo1 = Rectangulo(20,5);


print(f'Area: {rectangulo1.areaRectangulo()}')
print(f"Ancho: {rectangulo1.multiplicarAncho(10)}")


```


