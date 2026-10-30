# Resultado final de las pruebas

Las dos skills principales se probaron en Atlas sobre el proyecto real de Roger. El informe de Radar se creó una sola vez mediante el Zapier existente y se comprobó por separado en Google Docs. Tutor inició una práctica y corrigió un intento erróneo identificado como simulación del asistente.

## Radar: creación y comprobación independiente

- Documento: [Radar de entrega de Roger](https://docs.google.com/document/d/19nC97xH1C-sSDuTjX-JkzduX138qZXxxPybwws5D4PE/edit).
- `evidencias/skills/radar-zapier-creacion.json` conserva solo los metadatos necesarios de la respuesta real: ID, título, URL, fecha, `shared: false` y salida exitosa.
- Se comprobó el registro completo de esta sesión, incluidos eventos comprimidos: una sola llamada de creación. El primer timeout ocurrió antes de escribir; la continuación creó el documento y una repetición interna posterior evitó duplicarlo.
- Se abrió el Doc en Chrome con la cuenta conectada. La interfaz confirmó «Guardado en Drive» y «Privado, solo para mí». Se revisó la página y se exportó el contenido guardado mediante la interfaz del navegador: `radar-doc-exportado.md`. Contiene estado, alcance, diez criterios, evidencia, prioridades y siguiente acción. `radar-verificado.jpg` muestra el resultado visible.
- `radar-respuesta-inicial.md` conserva la respuesta del turno que creó el Doc. La respuesta posterior, reproducida más abajo, detectó la creación anterior y no volvió a escribir.

## Cómo interpretar el informe

El Doc es una fotografía del estado durante la prueba, anterior a las evidencias finales y al push. Sus «pendientes» no son el estado final del repositorio. En particular: ahora existe salida real de Radar y lectura independiente; Tutor tiene inicio y seguimiento; el diagnóstico final se conserva aparte; GitHub se verifica al publicar. No se ha alterado la salida de prueba para hacerla parecer perfecta.

Hay dos limitaciones registradas: Radar reutilizó evidencia antigua al redactar algunos estados, y su respuesta posterior fue contradictoria al decir que faltaba una salida válida pese al ID recuperado. La comprobación de Zapier y del Doc resuelve esa contradicción; no se toma el texto del agente como única fuente. La prueba sigue demostrando revisión de rúbrica, creación real y prevención de duplicados.

## Tutor: comportamiento observado

La primera respuesta planteó un único microejercicio y esperó un intento. La segunda corrigió la confusión entre skill, herramientas y acción; dio una pista y un solo siguiente paso. Los inputs y las respuestas aparecen debajo. El intento es una simulación de validación; no se presenta como aprendizaje ni respuesta de Roger.

## Conexiones y privacidad

No se añadieron APIs, OAuth ni servicios durante este proyecto. Se reutilizó el servidor Zapier ya existente de la entrega anterior, limitado a Docs y Calendar; Radar solo usó la acción de Docs. No se publican tokens, configuración MCP, memoria privada ni resultados completos del runtime. El informe de Docs permanece privado: el repositorio contiene su exportación saneada para que el evaluador no dependa de permisos de acceso.

---

# Pruebas reales de Atlas

Fecha: 30/10/2026. Se conservan los mensajes de entrada en evidencias/skills. Las respuestas siguientes son resultados del agente; la lectura independiente de documentos se registra aparte.

## diario

Estado del runtime: ok

Creé **una única entrada** en Google Docs. El documento figura en el Drive personal de Roger y la respuesta de creación indica que no está compartido.

- **Título:** Diario de Roger — 2026-10-30 — Personalización de Atlas y diseño de skills
- **ID:** `1uUMQjnbd5k_l_09PVsQuUCg99ZGnPml9UV6Y7mqEbtA`
- **Enlace:** https://docs.google.com/document/d/1uUMQjnbd5k_l_09PVsQuUCg99ZGnPml9UV6Y7mqEbtA/edit
- **Verificación:** creación confirmada por Zapier con ID y enlace reales. No hice una lectura independiente del contenido; esa revisión queda pendiente para Roger antes de entregar.

Atlas 🤖

## sesion

Estado del runtime: ok

Para continuar necesito que me indiques **la fecha, la hora de inicio y la duración**. Interpretaré la hora en **Europe/Madrid**. No he creado ningún evento ni enviado mensajes ni configurado conexiones.

Borrador: **Estudio de Roger — revisión de Mi Agente, A Mi Manera**. Objetivo: revisar la entrega y comprobar las evidencias de las dos skills. **Criterio de finalización:** revisar ambas evidencias y dejar identificados los resultados y cualquier pendiente.

Atlas 🤖

## radar

Estado del runtime: ok

Roger, recuperé la revisión y no voy a crear otro Doc: en el historial de esta misma sesión consta una creación exitosa con ID y enlace. Repetirla dejaría dos informes. **Ese documento no incluye la actualización reciente sobre el seguimiento del tutor**, y la acción de creación habilitada no permite actualizarlo; por eso no puedo presentarlo como la versión revisada con esa evidencia nueva.

- [Informe ya creado en Google Docs](https://docs.google.com/document/d/19nC97xH1C-sSDuTjX-JkzduX138qZXxxPybwws5D4PE/edit) · ID: `19nC97xH1C-sSDuTjX-JkzduX138qZXxxPybwws5D4PE`.
- **Estado breve: faltan evidencias y trabajo.** Los cinco archivos existen; el doctor posterior devuelve `ok=true` y sin errores, sin que eso permita afirmar que no haya advertencias. El diseño de radar y tutor está commiteado antes de su implementación.
- `tutor-rescate` ya tiene evidencia de inicio y de corrección adaptativa ante un intento **simulado**; no demuestra conocimientos de Roger. La publicación en GitHub sigue pendiente.
- La salida de Docs registrada es de `diario-bootcamp`, una utilidad conservada, no de las nuevas principales. El resultado del radar continúa sin evidencia de salida válida. No se ha hecho lectura independiente del Doc de diario ni del informe ya creado.
- En esta ejecución no se habilitó nada ni se configuró OAuth; no inspeccioné `config/`, así que no certifico el historial completo de conexiones. Atlas 🤖

## tutor

Estado del runtime: ok

Objetivo: distinguir dónde vive cada parte de la personalización de Atlas y cómo se conecta con una operación concreta. **Microejercicio:** imagina que Atlas debe saber *cómo* crear una nota de estudio, *qué herramientas de Zapier tiene disponibles* y luego crear un documento en Google Docs. ¿Qué responsabilidad asignarías a **SKILL.md**, **TOOLS.md** y a la **acción de Zapier**, respectivamente? Explica brevemente por qué.

Puedes decir **pista**, **ejemplo**, **voy con prisa** o **cerrar**. Esperaré tu intento; no crearé documentos ni ejecutaré acciones de escritura.

## tutor-seguimiento

Estado del runtime: ok

Este intento **simulado** confunde los papeles: las credenciales no deben guardarse en `SKILL.md`; el procedimiento del diario corresponde a la skill, y una acción de Zapier ejecuta una operación, pero no decide qué aprendiste.

**Pista:** separa las instrucciones que guían a Atlas, la descripción de herramientas disponibles y la operación que crea el documento.

**Siguiente paso:** vuelve a asignar esas tres responsabilidades a `SKILL.md`, `TOOLS.md` y la acción de Zapier, respectivamente.

## Alcance

- Los turnos del tutor son pruebas del asistente sobre el proyecto real de Roger; no prueban el nivel de conocimientos de Roger.
- La prueba de sesión incompleta verifica que se solicitan datos en vez de inventar una reserva; no acredita creación de un evento.
- Las respuestas de creación no equivalen a lectura independiente del contenido.
- Las validaciones de estructura y descubrimiento no equivalen a pruebas de comportamiento.
