
---
## ¿Que son los Sniffers?
Son herramientas que capturan el trafico TCP de una red, esta sirve para poder visualizar lo compartido por otras personas en la red en protocolos que no viajen cifrados. Estos protocolos que no viajan cifrado suelen: 

- HTTP - 80 (Protocolo Web sin capa de cifrado).
- SMTP  - 25 (Protocolo de Correos).
- Telnet - 23 (Parecido al protocolo SSH sino que sin cifrar).
- POP3 - 110 (Recuperacion de mensajes de correo electronico).
- IMAP - 143 (Recuperacion y transimision de mensajes de correos electronicos).

## ¿Como usamos Wireshark?
Al abrir Wireshark nos mostrara la serie de adaptadores inalambricos que tenemos en el equipo, deberemos usar el adaptador de red que queramos. 

![[Pasted image 20240220172223.png]]

**Pantalla Principal de Wireshark:**

![[Pasted image 20240220173145.png]]
- **No (Numero):** Hace referencia al numero de paquete capturado.
- **Source:** Es el origen, es decir quien emite ese paqeute
- **Destination:** Es quien recibe el paquete TCP 
- **Protocol:** Es el protocolo por el cual ha sido enviado el paquete.
- **Source:** Es el origen, es decir quien emite ese paqeute
## Filtrado de Paquetes TCP:

- **Filtrado por Protocolo:**
	 Simplemente es poner el nombre del Protocolo de Red en la opcion de busqueda de Wireshark. Ejemeplo:
	 
	 ![[Pasted image 20240220175317.png]]
	 
- **Filtrado por Puertos:**
	 Para hacer a los puertos usaremos la palabra reservada "tcp.port", seguido de operadores logicos, como el &&, ||, !, etc. De esta manera filtraremos los paquetes dados por cierto puerto.
	 
	 ![[Pasted image 20240220175626.png]]
	 Tambien podemos jugar con los prefijos "src" y "dst" para filtrar por puerto de origen y destino.
	 ![[Pasted image 20240220175757.png]]
	 
- **Filtrado por IP:**
	 Podemos filtrar mediante IP con la palabra reservada "ip.addr", esta hara referencia a la IP por la cual queremos buscar.
	 ![[Pasted image 20240220180227.png]]
	
	 Nuevamente combinar esto con operadores logicos para hacer referencia a  puertos, protocolos, etc. Ejemplo:
	![[Pasted image 20240220180444.png]] 




