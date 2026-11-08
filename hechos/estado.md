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

## Stack agente-cero-costo (versión 4, 2026-11-08)

Transmigración v0.1, sanguijuela, avisos v4, conector macho-hembra,
estado público (el foquito), puente de lectura, puente Groq,
orquestador, dsh, máquina en el repo.

## Worker Linux (2026-11-08)

- Se creó la rama `runtime-linux-worker-20261108` en
  `marcojpad-hash/agente-cero-costo`.
- Se añadieron `.github/workflows/runtime-linux-worker.yml`,
  `runtime/linux_probe.py` y `runtime/README.md`.
- El workflow solicita un runner GitHub-hosted `ubuntu-24.04`, mide
  CPU/RAM/disco reales, verifica una operación determinista y conserva
  `runtime-result.json` como artifact por 30 días.
- Commits: probe `73fd4c7a538dd28fe18d77e1c98208695ecacf98`;
  workflow `fcf4faf714a88c879e6bdef01052b897c5dc16ac`;
  documentación `65c8e1cd1617f5bca05ab80b386bccd2bd1ccc86`.
- Ejecución real confirmada: GitHub Actions run 42514758321 terminó
  SUCCESS el 2026-11-08. Runner Ubuntu 24.04.5 LTS en Azure,
  región chilecentral; 4 CPU; RAM total 16,760,344,576 bytes
  (15.61 GiB), disponible 15,798,530,048 bytes; disco total
  154,894,188,544 bytes. Prueba determinista PASS; SHA-256
  5288a09b87518e21e896d41d696226cf38ae65f0d7ac026ca1c7bc2aad8ecb12.
  Job 128835226991 y artifact 13630364569, conservado hasta
  2026-12-08. Evidencia duradera en
  `agente-cero-costo/runtime/evidence/2026-11-08-linux-probe-42514758321.json`.
  Workflow: `agente-cero-costo/.github/workflows/runtime-linux-worker.yml`.
- Estado: primer worker Linux activo y probado; host efímero por job.
  No equivale aún a E2E de Floot: faltan claim/complete OIDC y publicar
  runtime. PR #13 sigue draft; Oracle ARM 24 GB no provisionada.
- No conectado todavía a claim/complete de Postgres/Floot. El PR #13
  sigue draft y sin merge. Oracle ARM 24 GB sigue sin provisionar.

## Runtime multiagente — integración y escalado (2026-11-08)

- Se añadió `runtime/EXECUTION_CONTRACT.md` en
  `agente-cero-costo`, rama `runtime-linux-worker-20261108`,
  commit `e91b10c213d57e2c663c1dfd7ae3598790f62c94`.
- El contrato fija el ciclo queue -> OIDC claim -> ejecución de tareas
  allowlisted -> OIDC complete -> evidencia/artifacts, con leases,
  idempotencia, reintentos y dead-letter.
- Tipos iniciales permitidos: `linux_probe`, `repo_status`,
  `python_tests`, `capcot_text_package_validation` y
  `u6_readonly_validation`. No se permite shell ni código arbitrario.
- La plantilla se clonará para workers paralelos solo después de pasar
  la prueba E2E. Los workers compartirán la cola y el contrato de memoria;
  no se sumará artificialmente la RAM entre runners.
- Próximo trabajo: implementar endpoints Floot `claim` y `complete`,
  cablear el workflow con OIDC, probar un job real de extremo a extremo
  y publicar el runtime. No modificar CAPCOT ni Motor U6 en esta fase.
- El consumo diario de acciones de Floot estaba agotado y su reinicio
  estaba previsto para 2026-11-09 06:00 UTC (00:00 CDMX); por eso la
  implementación Floot queda para después del reinicio, sin gastar
  acciones en lecturas/escrituras exploratorias.

## Límites confirmados

- El runner GitHub-hosted es efímero; se solicita uno por ejecución.
- El PR #13 de eventos sigue draft y no se fusiona como parte de este
  trabajo.
- No se han creado workers clonados ni se afirma que exista todavía
  ejecución E2E desde la cola.
- CAPCOT y Motor U6 permanecen sin cambios.
