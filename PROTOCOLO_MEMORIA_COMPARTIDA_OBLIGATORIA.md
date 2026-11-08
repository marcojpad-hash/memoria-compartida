# Protocolo obligatorio de memoria compartida — todos los modelos

**Alcance:** cualquier modelo, agente, bot o sesión que trabaje en cualquier repositorio de este propietario. **No es opcional ni depende del proyecto.**

## Gate de arranque — antes de analizar, responder, buscar, ejecutar o escribir
1. Abrir `https://github.com/marcojpad-hash/memoria-compartida`.
2. Leer `INDICE.md`.
3. Leer los archivos de `hechos/` que correspondan al proyecto y a la tarea. Como mínimo, consultar `hechos/proyectos.md` y `hechos/decisiones.md`; consultar además `estado.md`, `correcciones.md`, `tokens.md` o `personas.md` cuando sean pertinentes.
4. Leer el README, AGENTS.md, FeedMe, contratos y handoffs del repositorio de trabajo. La memoria compartida complementa; no sustituye la autoridad técnica local.
5. Si la memoria no está accesible, declarar el archivo y error exactos. No fingir lectura ni reconstruir hechos ausentes desde recuerdos o conversación.

## Durante el trabajo
- Tratar la memoria compartida como fuente transversal de hechos verificados, decisiones y correcciones vigentes.
- Resolver conflictos respetando autoridad: seguridad y contrato global; después contrato canónico del proyecto/componente; después memoria compartida para hechos transversales. Una corrección vigente reemplaza explícitamente al hecho anterior.
- No inventar, completar por intuición ni convertir inferencias en hechos.
- No copiar conversaciones completas ni artefactos al repositorio de memoria. Los artefactos viven en el repositorio especializado; aquí se registra qué existe, dónde y con qué evidencia.
- No copiar secretos, claves, tokens, contraseñas, datos personales sensibles ni contenido privado innecesario.
- Antes de una modificación, inspeccionar el estado actual, rama, commit y archivo; respetar candados, permisos y reglas locales.

## Cierre obligatorio
Antes de cerrar una tarea:
1. Identificar si produjo un hecho durable, decisión, corrección, bloqueo o cambio de estado transversal.
2. Si sí, actualizar el archivo temático correspondiente en `memoria-compartida/hechos/`: fecha, afirmación verificable, fuente/ruta/commit y, si reemplaza algo, referencia explícita al hecho reemplazado.
3. Actualizar `INDICE.md` solo si aparece un tema/archivo nuevo.
4. Registrar el artefacto y su ubicación en el repositorio especializado; no duplicar el artefacto en memoria.
5. Releer desde GitHub lo escrito y reportar commit, rutas y evidencia. Si no hubo hecho durable, no crear ruido en memoria.

## Regla de no simulación
Leer código no prueba ejecución; escribir un archivo no prueba que otro agente lo leyó; crear un handoff no prueba recepción. Separar OBSERVADO, EJECUTADO, VERIFICADO, INFERIDO, PROPUESTO, PENDIENTE y BLOQUEADO. No declarar éxito sin evidencia.

## Texto de activación
**Antes de cualquier trabajo en mis repositorios, consulta obligatoriamente la memoria compartida. No empieces por tu memoria conversacional. Lee INDICE.md y los hechos pertinentes; después lee el contrato local y trabaja con evidencia. Al cerrar, sincroniza los hechos durables de vuelta a memoria-compartida.**
