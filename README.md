# 🛡️ Cybersecurity Engineering & Research Lab

## 🚀 Mi Objetivo: De la Teoría a la Autonomía Técnica
Este repositorio documenta mi transición de un aprendizaje guiado y lineal hacia la **maestría técnica autodidacta**. Mi meta es convertirme en un profesional de seguridad con capacidad analítica, capaz de montar infraestructuras, identificar vulnerabilidades complejas y proponer estrategias de defensa basadas en datos reales, no en manuales preestablecidos.

He decidido alejarme de plataformas de aprendizaje gamificadas para centrarme en el **Hacking Ético de "Caja Negra"** y la **Defensa Activa**, utilizando laboratorios locales en **VirtualBox** y bibliografía técnica de referencia. 

---

## 🏗️ Mi Infraestructura de Laboratorio (The Sandbox)
A diferencia de los entornos en la nube, mi laboratorio está diseñado para replicar escenarios de redes corporativas reales:
* **Virtualización:** Entorno aislado en VirtualBox con segmentación de redes (NAT Network / Host-Only).
* **Ofensiva:** Estación de trabajo Kali Linux personalizada con herramientas de auditoría manual.
* **Defensiva:** Análisis de tráfico mediante Wireshark y monitoreo de logs de sistemas vulnerados.
* **Objetivos:** Despliegue de máquinas de **VulnHub** (Kioptrix, Mr. Robot, etc.) y servidores Linux/Windows con configuraciones inseguras.

---

## 📖 Framework de Aprendizaje (Ruta Bibliográfica)
Mi formación se estructura bajo el estudio profundo de los siguientes pilares:

| Pilar | Referencia Bibliográfica | Aplicación Práctica |
| :--- | :--- | :--- |
| **Fundamentos** | *Penetration Testing* (Georgia Weidman) | Construcción de laboratorios y explotación manual (sin Metasploit). |
| **Operaciones** | *The Hacker Playbook 3* (Peter Kim) | Simulación de campañas de Red Team y movimientos laterales. |
| **Defensa** | *Blue Team Handbook: IR* (Don Murdoch) | Respuesta ante incidentes y análisis forense post-explotación. |
| **Redes** | *Practical Packet Analysis* (Chris Sanders) | Inspección profunda de paquetes para detección de anomalías. |

---

## 📂 Organización del Repositorio

### [🔴 Red Team - Operaciones Ofensivas](./RedTeam/)
Documentación detallada de mis auditorías. No son simples soluciones, sino **análisis de vectores de ataque**.
* **Vulnerability Research:** Investigación de exploits y bypass de seguridad.
* **Privilege Escalation:** Técnicas de elevación de privilegios en Linux/Windows.
* **Exploitation Writeups:** El "paso a paso" lógico de mis intrusiones en máquinas de VulnHub.

### [🔵 Blue Team - Operaciones Defensivas](./BlueTeam/)
El análisis de lo que ocurre cuando un sistema es atacado.
* **Incident Response:** Documentación de la "huella" que dejan los ataques.
* **Traffic Analysis:** Capturas (.pcap) analizadas para entender el comportamiento de protocolos maliciosos.
* **Hardening:** Guías de configuración segura para mitigar las brechas encontradas.

---

## 📉 Mi Compromiso de Documentación
Cada entrada en este repositorio sigue el estándar de **"Lecciones Aprendidas"**. No busco cantidad, sino calidad de análisis. Cada máquina vulnerada incluye:
1.  Metodología aplicada (PTES).
2.  Errores cometidos y cómo se solucionaron (Troubleshooting).
3.  Análisis de la causa raíz de la vulnerabilidad.

---
*"El hacking no es una receta, es un proceso de investigación constante."*
