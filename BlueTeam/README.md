# 🔵 Blue Team Operations & Defensive Security

## 🛡️ Objetivo Defensivo
Esta sección está dedicada al análisis de la seguridad desde la perspectiva del defensor (SOC Analyst / Incident Responder). El objetivo es entender la "huella" que dejan los ataques para mejorar la detección, el monitoreo y el endurecimiento (hardening) de los sistemas.

## 📖 Bibliografía de Referencia
* **"Blue Team Handbook: Incident Response Edition"** - Don Murdoch.
* **"Practical Packet Analysis"** - Chris Sanders.
* **"The Practice of Network Security Monitoring"** - Richard Bejtlich.

## 🛠️ Toolstack Defensivo (Laboratorio)
* **Análisis de Red:** Wireshark, Tshark, Zeek.
* **SIEM/Monitoreo:** Wazuh, ELK Stack (Elasticsearch, Logstash, Kibana).
* **Análisis de Logs:** Grep/Awk (Linux), Event Viewer (Windows).
* **IDS/IPS:** Suricata, Snort.

## 🗂️ Estructura de Contenidos
1.  **/Traffic-Analysis:** Análisis de archivos `.pcap` donde se identifican escaneos, inyecciones SQL o tráfico de C2 (Command & Control).
2.  **/Incident-Response:** Simulacros de respuesta ante incidentes, documentando los pasos de contención y erradicación.
3.  **/Hardening-Guides:** Guías de configuración segura para servicios (SSH, Apache, Bases de Datos) basadas en benchmarks de CIS.
4.  **/SIEM-Rules:** Reglas personalizadas de detección creadas para identificar ataques específicos documentados en la sección de Red Team.

---
*"La mejor defensa es entender profundamente el ataque."*
