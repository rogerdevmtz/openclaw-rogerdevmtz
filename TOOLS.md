# Herramientas reales de Atlas

## Entorno
El workspace activo es ~/.openclaw/workspace en la VPS existente. Ejecuta mcporter desde este directorio: su configuración está en config/ y no debe publicarse. Nunca copies credenciales al repositorio.

## Zapier MCP existente
Servidor mcporter: zapier. Comprobado el 30/10/2026. Solo Google Docs y Google Calendar tienen acciones habilitadas; no confundas las herramientas administrativas del servidor con permisos para otras apps.

Antes de ejecutar: `mcporter call zapier.inspect_zapier_actions`; inspecciona la app, la acción y su esquema. Usa exclusivamente la conexión predeterminada ya existente. Resuelve enums dinámicos con inspect y usa los identificadores retornados; no inventes claves de parámetros.

- Google Docs: Create Document From Text. Crear un documento nuevo por entrada de diario; no asumir que puedes leer, anexar, mover o compartir. Carpeta: ubicación predeterminada de la acción, sin inventar un ID. Español, título «Diario de Roger — AAAA-MM-DD — tema».
- Google Calendar: Create Detailed Event. Calendario principal de la conexión existente, resuelto desde las opciones de la acción. Zona Europe/Madrid. Sin invitados, sin recurrencia ni avisos añadidos salvo petición. Solicita fecha, hora y duración si faltan. Calcula el offset con la fecha, no con una constante.
- Telegram: canal de conversación ya emparejado con Atlas. No publicar en grupos ni enviar a otros destinatarios sin instrucción explícita.
- Gmail, Drive y Tasks: no hay acciones habilitadas verificadas. No usarlos ni activar nada para esta entrega. No hay firma de Gmail configurada.

Si una acción devuelve error o una respuesta ambigua, informa; no repitas creaciones automáticamente. Conserva ID y enlace reales para la verificación, sin guardar tokens, cabeceras ni datos ajenos.

### Creación de Docs: firma comprobada

Tras inspeccionar la acción actual, el servidor usa `execute_zapier_write_action` con `selected_api`, `action`, `tool_name` y `params`. En esta instalación los valores verificados son `GoogleDocsV2CLIAPI`, `newtxtdocument` y `google_docs_create_document_from_text`; `params` contiene `title` y `file`. Si el catálogo cambia, usa los valores que devuelva la inspección actual.

Para contenido largo, escribe los argumentos JSON en un archivo temporal privado y usa `mcporter call zapier.execute_zapier_write_action --args "$(cat /ruta/temporal.json)"`. No construyas el JSON concatenando texto del usuario en un comando. No necesitas listar el esquema de todo el servidor para cada creación. Reutiliza la firma ya verificada mientras siga vigente.
