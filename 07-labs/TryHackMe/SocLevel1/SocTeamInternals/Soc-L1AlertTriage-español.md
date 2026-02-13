# SOC L1 — Alert Triage (Notas)

## Objetivo

Comprender cómo un analista de un Security Operations Center (SOC) Nivel 1 gestiona las alertas desde su detección hasta su cierre.

---

## ¿Qué es una alerta?

Una alerta es una notificación generada por herramientas de seguridad cuando se detecta actividad sospechosa en los logs del sistema.

**Flujo básico:**

```
Evento → Log → SIEM/EDR → Detección → Alerta
```

Sin alertas, los analistas tendrían que revisar manualmente enormes volúmenes de logs.

---

## Rol de un Analista SOC L1

Los analistas SOC L1 son la primera línea de defensa. Su responsabilidad principal es revisar las alertas y determinar si representan amenazas reales.

**Responsabilidades dentro del SOC:**

* **Analista L1:** Revisa alertas y escala incidentes críticos.
* **Analista L2:** Realiza investigaciones más profundas y ejecuta la remediación.
* **Ingenieros de Seguridad:** Configuran reglas de detección y mejoran la calidad de las alertas.
* **SOC Manager:** Supervisa la eficiencia del triage y la calidad operativa.

---

## Propiedades Clave de una Alerta

Antes de comenzar una investigación, es fundamental comprender los principales campos de la alerta:

* **Alert Time:** Cuándo ocurrió el evento.
* **Alert Name:** Tipo de actividad detectada.
* **Severity:** Nivel de riesgo (Low → Critical).
* **Status:** New, In Progress, Closed.
* **Verdict:** True Positive o False Positive.
* **Assignee:** Responsable de la alerta.
* **Description:** Contexto del evento.
* **Additional Fields:** Datos técnicos para un análisis más profundo.

---

## Priorización de Alertas

Cuando se manejan grandes volúmenes de alertas:

1. Enfocarse en las alertas nuevas.
2. Ordenarlas por severidad (primero las críticas).
3. Atender primero las alertas más antiguas.

Las alertas de mayor severidad suelen tener más probabilidades de ser amenazas reales.

---

## Proceso de Alert Triage

### Acciones Iniciales

* Asignarte la alerta.
* Cambiar el estado a **In Progress**.
* Revisar el nombre de la alerta, la descripción y los indicadores.

---

### Investigación (Fase Central)

Buenas prácticas:

* Identificar qué activo está en riesgo (usuario, host, red, etc.).
* Comprender la actividad sospechosa.
* Revisar eventos ocurridos antes y después de la alerta.
* Validar los hallazgos utilizando fuentes de threat intelligence.

Muchas organizaciones utilizan **playbooks** o **runbooks** para estandarizar las investigaciones y mejorar la consistencia en la respuesta.

---

### Acciones Finales

Determinar si la alerta es:

* **True Positive:** Amenaza real de seguridad.
* **False Positive:** Actividad legítima marcada incorrectamente como maliciosa.

Documentar claramente la investigación y cerrar la alerta siguiendo los procedimientos establecidos.

---

## Idea Clave

Identificar correctamente una amenaza es solo el comienzo. La práctica constante, la documentación clara y el seguimiento de los procesos de escalación son esenciales para convertirse en un analista SOC efectivo.
