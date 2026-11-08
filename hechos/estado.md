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
- Estado: archivos creados en rama aislada. La consulta disponible
  de checks no mostró ejecución ni resultado; por tanto el host aún
  no está medido en evidencia y no se declara E2E activo.
- No conectado todavía a claim/complete de Postgres/Floot. El PR #13
  sigue draft y sin merge. Oracle ARM 24 GB sigue sin provisionar.
- Siguiente cierre: obtener el run/artifact real, luego integrar
  claim/complete con OIDC y publicar runtime. Sin cambios en CAPCOT
  ni Motor U6.
