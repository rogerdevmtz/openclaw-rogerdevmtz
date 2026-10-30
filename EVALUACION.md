# Correspondencia con la evaluación

| Criterio | Dónde comprobarlo |
| --- | --- |
| Cinco archivos específicos | IDENTITY.md, SOUL.md, AGENTS.md, USER.md y TOOLS.md del workspace activo |
| Diagnóstico sin errores | evidencias/skills/doctor-configuracion.json y doctor-final.json; se documentan aparte las advertencias preexistentes |
| Diseño anterior a implementación | SKILLS_DESIGN.md: commits a85f2bb → ff511ce para las utilidades iniciales y 826beb6 → 32cf491 para las principales |
| Dos skills de OpenClaw correctas | skills/radar-entrega/SKILL.md y skills/tutor-rescate/SKILL.md; JSON de descubrimiento con eligible y modelVisible |
| Resultado real en servicio conectado | PRUEBAS.md: informe de Radar en Docs, ID real y comprobación independiente; además se conserva el diario inicial |
| Sin API ni OAuth nuevos | Misma VPS, OpenClaw, Zapier y cuenta ya conectada; TOOLS.md limita las operaciones existentes |
| Personalización visible | Atlas 🤖, español breve, contexto de Roger y 4Geeks, rúbrica real, privacidad, preguntas ante datos esenciales ausentes |
| Razonamiento de cada skill | SKILLS_DESIGN.md explica utilidad, input y buen output; README.md explica uso y límites |
| Pruebas con contexto real | Entradas de evidencias/skills y respuestas saneadas en PRUEBAS.md; los intentos simulados del tutor están identificados |
| Entrega en GitHub | Repositorio original rogerdevmtz/openclaw-rogerdevmtz, con historial de diseño e implementación |

## Cómo explicarlo en clase

**Radar** resuelve un problema de Roger: saber si su trabajo cumple lo que se evalúa. Necesita enunciado y evidencia; devuelve un diagnóstico trazable y una acción concreta. No confunde falta de evidencia con un fallo y no promete una nota.

**Tutor** ayuda a comprender un concepto a partir de una respuesta propia. Necesita el bloqueo y, si existe, un intento; devuelve un ejercicio cada vez y ajusta las pistas. No toma un «sí» como prueba de aprendizaje.

Ambas usan conversación breve y controles sencillos. Guardan un documento solo cuando se pide, usando la conexión existente. El detalle de evaluación se conserva aunque el chat sea conciso.
