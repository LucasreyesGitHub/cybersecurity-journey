# ⚠️ Guía de Seguridad y Privacidad (OPSEC)

Este documento establece las directrices para la protección de datos personales y la seguridad del sistema anfitrión durante la documentación y ejecución de laboratorios de ciberseguridad.

## 1. Qué NUNCA incluir en el Repositorio (Sanitización)

Para proteger la privacidad y seguridad del analista, los siguientes datos deben ser eliminados o reemplazados por valores genéricos antes de realizar un `git push`:

* **IP Pública:** Nunca documentar la IP real proporcionada por el ISP (Internet Service Provider). Las IPs locales (192.168.x.x, 10.x.x.x) son seguras de compartir.
* **Rutas de Usuario Reales:** Al copiar logs de terminales de Windows o Linux, asegúrate de no mostrar nombres de usuario reales. 
    * *Mal:* `C:\Users\LucasReyes\Documents\...`
    * *Bien:* `C:\Users\User\Documents\...`
* **Tokens y API Keys:** Nunca subir claves de API (como de VirusTotal o Shodan) o tokens de acceso a servicios en la nube.
* **Credenciales Personales:** Nunca usar contraseñas reales en las pruebas que luego serán documentadas. Usa siempre contraseñas de ejemplo como `password123`.

## 2. Límites del Laboratorio (Reglas de Oro)

Para garantizar que las actividades no afecten al sistema anfitrión (Windows) o a terceros:

1.  **Aislamiento de Archivos:** No utilizar "Carpetas Compartidas" (Shared Folders) con máquinas virtuales vulnerables (como Metasploitable) para evitar que malware pueda infectar el disco del host.
2.  **Escaneo Externo Prohibido:** Está estrictamente prohibido dirigir herramientas de escaneo (Nmap) o explotación fuera del rango de IPs asignado localmente a las máquinas virtuales.
3.  **Descargas Seguras:** Todas las herramientas de hacking y muestras de malware deben descargarse y ejecutarse **exclusivamente** dentro de la máquina virtual Kali Linux.

## 3. Manejo de IPs en la Documentación

En este repositorio, se opta por documentar las IPs privadas de las máquinas virtuales para mantener la coherencia técnica del laboratorio.
* **Seguridad:** Las IPs privadas no son rastreables ni accesibles desde el internet público.
* **Claridad:** Permite a otros analistas entender la topología de red y el flujo del ataque/defensa.

---
*Este documento es una declaración de responsabilidad ética y técnica en el ejercicio de la ciberseguridad.*
