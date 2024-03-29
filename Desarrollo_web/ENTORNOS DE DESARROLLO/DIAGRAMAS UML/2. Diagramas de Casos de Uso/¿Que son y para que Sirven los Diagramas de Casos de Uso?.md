
---
## ¿Que son los Diagramas de Casos de Uso?
Son diagramas que utilizamos para entender como los usuarios interactuan con el sistema, de esta manera ayudandonos a ver que funcionalidades necesitan para el correcto uso de la aplicacion. 

## Preguntas Clave para el Desarrollo de Diagramas de Casos de Uso :

- **¿Quienes van a Interactuar con la Aplicacion? (Se obtienen los Actores)
- **¿Cuales seran sus Principales Funciones? (Se obtiene el Proceso)


## Componentes:

![[Pasted image 20240329134428.png]]o

- **Actores:**
	 Son roles de entidades que interactuan con el sistema, normalmente son usuario, administrador y otro sistemas. Los actores que son personas se suelen representar con un muñeco, mientras que los sistemas son representados con un cuadrado
	 
- **Sistema Principal:**
	 Es representado con un contenedor grande dentro del cual iran las funcionalidades representadas con un ovalo.
	 
- **Casos de Uso:**
	 Son representados con un ovalo dentro del sistema principal.
	 
- **Relaciones:**
	 - **Relaciones comunes:**
		 Son relaciones entre Usuario y Caso de Uso.
	 - **Relaciones Extend:**
		 Representan algo opcional para el usuario. Por ejemplo, en un hotel el usuario tiene la opcion de aplazar su tiempo de estadía.
		 
	 - **Relaciones Include:**
		  Es aquella funcionalidad se debe hacer de manera obligatoria para que el usuario pueda acceder a sus opciones, por ejemplo, en una red social para poder postear un comentario debemos habernos pasado por el login.

## Ejemplo:

- **¿Quienes van a Interactuar con la Aplicacion? (Se obtienen los Actores)**
	 El usuario final y otros sistemas.
	 
- **¿Cuales seran sus Principales Funciones? (Se obtiene el Proceso)**
	 El usuario podra:
		 -  Ver menu.
		 -  Ver el tiempo estimado del pedido
		

![[Pasted image 20240329135011.png]]


