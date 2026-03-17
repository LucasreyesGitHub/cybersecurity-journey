# Comandos Diarios: Red Team

### 🔍 Escaneo y Reconocimiento (Nmap)
* `nmap -sV -sC -T4 [IP]` -> Escaneo rápido de versiones y scripts básicos.
* `nmap -p- [IP]` -> Escaneo de los 65,535 puertos (lento pero necesario).
* `nmap --script vuln [IP]` -> Ejecuta scripts de nmap para detectar vulnerabilidades conocidas.

### 🐍 Explotación (Metasploit)
* `msfconsole` -> Abrir el framework de Metasploit.
* `search [servicio]` -> Buscar exploits para un servicio específico (ej: `search vsftpd`).
* `use [ruta_del_exploit]` -> Cargar un módulo.
* `show options` -> Ver qué parámetros necesita el exploit (como RHOSTS).
* `exploit` o `run` -> Ejecutar el ataque.

### 📂 Transferencia de Archivos y Conexión
* `nc -lvnp [puerto]` -> Escuchar conexiones entrantes (Netcat).
* `python3 -m http.server 80` -> Levantar un servidor web rápido para pasar archivos a la víctima.
