> **MEMORIA COMPARTIDA OBLIGATORIA:** Antes de cualquier trabajo, cualquier modelo debe leer [AGENTS.md](AGENTS.md), [el protocolo transversal](PROTOCOLO_MEMORIA_COMPARTIDA_OBLIGATORIA.md), [el índice de memoria](INDICE.md) y aplicar [el filtro de privacidad y minimización de huella](POLITICA_PRIVACIDAD_MINIMIZACION_HUELLA.md); consultar los hechos pertinentes y sincronizar los hechos durables al terminar. No empezar desde la memoria conversacional.

# Memoria compartida

Memoria persistente y consistente para los modelos del stack, para que no alucinen. Un solo lugar con los hechos verificados, las decisiones y las correcciones. Cualquier modelo que trabaje en el stack debe consultarla.

## Qué hay aquí y qué NO hay
- **Sí hay:** hechos verificados (con fecha y fuente), decisiones y correcciones. Lo destilado, no lo crudo.
- **No hay pláticas:** no están las conversaciones completas. Lo importante queda destilado.
- **No hay artefactos:** los artefactos viven en su repositorio especializado; aquí se registra qué existe y dónde está.

## Cómo se consulta
1. Lee `INDICE.md` primero.
2. Lee solo los archivos que tu tarea necesita.
3. Si un hecho no está en el índice, no está verificado: no lo inventes.

## Privacidad
El filtro `POLITICA_PRIVACIDAD_MINIMIZACION_HUELLA.md` es obligatorio antes de transmitir información a modelos o servicios externos. Minimiza datos personales y metadatos; no puede ocultar la IP, cuenta, dispositivo ni telemetría que el proveedor recibe por su propia infraestructura.

## Reglas
- Un hecho lleva fecha y fuente.
- Una corrección no borra el hecho viejo: lo marca como reemplazado.
- Nada de claves, contraseñas, tokens ni datos personales sensibles en ningún repo.
- Cuando algo cambia, se actualiza aquí y se avisa por el callback.
