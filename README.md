# Mi Agente, A Mi Manera

**Roger · Bootcamp de Ingeniería de IA · 4Geeks Academy**

Este proyecto adapta mi asistente Atlas a dos necesidades del estudiante: revisar una entrega antes de enviarla y superar un bloqueo al estudiar. Continúa sobre la misma VPS, el mismo repositorio y las conexiones existentes de OpenClaw, Telegram y Zapier.

## Mis dos skills

| Skill | Para qué sirve | Cómo se usa |
| --- | --- | --- |
| **Radar de entrega** | Compara el enunciado con el trabajo disponible, identifica evidencias faltantes y propone el siguiente paso. | «Revisa esta entrega y dime qué falta». |
| **Tutor de rescate** | Plantea un ejercicio corto, revisa la respuesta y adapta las pistas. | «No entiendo este concepto; tengo diez minutos». |

Radar puede guardar el informe en Google Docs. Tutor admite «pista», «ejemplo», «voy con prisa» y «cerrar»; guarda un resumen solo cuando se solicita.

## Personalización de Atlas

- **IDENTITY.md:** nombre Atlas y símbolo 🤖.
- **SOUL.md:** tono natural, claro y breve; iniciativa en tareas reversibles.
- **AGENTS.md:** privacidad, límites y preguntas cuando faltan datos esenciales.
- **USER.md:** mi contexto de estudiante, preferencias y zona Europe/Madrid.
- **TOOLS.md:** conexiones disponibles, acciones permitidas y valores por defecto.

La configuración activa y las skills están en `~/.openclaw/workspace/`. Se conservan también dos utilidades iniciales: diario de aprendizaje y reserva de estudio.

## Diseño y comprobaciones

El diseño de las dos skills principales está en el commit `826beb6`, anterior a su implementación en `32cf491`.

- Las skills pasan la validación de estructura y OpenClaw las reconoce como disponibles.
- El diagnóstico final devuelve `ok: true`, con 36 comprobaciones y cero errores.
- Radar creó un único documento y su contenido se comprobó por separado en Google Docs.
- Tutor tiene pruebas de inicio, corrección y práctica guiada con ejercicio de transferencia.
- No se añadieron APIs, OAuth ni servicios.

El diagnóstico completo inicial mostró dos advertencias previas sobre acceso de nodos y secretos en la configuración. El resultado sin errores no implica ausencia de advertencias.

## Entrega

- [Diseño de las skills](SKILLS_DESIGN.md).
- [Pruebas y resultados](PRUEBAS.md).
- [Correspondencia con la evaluación](EVALUACION.md).
- [Estado final y límites](CIERRE.md).

La configuración privada de Zapier, las credenciales y la memoria personal quedan fuera de esta entrega.

Referencias: [skills de OpenClaw](https://docs.openclaw.ai/tools/skills) y [workspace](https://docs.openclaw.ai/concepts/agent-workspace).
