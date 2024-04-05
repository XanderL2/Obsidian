
---
## ¿Que es el Testing?
Es el proceso en el que se evalua el software en distintos tipos de casos, todo con el objetivo de encontrar errores, defectos o deficiencias en el codigo. 

## ¿Para que Sirve el Testing? 

- **Asegurarse de que el software cumple con los requisitos funcionales y no funcionales** 
- **Identifica Errores y defectos antes de que lleguen a los usuarios finales** 
- **Mejora la calidad del Software, garantizando una mejor experiencia al usuario** 

## Error, Defecto y Problema

- **Error:** Equivocacion que se realiza durante el desarrollo, por ejemplo cuando sucede una excepcion.
- **Defecto:** Es lo que resulta al introducir un error de software.
- **Problema:** Representacion del defecto.
## ¿Para que Sirve el Testing? 

![[Pasted image 20240326162603.png]]

- **Pruebas Unitarias:**
	 Se centrar en probar fragmentos de codigo especificos que lleven a cabo una funcion en programa, con el objetivo de garantizar su funcion correcta.
	 
- **Pruebas de Integracion**
	 Las pruebas de integracion evaluan como interactua lo evaluado en las pruebas unitarias, garantizando asi la correcta ejecucion del programa.
	 - **Integracion No Incremental:**
		 Primero se prueba cada modulo por separado y luego se integra todo en una sola prueba
	 - **Integracion Incremental:**
		 Se van integrando progresivamente conforme se vayan probando unitariamente modulos 
		 
	 
- **Pruebas End to End;**
	 Evaluan todo el programa, desde el inicio hasta el final, tal y como lo haria un usuario. 

- **Pruebas de Aceptacion;**
	 Sirven para verificar si el software hace lo que el cliente espera, se llama asi porque se prueba si el cliente acepta el software como tal.
	 
- **Pruebas Funcionales;**
	 Son las pruebas que se hacen para ver si el softtware cumple con los requisitos funcionales y no funcionales estalecidos. Caja negra

## Formas de Clasificar los tipos de testing:

	
	![[Pasted image 20240326173003.png]]
	
- **Testing de Caja Negra:**
	 Son aquellos que se realizan solo en base a una entrada y salida, sin ver o saber lo que pasa por detras del programa. Aqui estarian los betatesters por ejemplo.
	 
- **Testing de Caja Blanca:**
	 Son aquellos que se realizan tomando en cuenta su estructura interna, aqui estarian las pruebas de integracion, las unitarias, etc.  
	 
- **Testing de Caja Gris:**
	 Son aquellos que son 50/50 de los anteriores, y se da cuando sabemos algo des cosas de caja blanca y en base a eso se hacen las pruebas.








Link Explicativo: https://www.youtube.com/watch?v=N-a5DEa_f0U 











