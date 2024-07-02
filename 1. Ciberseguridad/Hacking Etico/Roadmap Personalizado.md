
---
```markmap
# Temario de Ciberseguridad y Pentesting (Red Team)

## Temas Previos a Conocer
- **Criptografía**
  - Día 1: Conceptos básicos y criptografía simétrica
  - Día 2: Criptografía asimétrica y PKI
  - Día 3: Algoritmos comunes (AES, RSA, SHA)
  - **Proyecto:** Crear una herramienta en Python que implemente un sistema de autenticación de dos factores (2FA) utilizando HMAC (SHA-256) y cifrado de datos sensibles con AES.

- **Redes y Protocolos**
  - Día 4: Modelos OSI y TCP/IP
  - Día 5: Protocolos comunes (HTTP, HTTPS, FTP, DNS, SMB, RDP)
  - Día 6: Conceptos de routing y switching
  - Día 7: VPN y túneles seguros
  - **Proyecto:** Desarrollar un sniffer en Python que capture y analice tráfico de red para diferentes protocolos.

- **Sistemas Operativos**
  - Día 8: Linux: comandos básicos, administración, permisos
  - Día 9: Windows: administración, Active Directory, PowerShell
  - **Proyecto:** Crear un script en Python para automatizar tareas de administración en Linux y Windows (e.g., gestión de usuarios, permisos).

## Temario de Hacking a Sistemas y Web

### Semana 1: Fundamentos y Reconocimiento
- **Día 10: Introducción al Pentesting y Red Team**
  - Definición y objetivos
  - Fases del pentesting
  - Metodologías y estándares (PTES, OWASP)

- **Día 11-12: Reconocimiento Pasivo (OSINT)**
  - Uso de herramientas: Recon-ng, theHarvester, Maltego
  - Técnicas de búsqueda de información pública

- **Día 13-14: Fingerprinting y Reconocimiento Activo**
  - Nmap avanzado: escaneo de puertos, detección de servicios y sistemas operativos
  - Netcat para reconocimiento básico

- **Día 15: Enumeración de DNS y Subdominios**
  - Herramientas: Sublist3r, Amass, DNSenum
  - Técnicas de enumeración de DNS

- **Proyecto:** Desarrollar un script en Python que automatice el reconocimiento pasivo y activo utilizando Nmap, Recon-ng y Sublist3r.

### Semana 2: Escaneo y Enumeración de Servicios
- **Día 16-18: Enumeración de Servicios Comunes**
  - SMB enumeration: enum4linux, smbclient
  - SNMP enumeration: snmpwalk, onesixtyone
  - LDAP enumeration: ldapsearch

- **Día 19-21: Enumeración de Usuarios y Recursos**
  - Enumeración de usuarios en Windows y Linux
  - Herramientas: ridEnum, rpcclient

- **Día 22: Enumeración de Servicios Web**
  - Enumeración de directorios y archivos: DirBuster, Gobuster
  - Identificación de tecnologías web: Wappalyzer

- **Proyecto:** Crear un script en Python para automatizar la enumeración de servicios y usuarios en una red, integrando herramientas como enum4linux, snmpwalk y ldapsearch.

### Semana 3: Explotación de Vulnerabilidades Web
- **Día 23-25: Inyección de SQL**
  - SQL Injection (manual y automatizado)
  - Herramientas: SQLmap

- **Día 26-28: Cross-Site Scripting (XSS)**
  - Reflected y Stored XSS
  - Uso de Burp Suite para explotación

- **Día 29: File Inclusion**
  - Local File Inclusion (LFI) y Remote File Inclusion (RFI)

- **Día 30-31: Server-Side Request Forgery (SSRF)**
  - Conceptos y explotación
  - Mitigaciones y contramedidas

- **Día 32: Deserialización Insegura**
  - Conceptos y explotación
  - Herramientas y técnicas

- **Proyecto:** Desarrollar un script en Python que detecte y explote vulnerabilidades comunes en aplicaciones web, incluyendo SQL Injection, XSS, LFI, y SSRF.

### Semana 4: Explotación de Vulnerabilidades en Redes
- **Día 33-35: Explotación de Servicios Comunes**
  - FTP, SSH, RDP
  - Herramientas: Hydra, Medusa, John the Ripper

- **Día 36-38: Ataques a Protocolos de Red**
  - ARP spoofing: Ettercap
  - DNS poisoning: Dnsmasq, Responder

- **Día 39: Evasión de Firewalls y IDS/IPS**
  - Técnicas de evasión básicas y avanzadas

- **Proyecto:** Crear un script en Python que automatice ataques a servicios de red y protocolos, incluyendo fuerza bruta con Hydra y ataques ARP/DNS.

### Semana 5: Post-Explotación y Movimientos Laterales
- **Día 40-42: Post-Explotación en Sistemas Windows**
  - Recopilación de información post-explotación
  - Herramientas: Mimikatz, PowerShell Empire

- **Día 43-45: Post-Explotación en Sistemas Linux**
  - Recopilación de información post-explotación
  - Herramientas: LinEnum, Linux Exploit Suggester

- **Día 46-48: Movimientos Laterales**
  - Técnicas de pivoting
  - Herramientas: SSH pivoting, ProxyChains

- **Proyecto:** Desarrollar un script en Python para automatizar tareas post-explotación y movimientos laterales en redes comprometidas.

### Semana 6: Persistencia y Técnicas Avanzadas
- **Día 49-51: Persistencia en Sistemas Windows**
  - Técnicas de persistencia: Servicios, Scheduled Tasks, Registry
  - Herramientas: PowerShell, WMI

- **Día 52-54: Persistencia en Sistemas Linux**
  - Técnicas de persistencia: Cron Jobs, RC Scripts
  - Herramientas: bash, cron

- **Día 55: Técnicas Anti-Forense**
  - Ocultación de actividad y limpieza de logs

- **Proyecto:** Crear un script en Python que implemente técnicas de persistencia y anti-forense en sistemas comprometidos.

### Semana 7: Operaciones de Red Team y Simulación de Ataques
- **Día 56-58: Simulación de Ataques**
  - Planificación y ejecución de campañas de phishing
  - Creación de payloads con herramientas como Cobalt Strike

- **Día 59-61: Evasión de Detección**
  - Técnicas de evasión de EDR/AV
  - Herramientas: Obfuscación de scripts

- **Día 62-64: Exfiltración de Datos**
  - Técnicas y herramientas para exfiltración
  - Herramientas: DNS exfiltration scripts, HTTPS tunneling

- **Proyecto:** Desarrollar un script en Python para simular ataques avanzados, incluyendo la creación de payloads y técnicas de evasión de detección.

### Semana 8: Proyecto Final y Práctica Avanzada
- **Día 65-71: Proyecto Final - Pentest Completo**
  - Realización de un pentest completo a un entorno simulado
  - Documentación y reporte de hallazgos

- **Día 72-75: Práctica Avanzada**
  - Perfeccionamiento de técnicas y herramientas utilizadas
  - Desafíos prácticos adicionales y revisión de temas complejos

```
