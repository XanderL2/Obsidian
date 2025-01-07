	
---


- **Object Keys"**
	- Nos devuelve una lista con las claves de los objetos, por lo que al hacer el .leght podemos saber la la cantidad de claves que tiene y si tiene claves o no.

	```js
	Object.Keys(object) 
	Object.Keys(object).lemght
	```


- **Object Evento Input"**
	- Se ejecuta cada que el valor de un input cambia en tiempo en tiempo real.
	- La diferencia con el change es que el change se ejecuta una vez que ya se ha terminado de escribir en el input














---

- **Recursividad"**
	
	```js
	let json2 = `{
	    "Aves": {
	        "voladoras": {},
	        "no voladoras": {}
	    },
	    "Peces": {},
	    "Mamiferos": {
	        "ungulados": {},
	        "paquidermos": {}
	    }
	}`;
	
	
	let object =  JSON.parse(json2);
	
	
	
	function createList(object) {
	
	    const ulElement = document.createElement("ul");
	    
	    for (let key in object) {
	        let liElement = document.createElement("li"); 
	        liElement.innerText = key;
	        liElement.id = key;
	
	        ulElement.append(liElement); 
	
	        if(!(Object.keys(object[key]).length <= 0)){
	            liElement.append(createList(object[key]));
	        }
	        
	    }
	   
	    return ulElement;
	}
	
	
	
	document.getElementById("divContainer").append(createList(object));
	```
