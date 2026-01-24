# Lab 01 – Linux Basics (Kali Linux)

## 📌 Objetivo
Familiarizarse con comandos básicos de Linux para identificar
usuarios, sistema, red, procesos y logs.  
Este conocimiento es fundamental tanto para Blue Team (SOC) como para Pentesting.

---

## 🖥️ Entorno
- SO: Kali Linux
- Virtualización: VirtualBox
- RAM asignada: 4 GB
- CPU: 2 cores
- Red: NAT

---

## 🔍 Comandos utilizados y análisis

### whoami
**Descripción:**  
Muestra el usuario actual que ejecuta comandos en el sistema.

**Utilidad en ciberseguridad:**  
Permite saber si se tienen privilegios elevados.  
Un atacante buscaría escalar privilegios si no es root.

---

### hostname
**Descripción:**  
Muestra el nombre del host.

**Utilidad en ciberseguridad:**  
En redes corporativas permite identificar máquinas comprometidas.

---

### uname -a
**Descripción:**  
Muestra información del kernel y arquitectura del sistema.

**Utilidad en ciberseguridad:**  
Sirve para identificar vulnerabilidades específicas del kernel.

---

### ip a
**Descripción:**  
Muestra interfaces de red y direcciones IP.

**Utilidad en ciberseguridad:**  
Clave para reconocimiento de red y detección de configuraciones inseguras.

---

### ps aux
**Descripción:**  
Lista procesos en ejecución.

**Utilidad en ciberseguridad:**  
En SOC se usa para detectar procesos maliciosos o inusuales.

---

### ls /var/log
**Descripción:**  
Lista archivos de log del sistema.

**Utilidad en ciberseguridad:**  
Los logs son fundamentales para análisis forense e incident response.

---

## 🧠 Conclusión
Este laboratorio introduce conceptos básicos de Linux aplicados a
ciberseguridad.  
El reconocimiento del sistema es el primer paso tanto en defensa
como en ataque.

---

## 🏷️ Tags
`linux` `kali` `tryhackme` `pre-security` `soc` `fundamentals`
