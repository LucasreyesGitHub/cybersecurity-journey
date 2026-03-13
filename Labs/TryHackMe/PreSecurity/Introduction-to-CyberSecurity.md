# Introduction to CyberSecurity

## Executive Summary

Este documento consolida los fundamentos técnicos adquiridos tras completar los módulos introductorios de TryHackMe:

- Careers in Cyber
- Introduction to Defensive Security
- Introduction to Offensive Security

El objetivo es establecer una base sólida sobre los dominios principales de la ciberseguridad, comprender la interacción entre equipos ofensivos y defensivos, y entender el flujo técnico de detección y explotación de vulnerabilidades en entornos reales.

---

# 1. Careers in Cyber

## Panorama General del Sector

La ciberseguridad es un dominio multidisciplinario que combina conocimientos técnicos, gestión de riesgos y respuesta operativa. Las principales áreas se agrupan en:

- Offensive Security
- Defensive Security
- Governance, Risk & Compliance (GRC)

Cada una cumple un rol específico dentro de la estrategia global de seguridad organizacional.

---

## Offensive Security (Red Team)

### Objetivo Técnico

Identificar vulnerabilidades técnicas explotables antes de que puedan ser utilizadas por actores maliciosos.

### Funciones Principales

- Evaluación de superficie de ataque
- Enumeración de servicios y activos
- Identificación de fallos de configuración
- Explotación controlada
- Escalamiento de privilegios
- Generación de reportes técnicos con evidencia

### Enfoque Metodológico

Se basa en marcos como:

- Reconocimiento activo y pasivo
- Modelado de amenazas
- Pruebas de penetración autorizadas

El objetivo no es “romper por romper”, sino evaluar impacto y riesgo real.

---

## Defensive Security (Blue Team)

### Objetivo Técnico

Detectar, analizar y responder ante actividades anómalas o maliciosas en sistemas y redes.

### Componentes Fundamentales

#### SOC (Security Operations Center)

Centro operativo responsable de:

- Monitoreo continuo
- Triage de alertas
- Investigación de incidentes
- Escalación y respuesta

#### SIEM (Security Information and Event Management)

Sistema que:

- Centraliza logs de múltiples fuentes
- Correlaciona eventos
- Genera alertas basadas en reglas
- Permite búsquedas forenses

#### Incident Response Lifecycle

1. Preparation  
2. Identification  
3. Containment  
4. Eradication  
5. Recovery  
6. Lessons Learned  

---

## Governance, Risk & Compliance (GRC)

Área enfocada en:

- Identificación y evaluación de riesgos
- Implementación de controles
- Cumplimiento normativo
- Políticas y auditorías de seguridad

Es el puente entre la estrategia empresarial y la seguridad técnica.

---

# 2. Introduction to Defensive Security

## Flujo Técnico de Detección

Actividad → Generación de Log → Ingesta en SIEM → Correlación → Alerta → Triage → Investigación → Respuesta

Cada etapa es crítica para reducir falsos positivos y detectar amenazas reales.

---

## Análisis de Logs

El análisis defensivo se basa en:

- Event IDs (Windows)
- Syslog (Linux)
- Logs de firewall
- Logs de autenticación
- Telemetría de endpoint

La capacidad de correlacionar múltiples fuentes es clave para confirmar un incidente.

---

## Indicadores de Compromiso (IoCs)

Ejemplos:

- Direcciones IP maliciosas
- Hashes de archivos
- Dominios sospechosos
- Comportamientos anómalos

El análisis no debe limitarse a IoCs estáticos, sino incluir detección basada en comportamiento.

---

## Habilidades Técnicas Fundamentales

- Interpretación de logs
- Identificación de patrones anómalos
- Priorización basada en severidad e impacto
- Documentación técnica clara
- Comunicación efectiva con equipos técnicos y no técnicos

---

# 3. Introduction to Offensive Security

## Ciclo Técnico de Ataque

Reconocimiento → Enumeración → Explotación → Escalamiento de Privilegios → Persistencia → Movimiento Lateral


### Reconocimiento

- OSINT
- Descubrimiento de activos
- Identificación de puertos y servicios

### Enumeración

- Versiones de software
- Usuarios
- Configuraciones expuestas

### Explotación

Uso de vulnerabilidades conocidas o malas configuraciones para obtener acceso.

### Post-Explotación

- Escalamiento de privilegios
- Recolección de credenciales
- Persistencia
- Exfiltración de datos

---

## Enfoque Ético

Las pruebas ofensivas deben:

- Tener autorización formal
- Definir alcance claro
- Documentar hallazgos con evidencia
- Proponer remediaciones técnicas

---

# Offensive vs Defensive: Enfoque Comparativo

| Offensive Security | Defensive Security |
|-------------------|-------------------|
| Identifica debilidades explotables | Detecta actividad maliciosa |
| Evalúa impacto potencial | Reduce tiempo de detección |
| Simula técnicas de adversario | Mitiga riesgos reales |
| Enfoque proactivo | Enfoque reactivo y preventivo |

Ambos enfoques son complementarios y necesarios para una postura de seguridad madura.

---

# Conclusiones Técnicas

Tras completar estos módulos:

- Comprendo la estructura operativa de un SOC.
- Entiendo el ciclo técnico básico de un ataque.
- Identifico cómo se generan y procesan alertas.
- Reconozco la importancia de la correlación de eventos.
- Entiendo la diferencia entre vulnerabilidad, amenaza e incidente.
- Poseo una base conceptual sólida para profundizar en análisis de incidentes y threat hunting.

---

# Próximos Objetivos Técnicos

- Profundizar en análisis de eventos Windows (Event IDs críticos).
- Practicar triage de alertas en entornos controlados.
- Estudiar MITRE ATT&CK para mapear técnicas adversarias.
- Desarrollar proyectos prácticos enfocados en detección y respuesta.
- Construir un home lab para generar y analizar logs reales.

---




