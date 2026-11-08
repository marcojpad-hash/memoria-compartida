# Protocolo obligatorio de memoria compartida — todos los modelos

**Alcance:** cualquier modelo, agente, bot o sesión que trabaje en cualquier repositorio de este propietario. No es opcional.

## Gate de arranque — antes de analizar, responder, buscar, ejecutar o escribir
1. Abrir el repositorio de memoria compartida.
2. Leer `INDICE.md`.
3. Leer los hechos pertinentes en `hechos/`.
4. Leer y aplicar `POLITICA_PRIVACIDAD_MINIMIZACION_HUELLA.md` antes de transmitir datos a cualquier modelo, API, conector, issue, commit, log o artifact.
5. Leer README, AGENTS.md y contratos del repositorio de trabajo.
6. Si la memoria no está accesible, declarar el archivo y error exactos; no fingir lectura.

## Durante el trabajo
- Minimizar toda información transmitida. Eliminar nombres, correos, teléfonos, direcciones, ubicación precisa, IDs personales, rutas locales y metadatos si no son necesarios.
- Nunca incluir secretos, tokens, cookies, claves ni encabezados de autorización en prompts, archivos o logs.
- Usar conectores/secret managers para autenticación.
- No copiar conversaciones completas ni perfiles personales.
- Conservar identificadores técnicos (repo, branch, commit, run) solo cuando sean necesarios para ejecutar o verificar.
- No usar proxies, rotación de IP ni identidades falsas para eludir cuotas o controles.
- No atribuir restricciones a la IP sin evidencia explícita del proveedor.
- La política reduce lo que el stack transmite; no puede ocultar IP, cuenta, dispositivo, cookies o telemetría que la plataforma/red recibe por su propia infraestructura.

## Cierre obligatorio
1. Sincronizar hechos durables, decisiones y correcciones verificadas con fecha y fuente.
2. Registrar artefactos en su repositorio especializado.
3. Releer lo escrito y reportar commit, rutas y evidencia.
4. Separar OBSERVADO, EJECUTADO, VERIFICADO, INFERIDO, PROPUESTO, PENDIENTE y BLOQUEADO.

## Regla de no simulación
Leer código no prueba ejecución; escribir un archivo no prueba que otro agente lo leyó; crear un handoff no prueba recepción. No declarar éxito sin evidencia.

**Activación:** antes de cualquier trabajo en mis repositorios, consulta memoria compartida, aplica el filtro de privacidad y minimización de huella, y sincroniza los hechos durables al cerrar.
