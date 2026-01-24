# Lab 02 – Networking Fundamentals (Kali Linux)

## 📌 Objetivo
Comprender cómo un sistema Linux se conecta a una red, cómo enruta el tráfico
y cómo resuelve nombres de dominio.  
Estos conceptos son fundamentales para análisis de red, SOC y pentesting.

---

## 🖥️ Entorno
- SO: Kali Linux
- Virtualización: VirtualBox
- RAM: 4 GB
- CPU: 2 cores
- Red: NAT

---

## 🔍 Comandos utilizados y análisis

### ip a
**Descripción:**  
Muestra las interfaces de red del sistema y sus direcciones IP.

**¿Para qué sirve en ciberseguridad?**  
Permite identificar:
- qué interfaces están activas
- qué IP tiene la máquina
- si está conectada a una red interna o externa  

Un atacante lo usa para reconocimiento inicial.  
Un analista SOC lo usa para validar configuración de red.

---

### ip route
**Descripción:**  
Muestra la tabla de ruteo del sistema.

**¿Para qué sirve en ciberseguridad?**  
Indica:
- por dónde sale el tráfico
- cuál es el gateway
- si hay rutas sospechosas

En SOC puede revelar:
- desvíos de tráfico
- configuraciones maliciosas

---

### cat /etc/resolv.conf
**Descripción:**  
Muestra los servidores DNS configurados en el sistema.

**¿Para qué sirve en ciberseguridad?**  
El DNS es crítico:
- DNS malicioso puede redirigir tráfico
- DNS incorrecto rompe la conectividad

En incident response se revisa para detectar DNS hijacking.

---

### ping -c 4 8.8.8.8
**Descripción:**  
Envía paquetes ICMP a una IP para verificar conectividad.

**¿Para qué sirve en ciberseguridad?**  
Permite confirmar:
- salida a Internet
- funcionamiento básico de la red

Si responde a IP pero no a dominios, el problema suele ser DNS.

---

### ping -c 4 google.com
**Descripción:**  
Verifica conectividad y resolución de nombres DNS.

**¿Para qué sirve en ciberseguridad?**  
Confirma:
- funcionamiento del DNS
- correcta resolución de dominios

Útil para diferenciar fallas de red vs fallas de DNS.

---

## 🧠 Análisis general
El reconocimiento de red es uno de los primeros pasos tanto en defensa
como en ataque.  
Entender cómo un sistema se comunica permite detectar configuraciones
incorrectas, tráfico anómalo o intentos de evasión.

---

## 🧾 Conclusión
Este laboratorio refuerza los fundamentos de networking en Linux,
esenciales para roles de SOC, análisis de tráfico y seguridad ofensiva.

---

## 🏷️ Tags
`networking` `linux` `kali` `soc` `tryhackme` `pre-security`
