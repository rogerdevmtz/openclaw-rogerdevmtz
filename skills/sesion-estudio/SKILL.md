---
name: sesion-estudio
description: Reserva en Google Calendar una sesión de estudio de Roger con objetivo y criterio de finalización, usando la conexión Zapier existente. Pregunta por fecha, hora o duración ausentes; no gestiona reuniones con invitados ni recurrencias.
metadata: {"openclaw":{"requires":{"bins":["mcporter"]}}}
---

# Sesión de estudio para Roger

Aplica los cinco archivos del workspace: IDENTITY.md, SOUL.md, AGENTS.md, USER.md y TOOLS.md. Lee solo los que falten en contexto. Usa el español directo de Atlas, objetivos prácticos del bootcamp de Roger y sus límites de privacidad.

Requiere objetivo, fecha inequívoca, hora y duración. Pregunta en un único mensaje por los datos esenciales ausentes antes de cualquier escritura. «Por la tarde» no es una hora. No deduzcas disponibilidad a partir de una acción que solo puede crear eventos. Si existe una referencia relativa, conviértela a fecha explícita con Europe/Madrid y comunícala.

Propón contenido útil y breve:
- Título: Estudio de Roger — tema.
- Descripción: objetivo, pasos y criterio de finalización observable.
- Material: enlace proporcionado, si existe.
No añadas asistentes, recurrencias ni recordatorios sin una petición. No envíes mensajes a terceros.

Para una petición explícita de reserva, usa solo Google Calendar Create Detailed Event ya habilitada. Desde el workspace, inspecciona el catálogo Zapier con mcporter, el esquema de google_calendar_create_detailed_event y las opciones dinámicas de calendario. Selecciona el calendario principal de la conexión existente; pregunta si no puede identificarse. Calcula inicio/fin con Europe/Madrid y el offset correspondiente a esa fecha. Si el usuario pide comprobar conflictos, explica que esa lectura no está habilitada y pide decisión antes de reservar.

Ejecuta execute_zapier_write_action con el nombre y parámetros obtenidos del esquema, sin activar otras acciones ni nuevas conexiones. No inventes identificadores ni campos. Crea un solo evento por solicitud y no repitas automáticamente tras un timeout.

Confirma únicamente a partir del resultado real: título, fecha, inicio/fin, Europe/Madrid, calendario, sin invitados e ID/enlace. Si solo se solicitó propuesta o faltan datos, devuelve el borrador o la pregunta e indica que no se creó evento. Firma Atlas 🤖.
