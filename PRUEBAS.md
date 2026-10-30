# Pruebas y resultados

**Fecha: 30 de octubre de 2026.** Las pruebas usan el proyecto «Mi Agente, A Mi Manera» y sus requisitos reales.

## Radar de entrega

**Entrada:** enunciado, criterios de evaluación y avances del repositorio.

**Resultado:** informe con diez criterios, estado, evidencias, prioridades y siguiente acción. Se creó una única copia mediante la conexión existente de Zapier.

- [Documento en Google Docs](https://docs.google.com/document/d/19nC97xH1C-sSDuTjX-JkzduX138qZXxxPybwws5D4PE/edit).
- [Respuesta de creación](evidencias/skills/radar-zapier-creacion.json): ID real, salida exitosa y `shared: false`.
- [Contenido exportado del documento](evidencias/skills/radar-doc-exportado.md), comprobado después desde Chrome.
- [Captura del resultado](evidencias/skills/radar-verificado.jpg).
- [Respuesta inicial de Radar](evidencias/skills/radar-respuesta-inicial.md).

El informe refleja el estado durante la prueba, anterior a la publicación y al cierre. Algunos puntos ya están resueltos. Radar también reutilizó información antigua en una respuesta posterior; se ajustó la skill para priorizar resultados recientes y distinguir una creación de su comprobación independiente. El estado de la prueba posterior se registra en [CIERRE.md](CIERRE.md).

**Comprobación posterior:** Radar reconoció la creación del Doc y la publicación ya completadas. Distinguió los datos aportados de una inspección propia y no volvió a crear documentos. La [respuesta final](evidencias/skills/practica-final.md) conserva el resultado.

## Tutor de rescate

**Tema:** diferencia entre SKILL.md, TOOLS.md y una acción de Zapier.

| Prueba | Comportamiento observado |
| --- | --- |
| Inicio | Planteó un microejercicio, ofreció controles de ayuda y esperó una respuesta. |
| Corrección de un intento simulado | Detectó la confusión, explicó el error y dio una pista con un solo siguiente paso. |

Las [respuestas conservadas](evidencias/skills/tutor-practica.md) permiten revisar el comportamiento. Esta prueba valida la interacción; no acredita dominio del tema.

**Práctica guiada completada:** se presentó una explicación sobre las funciones de SKILL.md, TOOLS.md y Zapier. Tutor revisó la respuesta, añadió un matiz y propuso un ejercicio sobre qué hacer ante un timeout. Se conserva junto a la actualización de Radar en [practica-final.md](evidencias/skills/practica-final.md).

## Entorno

- [Diagnóstico final](evidencias/skills/doctor-final.json): `ok: true`, 36 comprobaciones y cero errores.
- [Radar disponible](evidencias/skills/radar-discovery.json) y [Tutor disponible](evidencias/skills/tutor-discovery.json): elegibles y sin requisitos faltantes.
- [Revisión de archivos para publicar](evidencias/skills/auditoria-publicacion.json): sin credenciales detectadas.
- [Gateway](evidencias/skills/gateway-final.txt): activo tras la comprobación.

Se utilizaron las conexiones previas. No se crearon APIs, OAuth, eventos ni automatizaciones nuevas para estas pruebas.
