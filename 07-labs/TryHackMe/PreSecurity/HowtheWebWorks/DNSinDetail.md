
DNS en Detalle
¿Qué es DNS?

El DNS (Domain Name System) es el sistema que traduce nombres de dominio legibles por humanos, como google.com, en direcciones IP, como 142.250.190.14, que son las que las computadoras utilizan para comunicarse en la red.

Se lo suele describir como la guía telefónica de Internet.

Importancia en Ciberseguridad

DNS es un componente crítico porque:

Puede ser explotado para realizar ataques.

Permite detectar actividad maliciosa mediante análisis de consultas.

Es fundamental en el monitoreo de tráfico dentro de un SOC.

Interviene en ataques como phishing, malware y exfiltración de datos.

El análisis de logs DNS es una práctica común en entornos de seguridad defensiva.

Funcionamiento del Proceso de Resolución DNS

Cuando un usuario escribe www.ejemplo.com, ocurre lo siguiente:

El navegador consulta al resolver DNS configurado en el sistema (generalmente el del ISP).

Si la respuesta no está en caché, el resolver consulta:

Servidores Root

Servidores TLD (.com, .org, etc.)

Servidor autoritativo del dominio

El servidor autoritativo responde con la dirección IP correspondiente.

El resolver devuelve la IP al cliente.

Este proceso se denomina resolución recursiva.

Tipos de Servidores DNS

Resolver Recursivo
Realiza las consultas en nombre del cliente.

Servidor Root
Primer nivel de la jerarquía DNS. Indica qué servidor TLD consultar.

Servidor TLD
Gestiona dominios de nivel superior como .com, .net, .org.

Servidor Autoritativo
Contiene la información definitiva del dominio y responde con la IP correcta.

Tipos de Registros DNS

A
Asocia un dominio con una dirección IPv4.

AAAA
Asocia un dominio con una dirección IPv6.

MX
Define el servidor de correo del dominio.

CNAME
Alias que apunta a otro dominio.

TXT
Permite almacenar información adicional (por ejemplo SPF o verificaciones).

NS
Indica los servidores de nombres del dominio.

Ataques Relacionados con DNS

DNS Spoofing / Cache Poisoning
Manipulación de respuestas DNS para redirigir tráfico hacia un servidor malicioso.

DNS Tunneling
Uso del protocolo DNS para transportar datos ocultos, común en exfiltración.

DNS Amplification
Ataque DDoS que aprovecha respuestas DNS amplificadas para saturar un objetivo.

DNS en un Entorno SOC

En un Security Operations Center se analiza:

Consultas a dominios sospechosos.

Tráfico hacia dominios recientemente registrados.

Consultas repetitivas que pueden indicar beaconing.

Actividad anómala en patrones de resolución.

Herramientas utilizadas frecuentemente incluyen Wireshark, Splunk y Zeek.

Comandos Prácticos

Consultar resolución DNS:

nslookup google.com
dig google.com

Ver servidores DNS configurados en Linux:

cat /etc/resolv.conf
Conceptos Clave

TTL (Time To Live)
Tiempo durante el cual una respuesta DNS permanece en caché.

Resolución recursiva
El resolver realiza todas las consultas necesarias hasta obtener la respuesta final.

Resolución iterativa
Cada servidor responde indicando el siguiente servidor a consultar.

Caché DNS
Almacenamiento temporal de respuestas para reducir latencia.

DNSSEC
Extensión de seguridad que agrega validación criptográfica a las respuestas DNS.

Conclusión

DNS es una infraestructura fundamental de Internet y un punto estratégico en ciberseguridad. Comprender su funcionamiento permite detectar amenazas, analizar tráfico de red y entender múltiples vectores de ataque utilizados por actores maliciosos.
