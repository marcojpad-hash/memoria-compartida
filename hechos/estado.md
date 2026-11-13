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


## Actualización VoxCPM2 — 2026-11-10

- El paquete VoxCPM2 para la microserie «La heredera que vendieron» está publicado en `marcojpad-hash/microserie-heredera-voces`, rama `main`: `.github/workflows/voxcp2-cpu.yml`, `scripts/generar_muestras.py`, `muestras.json` y su README de operación.
- El script usa `openbmb/VoxCPM2` (2B), Voice Design con texto de control en inglés y líneas en español, CPU, Python 3.11, 48 kHz; genera Camila/Carmen/Don Emilio con seeds 42/43/44, carga el modelo una sola vez y produce WAV + manifiesto de corrida.
- No hay evidencia en esta sesión de ejecución real de VoxCPM2, WAV generado, reproducción ni escucha humana. No declarar muestra terminada ni calidad escuchada.
- El README del repo se corrigió y releyó; commit `7867ff8e097ec4df544ccc8dcf6cb04ee10077a1`. Se reemplazó el estado obsoleto «solo local / nada subido» por el estado comprobado en GitHub.
- El disparo sigue condicionado a confirmar que la corrida #3 de SadTalker quedó resuelta, tal como indica el expediente previo. Esta sesión no dispone de una acción GitHub `workflow_dispatch`; no se disparó Actions ni se intentó eludir la compuerta.
- Fuente: lectura directa de los tres archivos y README en GitHub, rama `main`, 2026-11-10; verificación posterior del README tras el commit citado.

## Actualización CAPCOT — auditoría 2026-11-13

- Informe de auditoría creado y releído en `marcojpad-hash/capcot-capsulas-imaginantes/docs/briefs/2026-11-13_CONTROL_COLA.md`, rama `feature/capcot-video-discovery-continuity`, commit `4574b4735dcf2c11da441f0bdb4c1cc5ff84eded`.
- El borrador `2026-11-13_dato-caracol-16-embriones` recibió `narrative_qa=PASS`, score 91, siete checks true y flags vacíos. Sigue como propuesta; `slot_cesta` y horario diario no están definidos, DOI `10.1038/s42003-026-11188-7` sigue `PENDIENTE_RESOLVEDOR`, `cola/estado` 404. No se promovió porque el usuario prohibió disparar workflows y no hubo runtime para ejecutar el validador.
- Lote obligatorio 5–7 nov re-auditado en frío: 2 PASS (Venus 88, Arena 94), 10 FAIL; todos los `reviewed_at` actualizados a 2026-11-13 y releídos. La estructura sigue 0/12 apta: 510 campos narrativos ausentes, 75/85 SFX vacíos y Árboles con 169 palabras y sin mapa/dato. Los 12 estados Grok devuelven 404.
- Reconciliación de publicaciones (corrección 13-nov tras contrastar horarios diarios): evidencia exacta por `project_id` para cinco proyectos: Palomitas `zTP5akrGA9M`, Ranas `UBFuKBU3cx0`, Aguacate `nSS_q2tj2P0`, Ballena `wbFrlM2e_YE` y Hielo `HSgrnejAcaI`. Los IDs globales de Venus `phVfyHp3CnY` y Arena `m4RqQRaz55k` no tienen vínculo exacto con `project_id`/slot y no se atribuyen a esos proyectos. Los cinco quedan protegidos contra redispatch.
- Hielo: QA audiovisual 89.83 s; YouTube ID ya no aparecía el 12-nov; Facebook publicado y TikTok en discrepancia (archivo social `programado`, registro central `publicado`). `capsula.mp4` y `portada.jpg` no están en el árbol: `MEDIOS_NO_VERIFICADOS_EN_REPOSITORIO`. Metadata/caption afirma que el agua caliente se congela antes que la fría, aunque el storyboard presenta el efecto como no universal/en disputa.
- Pulpo: el storyboard dice `Octopus insularis`, pero el DOI `10.1038/s41586-023-06203-4` corresponde al estudio de `Octopus laqueus` (PubMed, https://pubmed.ncbi.nlm.nih.gov/37380770/).
- El workflow solo acepta `cola/entrada/*.json` de primer nivel; `procesar_cola.py` acepta carpetas anidadas y `--fecha` histórica, filtrando por prefijo de ruta. `registro_editorial.py` no incorpora cierres diarios, horario semanal, bloqueados ni handoffs. Las tablas `data/temas_del_dia`, `rotacion`, `estilos_usados`, `vistas_historico` y `balances_6h` siguen con cortes 28–31 oct.
- No se obtuvo runtime local ni acceso al listado/logs recientes de Actions. No se modificaron `data/*.json`, `main`, workflow, secretos, permisos ni estados Grok; no se generaron medios ni se consumieron créditos.
- Fuente: lectura y relectura directa de GitHub en la rama feature y `main` solo para evidencias de publicación; informe citado y PubMed, 2026-11-13.
