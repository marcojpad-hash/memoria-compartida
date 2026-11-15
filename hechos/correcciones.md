# Correcciones

Lo que se corrigió y qué reemplaza. Un hecho viejo no se borra: se
marca como reemplazado.

- **La app de GitHub SÍ puede crear repos por API** si tiene el
  permiso `Repository creation`. Reemplaza: "la creación de repos no
  se puede automatizar". Lo que falta es el permiso, no la
  capacidad. (2026-11-08, investigación)
- **El motor SÍ tiene 8 workflows en GitHub Actions.** Reemplaza:
  "CAPCOT y el motor no tienen automatización". CAPCOT tiene cero.
  (2026-11-07, auditoría)
- **La cola CAPCOT tiene 16 paquetes**, no 14. (2026-11-08)
- **Free Claude Code: licencia por verificar.** La investigación
  decía MIT; el puente la leyó como AGPL v3. No copiar nada de FCC
  hasta verificar. (2026-11-08)
- **Cerebras NO es $0 permanente.** Desde 2026-07-16 es Free Trial
  con tarjeta, $5, 30 días. Reemplaza: "Cerebras gratis".
  (2026-11-08, investigación)
- **El texto del issue de escala está desactualizado**: dice que la
  creación de repos "no se puede automatizar". Ver la primera
  corrección de esta lista. (2026-11-08)

- **CAPCOT 5–7 nov — recuento de publicaciones preexistentes:** al 2026-11-13, la evidencia exacta por `project_id` enlaza cinco proyectos (Palomitas, Ranas, Aguacate, Ballena y Hielo), no siete. Los IDs globales de Venus y Arena no se pueden atribuir sin `project_id`/slot. Reemplaza el recuento preliminar de siete en la actualización CAPCOT del 2026-11-13 de `hechos/estado.md`. Fuente: `data/horario_2026-11-08.json` a `data/horario_2026-11-11.json` y `docs/briefs/2026-11-13_CONTROL_COLA.md` en `capcot-capsulas-imaginantes`, rama `feature/capcot-video-discovery-continuity`.

- **Auditoría ChatGPT sobre Mozart: los 5 hallazgos están corregidos (re-corrida FIX5 verificada 18/18).** Reemplaza: "efectividad_corte_retenido.estado=INTERNAL_T1_RUN_FAILED, previo_error=DATO_AUSENTE_REQUIERE_CLASIFICACION, CEB INCOMPLETE, Caldero FALLO DE EJECUCIÓN SIMULADO_FIXTURE". Ahora: estado=T1_COMPLETADO con hit_H=HIT_HIPOTESIS_SET (el KeyError 'creatividad' era del runner, no del motor: el visto era un caso pelado sin external_lights); previo_error=SIN_ERROR_CORRIDA_PREVIA_COMPLETADA; CEB VERIFIED_FLOW 77/77; Caldero INFO_FIXTURE_AUTORIZADO (fixture autorizado por contrato PATCH10); semantica_estados en el contrato de salida. H1/H2/apuesta idénticos al original. PR motor-u6-storage #14 (rama alterno/reconexion-2a1-correccion-auditoria-mozart → alterno/reconexion-2a1). (2026-11-14, re-corrida FIX5)
- **El código de la rama alterno/reconexion-2a1 NO reproducía el RESULT de Mozart del 13-nov.** Reemplaza: "la rama tiene el código que produjo el RESULT". Su adaptador no tenía las guardas degeneradas y la geometría moría con `ValueError:A: expected [T>=3,D>=1], got (3, 0)` (set 5→3); tampoco tenía los módulos schrodinger_transport_v0_1/v0_2.py (solo el esqueleto). El PR #14 publica el código del 13-nov + las correcciones. El RESULT de 8.4 MB no pudo subirse por MCP (HTTP 413; .gz rechazado por no ser UTF-8); quedan en la rama el código, la entrada, el verificador, la nota y el recibo con el output_sha256 para reproducirlo byte a byte. (2026-11-14)
- **Issue #64 (agente-cero-costo, clasificar previo_error): ChatGPT no la entregó; el hueco se corrigió aquí.** Solapa documentado en el PR #14 de motor-u6-storage. (2026-11-14)
