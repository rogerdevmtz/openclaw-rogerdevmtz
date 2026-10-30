# Diseño de skills de Atlas para Roger
Fecha: 30 de octubre de 2026. Este diseño se versiona antes de crear las skills.

## 1. diario-bootcamp
**Qué hace:** transforma apuntes reales del bootcamp de Ingeniería de IA en una entrada de aprendizaje y crea un Google Doc mediante el Zapier ya conectado.
**Input:** fecha y puntos sobre lo aprendido, dificultad y siguiente paso. Atlas ya conoce el nombre Roger, el idioma español, Europe/Madrid y el contexto OpenClaw por USER.md; aplica el tono directo de SOUL.md, su identidad y los límites de AGENTS.md. TOOLS.md determina las acciones disponibles.
**Buen output:** título «Diario de Roger — AAAA-MM-DD — tema» y secciones Aprendido, Aplicación, Duda pendiente y Próximo paso. No inventa aprendizajes. Devuelve enlace e ID reales del Doc; nunca confunde un borrador con una creación.
**Por qué:** reduce la tarea repetitiva de convertir apuntes del bootcamp en notas utilizables. Un documento por entrada funciona con Create Document From Text sin exigir permisos nuevos para anexar contenido.
**Prueba real prevista:** aprendizaje de Roger sobre personalización de Atlas, diseño previo de skills y distinción entre instrucciones y acciones de Zapier durante esta entrega. Separar hechos comprobados de propuestas.

## 2. sesion-estudio
**Qué hace:** convierte una petición de estudio en un bloque de Google Calendar sin invitados.
**Input:** objetivo, fecha explícita, hora y duración; enlace de material opcional. USER.md aporta Europe/Madrid y contexto bootcamp; SOUL.md aporta brevedad; AGENTS.md obliga a preguntar si falta la fecha/hora; TOOLS.md fija calendario principal y acción disponible; IDENTITY.md mantiene la voz de Atlas.
**Buen output:** evento «Estudio de Roger — tema», descripción con objetivo, tareas y criterio de finalización, inicio y fin con offset correcto y sin invitados. Confirmación con ID/enlace real. Si faltan datos esenciales, pregunta antes de crear.
**Por qué:** evita repetir título, zona, estructura y límites cada vez que Roger reserva estudio. Usa exclusivamente Create Detailed Event.
**Prueba real prevista:** primero una petición incompleta para comprobar que Atlas pregunta sin crear; después un bloque de revisión de esta entrega con fecha/hora explícitas, autorizado como prueba del proyecto.

## Verificación y entrega
- Ejecutar doctor antes y después de personalizar; conservar su resultado real.
- Instalar las skills como workspace/skills/<nombre>/SKILL.md según la documentación de la versión instalada.
- Verificar descubrimiento y disponibilidad con OpenClaw.
- Probar con Atlas, conservar entrada, salida y resultados reales de Zapier sin secretos.
- No configurar APIs, OAuth, herramientas ni servicios nuevos.
- Publicar solo configuración curada, skills, diseño y evidencias saneadas en el repositorio existente; excluir config MCP, memoria privada, tokens y transcripciones ajenas.
- No marcar requisitos completos si la prueba está bloqueada.
