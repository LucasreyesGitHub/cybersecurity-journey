# Lab 01: Despliegue de Entorno Metasploitable 2

## Objetivo
Configurar un entorno controlado de pruebas para la ejecución de auditorías de seguridad y monitoreo de eventos (SOC).

## Detalles del Entorno
* **Target:** Metasploitable 2 (Linux 2.6.X)
* **Attacker:** Kali Linux
* **Conectividad:** Adaptador Puente (Bridged) / Red NAT

## Fase de Conectividad
Se verificó la visibilidad entre ambas máquinas mediante el comando `ping`.
- **IP Metasploitable:** [Poner aquí la IP que te dio ifconfig]
- **IP Kali Linux:** [Poner aquí la IP de tu Kali]

## Escaneo de Reconocimiento (Nmap)
Ejecución de escaneo agresivo para identificación de servicios y versiones:
`nmap -T4 -A [IP_METASPLOITABLE]`

### Resultados del Escaneo:
```text
[COPIA Y PEGA AQUÍ EL RESULTADO QUE TE DIO LA TERMINAL DE KALI]
