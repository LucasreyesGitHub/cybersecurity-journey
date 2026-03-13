🔍 Hallazgos Críticos Identificados

A partir de este escaneo, se destacan los siguientes puntos para investigar en las fases de Red Team y Blue Team:

    Puerto 21 (FTP): Versión vsftpd 2.3.4. Es altamente crítica por tener un backdoor conocido. Además, permite Anonymous Login.

    Puerto 1524 (Bindshell): Este puerto es una "puerta trasera" directa que entrega una shell de root sin pedir contraseña.

    Puerto 23 (Telnet): Servicio que transmite todo en texto claro, un riesgo crítico para la interceptación de credenciales.

    Puerto 445 (SMB): La versión de Samba 3.0.20 es vulnerable a ejecución remota de código (RCE) mediante usermap_script.

    Puerto 6667 (IRC): La versión Unreal3.2.8.1 también contiene un backdoor muy famoso.
