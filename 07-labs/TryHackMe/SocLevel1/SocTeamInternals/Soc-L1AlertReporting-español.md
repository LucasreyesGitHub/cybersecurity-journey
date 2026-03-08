# SOC L1 Alert Triage — Notas

## Descripción

Este room introduce los conceptos básicos del **análisis de alertas en un Security Operations Center (SOC)**.  

Los analistas SOC reciben alertas generadas por herramientas de seguridad y deben investigarlas para determinar si representan una amenaza real o un falso positivo.

En este laboratorio se aprende:

- Qué son eventos y alertas
- Cómo funcionan las plataformas de gestión de alertas
- Roles dentro de un SOC
- Propiedades de una alerta
- Proceso de triage de alertas
- Cómo investigar y clasificar incidentes

Los analistas **SOC Level 1** actúan como la **primera línea de defensa** contra amenazas de seguridad.

---

# Eventos vs Alertas

## Eventos

Un **evento** es cualquier actividad registrada dentro de un sistema.

Ejemplos:

- Inicio de sesión de usuario
- Descarga de archivos
- Ejecución de procesos
- Conexiones de red

Estos eventos se registran en logs generados por:

- Sistemas operativos
- Firewalls
- Aplicaciones
- Servicios en la nube

---

## Alertas

Una **alerta** se genera cuando una herramienta de seguridad detecta actividad sospechosa basada en los eventos registrados.

Las herramientas analizan grandes volúmenes de logs y activan alertas cuando se cumplen ciertas reglas de detección.

Ejemplos de alertas:

- Inicio de sesión desde una ubicación inusual
- Intentos de fuerza bruta
- Ejecución de software sospechoso
- Correos electrónicos de phishing detectados

Las alertas permiten que los analistas SOC se enfoquen en actividades potencialmente maliciosas.

---

# Plataformas de Gestión de Alertas

Los equipos SOC utilizan diferentes plataformas para gestionar e investigar alertas.

| Plataforma | Ejemplos | Función |
|---|---|---|
| SIEM | Splunk, Elastic | Recolección y análisis centralizado de logs |
| EDR / NDR | Microsoft Defender, CrowdStrike | Detección de amenazas en endpoints o red |
| SOAR | Cortex SOAR, Splunk SOAR | Automatización de procesos de seguridad |
| ITSM | Jira, TheHive | Gestión de tickets e incidentes |

Normalmente las alertas se centralizan en un **SIEM** para facilitar su análisis.

---

# Roles dentro de un SOC

## SOC Level 1 (L1)

Responsabilidades:

- Monitorizar alertas
- Realizar análisis inicial
- Identificar si la alerta es maliciosa
- Escalar incidentes a niveles superiores si es necesario

---

## SOC Level 2 (L2)

Responsabilidades:

- Investigación más profunda
- Respuesta a incidentes
- Contención de amenazas

---

## Ingenieros SOC

Responsabilidades:

- Crear reglas de detección
- Mantener la infraestructura del SIEM
- Optimizar alertas

---

## SOC Manager

Responsabilidades:

- Supervisar las operaciones del SOC
- Gestionar al equipo
- Evaluar el rendimiento del SOC

---

# Propiedades de una Alerta

Cada alerta contiene información que ayuda en la investigación.

| Propiedad | Descripción |
|---|---|
| Alert Time | Momento en que se generó la alerta |
| Alert Name | Nombre o descripción de la alerta |
| Severity | Nivel de gravedad |
| Status | Estado actual de la investigación |
| Verdict | Resultado final de la investigación |
| Assignee | Analista asignado |
| Description | Detalles del evento detectado |
| Fields | Información adicional relevante |

---

# Niveles de Severidad

La severidad indica la urgencia de la alerta.

| Nivel | Significado |
|---|---|
| Low | Actividad informativa |
| Medium | Actividad sospechosa |
| High | Probable actividad maliciosa |
| Critical | Amenaza crítica |

---

# Estado de la Alerta

Indica el progreso de la investigación.

| Estado | Significado |
|---|---|
| New | Alerta sin revisar |
| In Progress | Alerta en investigación |
| Closed | Investigación finalizada |

---

# Clasificación de Alertas

Al finalizar la investigación, la alerta se clasifica como:

| Clasificación | Significado |
|---|---|
| True Positive | Amenaza real |
| False Positive | Actividad legítima |

---

# Priorización de Alertas

Un SOC puede recibir **muchas alertas diariamente**, por lo que es importante priorizarlas.

## 1. Filtrar alertas

Primero se eliminan alertas:

- Ya investigadas
- Asignadas a otros analistas
- Duplicadas

Se investigan principalmente alertas **nuevas y no asignadas**.

---

## 2. Ordenar por severidad

Orden de prioridad:

1. Critical
2. High
3. Medium
4. Low

Las alertas más críticas deben investigarse primero.

---

## 3. Ordenar por tiempo

Las alertas más antiguas se investigan primero, ya que pueden indicar ataques en progreso.

---

# Proceso de Alert Triage

El **alert triage** es el proceso de analizar alertas para determinar su importancia y legitimidad.

Consta de tres fases principales.

---

# 1. Acciones Iniciales

Antes de comenzar la investigación:

- Asignar la alerta a uno mismo
- Cambiar el estado a **In Progress**
- Revisar la información básica de la alerta

Información clave:

- Nombre de la alerta
- Descripción
- Severidad
- Indicadores

---

# 2. Investigación

Durante esta fase se analiza la actividad sospechosa.

Preguntas clave:

## ¿Quién está involucrado?

- Usuario
- Equipo
- Sistema

---

## ¿Qué ocurrió?

Ejemplos:

- Inicio de sesión sospechoso
- Malware detectado
- Transferencia de datos anormal

---

## ¿Cuándo ocurrió?

Revisar la línea de tiempo del evento.

---

## Fuentes de investigación

Los analistas pueden consultar:

- Logs del SIEM
- Logs del endpoint
- Inteligencia de amenazas
- Incidentes anteriores

Muchas organizaciones utilizan **playbooks o runbooks** para guiar la investigación.

---

# 3. Acciones Finales

Después de investigar la alerta:

### Determinar el resultado

Opciones:

- True Positive
- False Positive

---

### Documentar la investigación

Se deben registrar:

- Pasos realizados
- Evidencia encontrada
- Conclusión

---

### Cerrar la alerta

Cambiar el estado a:

