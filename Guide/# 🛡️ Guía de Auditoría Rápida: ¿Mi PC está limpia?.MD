# 🛡️ Guía de Auditoría Rápida: ¿Mi PC está limpia?

Esta guía está diseñada para que cualquier persona, sin conocimientos previos en ciberseguridad, pueda verificar si su computadora tiene comportamientos sospechosos o posibles vulnerabilidades tras un reinicio inesperado o actividad inusual (como ventanas de terminal abriéndose solas).

---

## 1. Primeros Pasos: Observación del Sistema

Antes de usar herramientas complejas, observa el comportamiento de tu equipo. Si notas cambios en la resolución de pantalla o terminales que se abren, no entres en pánico, pero actúa de inmediato.

### Identificación de Procesos Extraños
1. Presiona `Ctrl + Shift + Esc` para abrir el **Administrador de Tareas**.
2. Ve a la pestaña **Detalles**.
3. Busca procesos con nombres aleatorios (ej. `ax39v.exe`) o que no tengan descripción ni icono oficial.

---

## 2. Auditoría de Red Local (Netstat)

Un atacante o un malware suele necesitar "escuchar" conexiones externas. Podemos ver qué "puertas" (puertos) tiene abiertas tu PC con un comando sencillo.

### Cómo hacerlo:
1. Abre el **Buscador de Windows**, escribe `cmd` y ejecútalo como **Administrador**.
2. Escribe el siguiente comando y presiona Enter:
   `netstat -ano | findstr LISTENING`

### Cómo leer los resultados:
Verás una lista con columnas. Fíjate en la última columna, llamada **PID** (Identificador de Proceso).

*   **Puertos Comunes (Normales):**
    *   **135, 445:** Servicios del sistema de Windows para compartir archivos.
    *   **5357:** Detección de dispositivos e impresoras en red.
    *   **7680:** Optimización de entrega de Windows Update (común tras reinicios).
*   **Puertos Altos (49000+):** Suelen ser servicios internos de Windows comunicándose entre sí.

**⚠️ Acción Clave:** Si ves un puerto extraño, busca su **PID** en la pestaña **Detalles** del Administrador de Tareas para saber qué programa exacto lo está usando.

---

## 3. Protocolo de Limpieza Profunda

Si sospechas que hay algo mal, sigue este orden de escaneo:

1.  **Examen de Microsoft Defender sin conexión:** 
    *   Ve a *Configuración > Privacidad y seguridad > Seguridad de Windows > Protección contra virus y amenazas*.
    *   Elige **Opciones de examen** > **Examen de Microsoft Defender sin conexión**. 
    *   *¿Por qué?* Esto reinicia el PC y busca virus antes de que el malware pueda "esconderse" al arrancar Windows.
2.  **Reparación de Archivos del Sistema:**
    *   En la terminal (CMD) como administrador, ejecuta:
        `sfc /scannow`
    *   Esto reparará archivos que el malware pudo haber dañado para cambiar el "look" de tu sistema.

---

## 4. Recomendaciones de Ciberseguridad Proactiva

Para mantener tu equipo seguro mientras aprendes más sobre defensa (SOC):

*   **Higiene de Inicio:** En el Administrador de Tareas, ve a la pestaña **Inicio** y deshabilita todo lo que no sea estrictamente necesario.
*   **Actualizaciones:** No ignores los reinicios de Windows Update; a menudo parchean vulnerabilidades críticas.
*   **Cuidado con los Scripts:** Si estudias programación o usas herramientas como Python, verifica siempre el origen de los scripts que ejecutas, ya que suelen abrir terminales que parecen ataques pero son procesos locales.
*   **Uso de Gestores de Contraseñas:** Si sospechas de una brecha, cambia tus credenciales desde un dispositivo distinto (como tu móvil).

---
*Esta guía forma parte de mis laboratorios de aprendizaje en Ciberseguridad.*
