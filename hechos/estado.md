# Estado

Foto del 2026-11-08. El estado vivo está en el tablero de CAPCOT
(ajustes_entre_modelos/DELEGACIONES.md) y en el estado público
(agente-cero-costo, conector/ESTADO.md).

## Pendientes (tablero CAPCOT, 5)

1. Montar la cápsula Mpemba (Imaginantes, pausado por créditos).
2. Montar la cápsula Barreleye con 2 arreglos de texto (Imaginantes,
   pausado por créditos).
3. Subir los workflows de seguridad de CAPCOT (Marco, por navegador).
4. Activar la seguridad nativa en GitHub (Marco, manual).
5. Crear cuenta gratuita de Clayzo (Marco).
6. Verificar si los runners de Meta fueron adaptados e integrados
   por ChatGPT al motor U6 (Pecas, en revisión 2026-11-08).

## Stack agente-cero-costo (versión 4, 2026-11-08)

Transmigración v0.1, sanguijuela, avisos v4, conector macho-hembra,
estado público (el foquito), puente de lectura, puente Groq,
orquestador, dsh, máquina en el repo.

## Actualización CAPCOT — 2026-11-09

- PR #3 en `marcojpad-hash/capcot-capsulas-imaginantes`: sigue abierto, Draft, no merged, `mergeable=false`; head `feature/capcot-video-discovery-continuity`, 587 archivos modificados. El diff incluye diez `data/*.json` operativos y muchos artefactos `_tmp/`. No restaurar ni borrar esos datos sin contrastar con su fuente operativa autorizada.
- Corrección técnica importante: el workflow `capcot-grok-dispatch.yml` coincide con el contrato vigente, que solo permite handoff como `cola/entrada/<project_id>.json` tras QA narrativo independiente PASS. No ampliarlo para aceptar carpetas anidadas.
- La carpeta `cola/entrada/2026-11-07_dato-clavo-te-cocina/` no cumple el formato canónico plano y no presenta evidencia `narrative_qa.status=PASS`; no es dispatchable. No generar estado Grok ni simular recepción.
- Se corrigió el diagnóstico en `capcot-capsulas-imaginantes/docs/briefs/2026-11-09_CONTROL_COLA.md`, commit `97dfd35b94de96ccecd7d366dc6acc4e808faf3c` en la rama feature. El archivo se releyó después de la actualización.
- No se modificaron workflow, storyboards, cola, estados Grok, `data/*.json`, `main`, permisos ni secretos. No se ejecutó Actions ni se generaron medios.
- Fuente: revisión GitHub y lectura de `docs/CONTRATO_OPERATIVO_UNIFICADO.md`, `docs/QA_NARRATIVO_EN_FRIO.md`, `docs/GROK_STATUS_CONTRACT.md`, `scripts/validar_storyboard.py` y `AGENTS.md`, 2026-11-09.