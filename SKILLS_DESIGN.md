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
# Ampliación: skills productivas para estudiantes
Fecha: 2026-10-30. Sustituye la selección principal de diario y agenda por dos skills de apoyo a entregas y comprensión, a petición de Roger. Las dos primeras se conservan como utilidades existentes.

## radar-entrega
1. **Qué hace:** convierte un enunciado y el estado real del trabajo en un mapa de criterios, evidencia faltante y próxima acción priorizada.
2. **Input:** enunciado completo pegado o archivo local y avances/evidencias aportados. Fecha límite y tiempo disponible son opcionales para priorizar; no se inventan. Los cinco archivos aportan identidad Atlas, español directo, contexto Roger/4Geeks, privacidad y conexión Docs.
3. **Buen output:** veredicto honesto (listo, faltan evidencias, falta trabajo o información insuficiente), matriz criterio/estado/evidencia/siguiente acción, tres prioridades como máximo y una acción inmediata. Distingue ausencia de evidencia de incumplimiento. Puede crear un Doc con petición de guardar; devuelve ID real. No promete una nota.
**Razón:** evita descubrir al final que una entrega funcional incumple la rúbrica. Roger pidió explícitamente respetar cada paso y evaluación.
**UX:** empieza por el estado y lo siguiente; pregunta solo por datos que bloquean. No hace que el estudiante rellene un formulario. En revisiones posteriores compara con el estado anterior disponible.
**Prueba real:** rúbrica actual de Mi Agente, A Mi Manera, diseño ya commiteado, cinco archivos personalizados, diagnóstico sin errores y skills descubiertas. Debe señalar que faltan las pruebas de las nuevas skills y publicación, sin certificar todo completo.

## tutor-rescate
1. **Qué hace:** transforma un bloqueo concreto del bootcamp en una práctica adaptativa breve con diagnóstico, pistas graduadas y comprobación final.
2. **Input:** concepto o ejercicio que bloquea, intento propio si lo hay y tiempo opcional (por defecto propuesta de 10 minutos, no compromiso). Usa contexto real de Roger, tono Atlas, herramientas y límites de los cinco archivos.
3. **Buen output:** un microejercicio diagnóstico, revisión del intento con evidencia, pistas progresivas y ejercicio de transferencia. Al cerrar, resumen separando habilidad demostrada de pendiente; guarda Doc solo a petición y con ID real. No afirma dominio por asentimiento.
**Razón:** resumir no demuestra comprender; una respuesta propia permite dirigir el repaso a la dificultad real.
**UX:** un ejercicio cada vez, opción «pista», «ejemplo» o «voy con prisa», salida fácil con «cerrar». No encadena preguntas ni revela la solución antes del intento salvo petición.
**Prueba real:** distinguir SKILL.md, herramientas Zapier y configuración de Atlas en este proyecto; ejecutar inicio y una respuesta concreta para observar adaptación. Una respuesta de prueba elaborada por el asistente se identifica como tal, nunca como demostración de Roger.

## Límites y aceptación
- Mismo entorno y conexiones. Sin OAuth/API nueva, sin automatizaciones periódicas.
- Diseño commiteado antes de implementar estas nuevas skills.
- Estructura válida, descubrimiento OpenClaw y pruebas reales registradas.
- Al menos una salida nueva creada por la skill en Docs, con evidencia del resultado real; separar respuesta del agente de comprobación independiente.
- No publicar secretos, memoria ni resultados completos del runtime.
