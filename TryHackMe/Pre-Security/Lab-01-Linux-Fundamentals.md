# Lab 01 – Linux Fundamentals (TryHackMe)

## 📌 Objetivo
Adquirir una base sólida en Linux para ciberseguridad, comprendiendo el uso
de la terminal, la estructura del sistema de archivos, usuarios, permisos,
procesos y logs.  
Este laboratorio se basa en *Linux Fundamentals Part 1, 2 y 3* de TryHackMe.

---

## 🖥️ Entorno
- Sistema operativo: Kali Linux
- Virtualización: Oracle VirtualBox
- RAM: 8 GB
- CPU: 2 cores
- Red: NAT

---

## 📁 Linux Fundamentals – Contenidos

### 🧱 Parte 1 – Fundamentos y navegación
- Uso de la terminal Linux
- Navegación por el sistema de archivos
- Comandos básicos
- Comprensión de rutas absolutas y relativas

**Relevancia en ciberseguridad:**  
Permite el reconocimiento inicial de un sistema, usuarios activos y
estructura de archivos.

---

### 🧱 Parte 2 – Archivos, permisos y acceso remoto
- Gestión de archivos y directorios
- Permisos de lectura, escritura y ejecución
- Usuarios y grupos
- Uso de `sudo`
- Acceso remoto mediante SSH

**Relevancia en ciberseguridad:**  
Los permisos y accesos mal configurados son una causa frecuente de incidentes
y escaladas de privilegios.

---

### 🧱 Parte 3 – Procesos, automatización y logs
- Edición de archivos desde la terminal
- Gestión de procesos
- Instalación de paquetes
- Automatización de tareas
- Análisis de logs del sistema

**Relevancia en ciberseguridad:**  
Los procesos y logs son la principal fuente de evidencia para detección y
respuesta a incidentes en entornos SOC.

---

## 📄 Logs del sistema
- `/var/log/auth.log` → autenticaciones y uso de sudo
- `/var/log/syslog` → eventos generales del sistema
- Logs de servicios (Apache, SSH, etc.)

---

## 📌 Conclusión
Este laboratorio proporciona los fundamentos esenciales de Linux necesarios
para roles de Blue Team, SOC y análisis de seguridad.  
Dominar estos conceptos es clave para interpretar eventos, investigar
incidentes y administrar sistemas de forma segura.

---

## 🏷️ Tags
`linux` `kali` `tryhackme` `pre-security` `fundamentals` `soc`

