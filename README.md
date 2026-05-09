# 🛡️ Cybersecurity Engineering & Research Lab

> Repositorio de investigación, laboratorios y herramientas de seguridad ofensiva y defensiva.  
> Autor: **Lucas Reyes** — Analista Bancario en transición a Ciberseguridad | Montevideo, Uruguay

[![GitHub](https://img.shields.io/badge/GitHub-LucasreyesGitHub-181717?style=flat&logo=github)](https://github.com/LucasreyesGitHub)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-lucasreyes2003-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/lucasreyes2003)
[![Portfolio](https://img.shields.io/badge/Portfolio-SOC%20Projects-2E75B6?style=flat&logo=vercel)](https://cyber-security-proyects.vercel.app/)
[![Cisco](https://img.shields.io/badge/Cisco-Junior%20Cybersecurity%20Analyst-1BA0D7?style=flat&logo=cisco)](https://www.netacad.com)

---

## 📌 Contexto y Objetivo

Soy analista de sistemas con experiencia en entornos bancarios regulados (FATCA/CRS, Bantotal, BROU), actualmente en transición hacia roles de **SOC Analyst** y **Data Security**.

Este repositorio documenta mi proceso de formación técnica autodidacta en ciberseguridad: desde fundamentos de redes y análisis de tráfico hasta laboratorios de hacking ético en entornos controlados. El foco está en la **defensa activa** y el **análisis de amenazas**, aplicando los conocimientos directamente a contextos financieros.

---

## 🏗️ Infraestructura de Laboratorio

| Componente | Detalle |
|---|---|
| **Virtualización** | VirtualBox con redes segmentadas (NAT + Host-Only) |
| **Estación ofensiva** | Kali Linux (herramientas: nmap, Metasploit, Burp Suite) |
| **Estación defensiva** | Análisis de tráfico con Wireshark, monitoreo de logs |
| **Objetivos de práctica** | VulnHub (Kioptrix, Mr. Robot), servidores configurados manualmente |
| **Plataformas** | TryHackMe · Hack The Box |

---

## 📂 Estructura del Repositorio

```
cybersecurity-journey/
│
├── 00-roadmap/                  # Hoja de ruta y planificación de aprendizaje
├── BlueTeam/                    # Defensa: análisis de logs, monitoreo, respuesta a incidentes
├── RedTeam/                     # Ofensiva: auditoría, enumeración, explotación controlada
├── Labs/                        # Laboratorios prácticos documentados paso a paso
├── HackTheBox/                  # Writeups y notas de máquinas HTB
├── Projects/                    # Herramientas y scripts de seguridad desarrollados
├── Introduction-SecurityCompliance/  # Fundamentos de cumplimiento y normativa
└── Guide/                       # Guías de referencia rápida y cheatsheets
```

---

## 🔴 Red Team

Metodología de auditoría basada en fases:

1. **Reconocimiento** — OSINT, enumeración de puertos y servicios
2. **Análisis de vulnerabilidades** — identificación y clasificación
3. **Explotación controlada** — entornos aislados únicamente
4. **Post-explotación** — escalada de privilegios, persistencia (laboratorio)
5. **Reporte** — documentación estructurada de hallazgos

Referencia principal: *Hacking Ético* — Carlos Tori

---

## 🔵 Blue Team

Foco en detección, análisis y respuesta:

- Análisis de tráfico de red con Wireshark
- Revisión e interpretación de logs del sistema
- Detección de anomalías y patrones de ataque
- Documentación de procedimientos de respuesta a incidentes

Referencias:
- *Guía Nacional de Notificación y Gestión de Ciberincidentes* (Gobierno de España)
- *Guías de Seguridad para PYMES* — INCIBE
- *Análisis de Tráfico con Wireshark* — INCIBE

---

## 🛠️ Proyectos Desarrollados

### 🔗 Link Sentinel
Herramienta Python para análisis y detección de URLs maliciosas.
- Integración con **VirusTotal API** para clasificación de amenazas en tiempo real
- Arquitectura contenerizada con **Docker**
- Caso de uso: detección de phishing en entornos financieros

### 📷 QrSocAnalyzer
Analizador de códigos QR con detección de amenazas embebidas.
- Extracción y evaluación de URLs codificadas contra bases de inteligencia de amenazas
- Orientado a prevención de fraude en canales digitales bancarios
- Stack: Python · VirusTotal API

### 📊 Financial Fraud Dashboard *(en desarrollo)*
Dashboard Power BI para análisis de patrones de fraude financiero.
- Identificación de sectores de mayor exposición
- Vectores de ataque más frecuentes
- Soporte a decisiones para áreas de seguridad bancaria

> 🔗 [Ver todos los proyectos en el Portfolio](https://cyber-security-proyects.vercel.app/)

---

## 📖 Framework de Aprendizaje

| Pilar | Referencia | Aplicación |
|---|---|---|
| **Gestión de Incidentes** | *Guía Nacional de Ciberincidentes* (Gob. España) | Metodología de reporte y categorización de ataques |
| **Hacking Ético** | *Hacking Ético* — Carlos Tori | Fases de intrusión y auditoría técnica |
| **Defensa / SOC** | *Guías de Seguridad* — INCIBE | Hardening de sistemas y monitoreo de red |
| **Análisis de Red** | *Análisis de Tráfico con Wireshark* — INCIBE | Inspección de paquetes y detección de anomalías |
| **Certificación** | Cisco Junior Cybersecurity Analyst (en curso) | Path estructurado de 120h hacia rol SOC |

---

## 🎯 Stack Técnico

```
Seguridad:    Kali Linux · Wireshark · Nmap · Metasploit · Burp Suite · VirusTotal API
Desarrollo:   Python · Docker · Git · GitHub · C#
Datos & BI:   Power BI · SQL · IBM Cognos · Excel Avanzado
Bancario:     Bantotal · FATCA/CRS · Auditoría de Datos · Reportería Regulatoria
```

---

## 📬 Contacto

- **LinkedIn:** [linkedin.com/in/lucasreyes2003](https://linkedin.com/in/lucasreyes2003)
- **Portfolio:** [cyber-security-proyects.vercel.app](https://cyber-security-proyects.vercel.app/)
- **Email:** lucasrfcapilla.1b2015@gmail.com

---

> *"La seguridad no es un producto, es un proceso."* — Bruce Schneier
