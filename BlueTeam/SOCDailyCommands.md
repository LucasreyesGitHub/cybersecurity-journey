# Comandos Diarios: Blue Team / SOC

### 🕵️ Monitoreo de Red y Conexiones
* `netstat -tunpa` -> Ver todas las conexiones activas y qué procesos las abrieron.
* `ss -lntp` -> Ver puertos escuchando en el sistema (útil para detectar backdoors).
* `tcpdump -i eth0 icmp` -> Ver en tiempo real si alguien nos está haciendo ping.

### 📜 Análisis de Logs (Linux)
* `tail -f /var/log/auth.log` -> Ver intentos de inicio de sesión en tiempo real (útil contra fuerza bruta).
* `grep "Failed password" /var/log/auth.log` -> Filtrar solo los intentos fallidos de login.
* `journalctl -u ssh` -> Revisar logs específicos del servicio SSH.

### 🛡️ Verificación de Integridad
* `ps aux --forest` -> Ver árbol de procesos (ayuda a ver procesos "padre" sospechosos).
* `find / -perm -4000 2>/dev/null` -> Buscar archivos con bit SUID (posible vector de escalada de privilegios).
