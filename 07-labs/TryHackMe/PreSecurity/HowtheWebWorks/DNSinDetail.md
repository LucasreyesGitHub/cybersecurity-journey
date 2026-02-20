# DNS en Detalle

## 1. ¿Qué es DNS?

El **DNS (Domain Name System)** es el sistema que traduce nombres de dominio legibles por humanos (como `google.com`) en direcciones IP (como `142.250.190.14`), que son necesarias para que los dispositivos se comuniquen en la red.

Se lo suele describir como la guía telefónica de Internet.

---

## 2. Importancia en Ciberseguridad

DNS es un componente crítico porque:

- Puede ser explotado para realizar ataques.
- Permite detectar actividad maliciosa mediante análisis de consultas.
- Es fundamental en el monitoreo de tráfico dentro de un SOC.
- Interviene en ataques como phishing, malware y exfiltración de datos.

El análisis de logs DNS es una práctica común en seguridad defensiva.

---

## 3. Funcionamiento del Proceso de Resolución DNS

Cuando un usuario escribe `www.ejemplo.com`, ocurre lo siguiente:

1. El navegador consulta al **resolver DNS** configurado en el sistema.
2. Si la respuesta no está en caché, el resolver consulta:
   - Servidores **Root**
   - Servidores **TLD** (.com, .org, etc.)
   - Servidor **autoritativo**
3. El servidor autoritativo responde con la IP correspondiente.
4. El resolver devuelve la IP al cliente.

Este proceso se denomina **resolución recursiva**.

---

## 4. Tipos de Servidores DNS

- **Resolver Recursivo**  
  Realiza las consultas en nombre del cliente.

- **Servidor Root**  
  Primer nivel de la jerarquía DNS. Indica qué servidor TLD consultar.

- **Servidor TLD**  
  Gestiona dominios de nivel superior como `.com`, `.net`, `.org`.

- **Servidor Autoritativo**  
  Contiene la información definitiva del dominio y responde con la IP correcta.

---

## 5. Tipos de Registros DNS

| Tipo  | Función |
|-------|---------|
| A     | Asocia un dominio con una dirección IPv4 |
| AAAA  | Asocia un dominio con una dirección IPv6 |
| MX    | Define el servidor de correo del dominio |
| CNAME | Alias que apunta a otro dominio |
| TXT   | Información adicional (SPF, verificaciones, etc.) |
| NS    | Indica los servidores de nombres del dominio |

---

## 6. Ataques Relacionados con DNS

### DNS Spoofing / Cache Poisoning
Manipulación de respuestas DNS para redirigir tráfico hacia un servidor malicioso.

### DNS Tunneling
Uso del protocolo DNS para transportar datos ocultos, común en exfiltración.

### DNS Amplification
Ataque DDoS que aprovecha respuestas DNS amplificadas para saturar un objetivo.

---

## 7. DNS en un Entorno SOC

En un Security Operations Center se analiza:

- Consultas a dominios sospechosos.
- Tráfico hacia dominios recientemente registrados.
- Consultas repetitivas que pueden indicar beaconing.
- Actividad anómala en patrones de resolución.

Herramientas utilizadas frecuentemente:

- Wireshark
- Splunk
- Zeek

---

## 8. Comandos Prácticos

Consultar resolución DNS:

```bash
nslookup google.com
dig google.com

Ver servidores DNS configurados en Linux:
cat /etc/resolv.conf

```

## 9. Conceptos Clave

### TTL (Time To Live)
Tiempo durante el cual una respuesta DNS permanece almacenada en caché antes de expirar.

### Resolución Recursiva
El resolver realiza todas las consultas necesarias hasta obtener la respuesta final para el cliente.

### Resolución Iterativa
Cada servidor DNS responde indicando cuál es el siguiente servidor que debe consultarse.

### Caché DNS
Almacenamiento temporal de respuestas DNS para reducir latencia y carga en los servidores.

### DNSSEC
Extensión de seguridad que agrega validación criptográfica a las respuestas DNS para evitar manipulación.

---

## 10. Conclusión

DNS es una infraestructura fundamental de Internet y un punto estratégico en ciberseguridad.

Comprender su funcionamiento permite:

- Detectar amenazas.
- Analizar tráfico de red.
- Identificar comportamientos anómalos.
- Entender vectores de ataque basados en resolución de nombres.

Un dominio sólido de DNS es esencial para cualquier profesional que aspire a trabajar en redes o en un SOC.
