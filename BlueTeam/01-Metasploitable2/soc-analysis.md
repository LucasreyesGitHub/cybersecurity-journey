
# Blue Team Analysis: Metasploitable 2

Análisis de seguridad defensiva y estrategias de mitigación basadas en los hallazgos del entorno Metasploitable 2.

### 🛡️ Estrategias de Defensa (SOC)
* **Detección de Escaneo Agresivo:** El uso de `nmap -A` genera firmas TCP específicas. Un analista debe monitorear picos de conexiones SYN/ACK en intervalos menores a 1 segundo.
* **Remediación de Servicios Legados:** La recomendación principal es la migración de FTP (texto claro) a SFTP (cifrado) para evitar la interceptación de credenciales.

### 🔍 Indicadores de Compromiso (IoCs)
* Intentos de acceso root fallidos en servicios SSH/Telnet.
* Tráfico saliente inusual por puertos altos después de una interacción con el puerto 21.
