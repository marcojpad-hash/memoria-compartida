# Memoria compartida

> **Gate obligatorio para todo modelo y todo repositorio:** [PROTOCOLO_MEMORIA_COMPARTIDA_OBLIGATORIA.md](PROTOCOLO_MEMORIA_COMPARTIDA_OBLIGATORIA.md). Antes de cualquier trabajo, leer `INDICE.md` y los hechos pertinentes; al cerrar, sincronizar hechos durables. No es opcional.

Memoria persistente y consistente para los modelos del stack, para que
no alucinen. Un solo lugar con los hechos verificados, las decisiones
y las correcciones. Cualquier modelo, en cualquier sesión, de cualquier
empresa, consulta esto y tiene la misma información.

## Qué hay aquí y qué NO hay

- **Sí hay:** hechos verificados (con fecha y fuente), decisiones y
  correcciones. Lo destilado, no lo crudo.
- **No hay pláticas:** no están las conversaciones completas. Pesan
  mucho y no hace falta: lo que importa de una plática es el hecho
  que dejó, y ese hecho está aquí destilado. Si algún día las
  pláticas pesaran poco, se podría guardar un resumen, nunca el
  transcript crudo.
- **No hay artefactos:** lo que crean los modelos (un .py, un .zip,
  un video) no vive aquí. Vive en su repositorio: en el motor, en
  CAPCOT, en agente-cero-costo, según corresponda. Aquí solo vive el
  hecho de que existe y dónde está.

## Cómo se consulta (para que no pese)

1. Lee `INDICE.md` primero. Es chiquito (menos de 1 KB): una línea
   por tema, con su archivo.
2. Lee **solo** los archivos que tu tarea necesita. Nunca leas todo
   el repo.
3. Si un hecho no está en el índice, no está verificado: no lo
   inventes. Pregunta o búscalo, y si lo verificas, agrégalo aquí.

## Presupuesto de peso

- Cada archivo: menos de 2 KB.
- El índice: menos de 1 KB.
- El repo completo: menos de 20 KB.

Así consultar la memoria cuesta poco: el índice es una lectura
chiquita y cada hecho es un archivo corto. Si un archivo crece,
se parte en dos.

## Reglas

- Un hecho lleva fecha y fuente. Sin fuente, es rumor, no hecho.
- Una corrección no borra el hecho viejo: lo marca como
  reemplazado y dice por cuál. Así nadie usa un hecho viejo.
- Nada de claves, contraseñas ni datos personales. Nunca van en
  ningún repo, ni privado.
- Cuando algo cambia, se actualiza aquí y se avisa por el callback
  (ver agente-cero-costo, `avisos/`).
