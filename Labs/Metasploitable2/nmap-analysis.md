# Escaneo de Reconocimiento con Nmap

En esta fase se realiza una enumeración profunda de los servicios activos en el objetivo para identificar posibles vectores de ataque y debilidades de configuración.

## ⚙️ Comando Ejecutado
`nmap -T4 -A -v 192.168.1.8`

### Explicación de los Parámetros:
* **`-T4` (Timing Template):** Establece la agresividad del escaneo en nivel 4 (de 5). Aumenta la velocidad de los paquetes para reducir el tiempo de espera. Es ideal para laboratorios, aunque muy "ruidoso" en entornos reales.
* **`-A` (Aggressive Scan):** Es un "todo en uno". Activa la detección de Sistema Operativo (`-O`), el escaneo de versiones de servicios (`-sV`), el uso de scripts predeterminados de Nmap (`-sC`) y el traceroute.
* **`-v` (Verbose):** Aumenta el nivel de detalle en la terminal mientras el escaneo está en curso, permitiendo ver los puertos abiertos en tiempo real antes de finalizar.
* **`192.168.1.8`:** La dirección IP de la máquina objetivo (Metasploitable 2).

---

## 📄 Resultado del Escaneo (Output)

```text
Starting Nmap 7.95 ( [https://nmap.org](https://nmap.org) ) at 2026-03-13 09:29 EDT
Nmap scan report for 192.168.1.8
Host is up (0.00070s latency).
Not shown: 977 filtered tcp ports (no-response)
PORT      STATE SERVICE     VERSION
21/tcp    open  ftp         vsftpd 2.3.4
|_ftp-anon: Anonymous FTP login allowed (FTP code 230)
22/tcp    open  ssh         OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)
23/tcp    open  telnet      Linux telnetd
25/tcp    open  smtp        Postfix smtpd
53/tcp    open  domain      ISC BIND 9.4.2
80/tcp    open  http        Apache httpd 2.2.8 ((Ubuntu) DAV/2)
139/tcp   open  netbios-ssn Samba smbd 3.X - 4.X
445/tcp   open  netbios-ssn Samba smbd 3.0.20-Debian
1099/tcp  open  java-rmi    GNU Classpath grmiregistry
1524/tcp  open  bindshell   Metasploitable root shell
3306/tcp  open  mysql       MySQL 5.0.51a-3ubuntu5
5432/tcp  open  postgresql  PostgreSQL DB 8.3.0 - 8.3.7
5900/tcp  open  vnc         VNC (protocol 3.3)
6667/tcp  open  irc         UnrealIRCd
8180/tcp  open  http        Apache Tomcat/Coyote JSP engine 1.1

<img width="706" height="413" alt="image" src="https://github.com/user-attachments/assets/cbaeb136-3ad4-4093-9513-15cebb29944f" />


[...]
