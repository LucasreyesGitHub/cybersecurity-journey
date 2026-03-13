# Red Team Analysis: Metasploitable 2

Este documento detalla las técnicas de explotación y vectores de ataque identificados específicamente durante el laboratorio de Metasploitable 2.

### 🚩 Vectores Críticos
* **Servicio FTP (vsftpd 2.3.4):** Identificado un backdoor histórico. La técnica consiste en intentar una conexión que dispare el puerto 6200.
* **Java RMI (Puerto 1099):** Un servicio vulnerable por defecto que permite ejecución remota de código (RCE).
* **VNC (Puerto 5900):** Se identifica el uso de contraseñas débiles por defecto (ej. 'password').

### 💡 Tip de Pentesting
Siempre que encuentres un sistema antiguo (Linux 2.6), prioriza la búsqueda de **Kernels exploits** para escalada de privilegios.
