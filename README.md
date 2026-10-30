# Mi Agente, A Mi Manera — Atlas para Roger

Entrega del bootcamp de Ingeniería de IA de 4Geeks Academy. Se amplía el mismo Atlas en la VPS y el mismo repositorio; no se reinstala OpenClaw ni se añaden APIs, OAuth o conexiones.

## Diseño anterior a implementación

El commit `a85f2bb` contiene SKILLS_DESIGN.md antes de cualquier archivo de skill. El commit `d3b68c7` personaliza los cinco archivos. La configuración activa vive en `~/.openclaw/workspace/`: es el workspace que carga esta instalación, dentro de `.openclaw`. No se duplica en una ruta que el runtime no lea.

## Personalización

- IDENTITY.md: Atlas 🤖, asistente de Roger para aprender y ejecutar proyectos de IA.
- SOUL.md: español directo, iniciativa en tareas reversibles, dudas explícitas y comprobación de resultados.
- AGENTS.md: privacidad, preguntas ante datos esenciales ausentes, límites de acciones externas y protección contra duplicados. Se conservaron las convenciones existentes.
- USER.md: contexto real de Roger, bootcamp, entrega actual, preferencias y zona Europe/Madrid.
- TOOLS.md: exclusivamente Docs y Calendar conectados mediante Zapier MCP y el canal Telegram existente. Documenta valores por defecto y operaciones no disponibles.

## Dos skills instaladas

1. `skills/diario-bootcamp/SKILL.md`: convierte apuntes en un Google Doc nuevo, sin atribuir aprendizajes inventados. Un documento por entrada permite usar la acción disponible sin añadir permisos de edición.
2. `skills/sesion-estudio/SKILL.md`: reserva estudio con objetivo, pasos y criterio de finalización. Pregunta si faltan horarios; no añade invitados ni presume disponibilidad.

Se eligieron porque ayudan a Roger a documentar el bootcamp y convertir próximos pasos en tiempo de estudio. Cada una aplica identidad, tono, límites, contexto y herramientas de los cinco archivos.

## Comprobaciones

- Ambas skills pasan `quick_validate.py` de skill-creator.
- OpenClaw las descubre como `openclaw-workspace`, `eligible: true`, `modelVisible: true`, sin requisitos faltantes. Ver JSON de descubrimiento en `evidencias/skills/`.
- Tras editar los cinco archivos: `openclaw doctor --lint --severity-min error --json` devuelve `ok: true`, 36 comprobaciones y ningún error. El diagnóstico completo inicial informó dos advertencias preexistentes sobre acceso de nodos y secretos en configuración; el resultado filtrado no pretende afirmar que no existen advertencias.
- Los resultados de pruebas reales se documentan en PRUEBAS.md una vez terminados. No se consideran cumplidos por la mera validación de archivos.

## Uso desde Atlas

- «Guarda en mi diario de hoy estos apuntes del bootcamp: …»
- «Reserva estudio de OpenClaw el [fecha] a las [hora], durante [duración]».

Los puntos suspensivos y corchetes son instrucciones de uso, no los datos de las pruebas. Las entradas reales se conservan en las evidencias.

## Reproducibilidad y privacidad

Ejecutar desde el workspace activo. La configuración privada de mcporter continúa en `config/` de la VPS y se excluye del repositorio; quien clone necesita su propia instalación y conexiones previas. No se incluye ningún token, clave ni exportación de configuración. Los resultados completos del runtime quedan privados; la entrega usa resúmenes saneados.

Referencias: [Skills de OpenClaw](https://docs.openclaw.ai/tools/skills), [workspace del agente](https://docs.openclaw.ai/concepts/agent-workspace). Se contrastó además la documentación local de la versión instalada 2026.10.7.
