# Estado

Foto del 2026-11-08. El estado vivo está en el tablero de CAPCOT
(ajustes_entre_modelos/DELEGACIONES.md) y en el estado público
(agente-cero-costo, conector/ESTADO.md).

## Pendientes (tablero CAPCOT, 5)

1. Montar la cápsula Barreleye con 2 arreglos de texto (Imaginantes,
   pausado por créditos).
2. Subir los workflows de seguridad de CAPCOT (Marco, por navegador).
3. Activar la seguridad nativa en GitHub (Marco, manual).
4. Crear cuenta gratuita de Clayzo (Marco).
5. Verificar si los runners de Meta fueron adaptados e integrados
   por ChatGPT al motor U6 (Pecas, en revisión 2026-11-08).

## Stack agente-cero-costo (versión 4, 2026-11-08)

Transmigración v0.1, sanguijuela, avisos v4, conector macho-hembra,
estado público (el foquito), puente de lectura, puente Groq,
orquestador, dsh, máquina en el repo.

## Actualización CAPCOT — 2026-11-09

- PR #3 en `marcojpad-hash/capcot-capsulas-imaginantes`: sigue abierto, Draft, no merged, `mergeable=false`; head `feature/capcot-video-discovery-continuity`, 587 archivos modificados. El diff incluye diez `data/*.json` operativos y muchos artefactos `_tmp/`. No restaurar ni borrar esos datos sin contrastar con su fuente operativa autorizada.
- Corrección técnica importante: el workflow `capcot-grok-dispatch.yml` coincide con el contrato vigente, que solo permite handoff como `cola/entrada/<project_id>.json` tras QA narrativo independiente PASS. No ampliarlo para aceptar carpetas anidadas.
- La carpeta `cola/entrada/2026-11-07_dato-clavo-te-cocina/` no cumple el formato canónico plano y no presenta evidencia `narrative_qa.status=PASS`; no es dispatchable. No generar estado Grok ni simular recepción.
- Se corrigió el diagnóstico en `capcot-capsulas-imaginantes/docs/briefs/2026-11-09_CONTROL_COLA.md`, commit `82c33a4b9c134ce60c9680b3529495ba482b6e95` en la rama feature. El archivo se releyó después de la actualización.
- No se modificaron workflow, storyboards, cola, estados Grok, `data/*.json`, `main`, permisos ni secretos. No se ejecutó Actions ni se generaron medios.
- Fuente: revisión GitHub y lectura de `docs/CONTRATO_OPERATIVO_UNIFICADO.md`, `docs/QA_NARRATIVO_EN_FRIO.md`, `docs/GROK_STATUS_CONTRACT.md`, `scripts/validar_storyboard.py` y `AGENTS.md`, 2026-11-09.

## Actualización CAPCOT — reauditoría 2026-11-09 16:20 CDMX

- Reporte de control actualizado y releído en `marcojpad-hash/capcot-capsulas-imaginantes/docs/briefs/2026-11-09_CONTROL_COLA.md`, rama `feature/capcot-video-discovery-continuity`, commit de ampliación `c0bb942e50f31386e5640d2427bb0ac8c602dffb`.
- Lote 5–7 nov: 12 storyboards; QA frío JSON: 2 PASS narrativo (Venus 88, arena 94), 10 FAIL; 0/12 estructura apta por 510 campos narrativos estructurales ausentes. No se promovió ni redispatchó ninguno.
- Cuatro proyectos tienen evidencia de procesamiento/publicación preexistente: Venus, palomitas, arena cantante y ranas. No redispatchar. No se encontró `cola/estado` para los doce; recepción Grok no confirmada. Los MP4 referenciados por archivos sociales no están en el árbol GitHub.
- Hallazgos de fuentes que requieren corrección del redactor: pulpo identifica `Octopus insularis` pero el artículo estudia `Octopus laqueus`; ranas cita −16 °C con DOI 10.1242/jeb.089342 no registrado en `sources[]`; arena no vincula SRC-002 a mapa/sincronización; aguacate omite DOI 10.1016/j.heliyon.2025.e42588 y el pin institucional no corresponde a las afiliaciones del artículo; ballena sobreafirma con “casi se detiene”.
- Rotación: las doce propuestas usan `estructura=pregunta` (cuatro por día); `papel_rasgado_capas` se repite 5 y 6 nov. `procesar_cola.py` no llama `rotacion.diferencias_con_hoy`; `registro_editorial.py` no incorpora JSON sociales, bloqueados ni horarios diarios.
- Divergencia en CAPCOT `main`: existe paquete Andes del 9-nov con storyboard incompleto, copia de cola de una escena, programación declarada 14:15 fuera de la política vigente, sin QA ni medios verificables. No se modificó CAPCOT `main`.
- Último run de dispatch conocido: 1-nov, falla literal `Falta configurar GROK_WEBHOOK_URL.`; no hay ejecución posterior de la versión actual. TTS smoke 8-nov solo verificó instalación/compilación/CLI, no audio.
- El runtime local no se pudo obtener (`Could not resolve host: github.com`); los validadores/helpers Python no se ejecutaron, solo revisión estática. No se modificaron `data/*.json`, storyboards, estados Grok, workflows, secretos, permisos ni `main`; no se generaron medios ni se consumieron créditos.
- Bitácora de coordinación CAPCOT actualizada en el commit `9c044710cca94a7a863bd81d1e4c04b251a11ab1`.

## Actualización CAPCOT — 2026-11-10

- Radar diario guardado y releído en `marcojpad-hash/capcot-capsulas-imaginantes/docs/briefs/2026-11-10_RADAR_CAPCOT.md`, rama `feature/capcot-video-discovery-continuity`, commit `fb4f2fecfca36fb387d69ecd14a23f6ff9730ad9`.
- Borrador guardado y releído en `proyectos/2026-11-10_comida-aprendizaje-sabor-nutriente/storyboard.json`, commit `29a79447241ec2116c5b9e59a3773e1feb8c0c26`. Fecha objetivo 10-nov, slot_local 13:30 dentro de la ventana de mediodía en prueba; no equivale a programación.
- Validación posterior desde GitHub: JSON parseado; 8 escenas, 192 palabras, 78 s de escenas + 6 s de cortinilla = 84 s; voz es-MX-JorgeNeural +7%, -2Hz; estilo claymation con prompt_base literal; mapa UCSF Mission Bay con coordenadas 37.76873, -122.39258 y advertencia de que es afiliación institucional, no lugar exacto del experimento; capa de mecanismo dato/gráfico presente.
- Compuerta: `approved_assets=[]`, `export.render_status=NOT_GENERATED`, sin `export.filename` ni rutas de medios, `publicacion.status=PENDIENTE_DECISION_GROK`; no existe `narrative_qa`. El borrador permanece solo en proyectos/ y no está en cola/entrada; auditor independiente conserva PASS/FAIL.
- Se crearon exactamente dos entregables para la fecha: radar y storyboard. No se modificaron `data/*.json`, workflows, main, motores canónicos ni Motor U6; no se generaron medios, no se publicó ni programó y no se consumieron créditos.
- Los cinco DOI del radar permanecen PENDIENTE_RESOLVEDOR porque Crossref y el resolvedor no completaron acceso; las páginas primarias y el registro PubMed sí fueron consultados. El informe técnico Meta/Google no se reescribió porque no apareció un cambio oficial nuevo sustentado.
- La lectura de QA preexistente de los doce canónicos 5–7 nov y el robot del 9-nov, además de los storyboards recientes sin campo narrative_qa, queda detallada en el radar. No se modificó ningún QA.
## Actualización Mpemba — 2026-11-10

- Mpemba (Imaginantes, cápsula CAPCOT): v2 relevo APROBADA en fragmento por Marco el 2026-11-09 (80.12 s, Kokoro em_santa 0.85, QA PASA); montaje OFICIAL por Imaginantes (JorgeNeural, 89.83 s, QA OK) hecho el 2026-11-10 y programado para el 2026-11-11 13:30 CST (YouTube HSgrnejAcaI).
- NO volver a montar Mpemba: ya hay dos versiones hechas. Detalle en `hechos/proyectos.md`.
