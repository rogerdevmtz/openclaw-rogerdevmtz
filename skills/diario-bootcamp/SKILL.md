---
name: diario-bootcamp
description: Convierte apuntes de Roger sobre su bootcamp de Ingeniería de IA en una entrada estructurada y crea un Google Doc mediante el Zapier existente. Úsala para registrar aprendizaje; no para inventar experiencias ni modificar documentos existentes.
metadata: {"openclaw":{"requires":{"bins":["mcporter"]}}}
---

# Diario de aprendizaje de Roger

Aplica IDENTITY.md, SOUL.md, AGENTS.md, USER.md y TOOLS.md ya presentes en contexto; lee los que falten. Conserva la voz directa y práctica de Atlas, español, el contexto bootcamp y la privacidad de Roger.

Recibe fecha, tema y apuntes en lenguaje natural. Si no hay apuntes reales, pide esos datos; no los sustituyas por una historia inventada. Puedes usar la fecha actual en Europe/Madrid si no se especifica, indicándola. No conviertas una duda en aprendizaje resuelto.

Estructura:
- Título: Diario de Roger — AAAA-MM-DD — tema.
- Aprendido: hechos aportados por Roger.
- Aplicación: utilidad concreta en su proyecto; marca propuestas como propuestas.
- Duda pendiente: conserva las dudas indicadas; si no existen, dilo.
- Próximo paso: acción pequeña comprobable, diferenciando recomendación de compromiso.

Cuando Roger pida guardar o crear el diario, crea un nuevo Doc con la acción habilitada. Si solo pide un borrador, devuelve el texto sin crear.
Desde el workspace, usa mcporter con el servidor zapier. Inspecciona acciones habilitadas y el esquema de google_docs_create_document_from_text. Resuelve parámetros según ese esquema y llama execute_zapier_write_action con esa acción y los parámetros requeridos. No actives herramientas ni configures OAuth. Usa la conexión existente y la ubicación predeterminada, sin compartir ni mover archivos.

No crees más de un documento por solicitud. Ante timeout, no reintentes automáticamente. Para confirmar éxito exige un resultado real con ID o enlace; si faltan, comunica que no está verificado. No afirmes lectura independiente del Doc si solo tienes el resultado de creación. Devuelve título, enlace/ID y un siguiente paso breve, firmado Atlas 🤖.
