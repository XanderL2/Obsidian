
---
## ¿Que hacer en caso una maquina tenga abierto puertos web pero no cargue bien la pagina?

**En estos casos debemos modificar el archivo /etc/hosts:**

- */etc/hots*: Contiene informacion sobre los DNS del sistema, se utiliza para actuar de DNS de manera local. 


**Para ello deberemos poner en el archivo /etc/hosts/ :**

```txt

# The following lines are desirable for IPv6 capable hosts
::1     localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters

# Aqui debemos poner:

<ip>    nombreDominio
```


Escanear todas las redes:
```
airodump-ng --band a wlan0mon
```

