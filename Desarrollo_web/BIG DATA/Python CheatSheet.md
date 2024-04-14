
---
## Metodos de cadenas

- **Split (Separar una cadena por un caracter y convertirlo en una lista):**

     candena.split('-')

- **Len (Longitud de cadena):**
    
    len(cadena)

- **Find (Buscar algo dentro de una cadena):**
    
    Si esta devolvera su posicion, sino devuelve -1.

    cadena.find("elementoABuscar")



## Metodos de Listas:

- **Max / Min (Maximo y minimo valor de la lista):**

    max(lista)

    min(lista)


- **Sorted:**

    sorted(lista) # Ordena valores de forma ascendiente
    
    sorted(lista, reverse = true) # Ordena valores de forma descendiente 

- **Eliminar valores (Posicion / Valor):**

    Valor:
        
        lista.remove(valor)


    Posicion:

        lista.pop(posicion)

- **Insertar valores (Al final / indice ):**

    Valor:
        
        lista.append(valor)


    Posicion:

        lista.insert(posicion, valor)


- **Sumar valores sum():**

    sum(nombrelista)

## Metodos de Diccionarios:

- **Get (Obtener valores):**

    diccionario.get("clave")

- **Items (Devuelve un par clave valor):**

    for clave, valor in diccionario.items():
    
    print({clave}: {valor})

- **Enumerate():**

    Le pone un iterador a cada par ordenado por el items


- **Agregar nueva clave al Diccionario:**

    grupo.update({"nuevaClave" : "valor"})


- **Values:**

    list(dictionary.values()) <--- devuelve una lista con los valores



## Manejo de Archivos TXT

- **Permisos:**
    

    - r = read
    - w = write
    - a = append
    - r+ = Lectura y escritura


- **Leer un archivo:**

    archivo.readlines()  <---- Devuelve una lista con las lineas, incluyendo los espacios


    archivo.read()  <--- devuekve un string grande, podemos usar el split


## Flask:

- Items (Diccionarios)
- Range ()
- Normal()
- El len se hace de la siguiente manera:
    - {% for i in range(0, lista|length) %}

- Acceder a atributos de diccionarios en Jinja:

    - diccionario["clave"]


- En un form la funcion se pasa en el action con 2 llaves {{}}
-
















