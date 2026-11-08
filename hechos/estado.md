# Estado

Foto del 2026-11-08. El estado vivo está en el tablero CAPCOT y en el
estado público de agente-cero-costo.

## Restricción económica vigente (2026-11-08)

- Prohibidas compras, suscripciones, upgrades, pruebas pagadas y
  aprovisionamientos con posibilidad de generar cargos.
- No agregar tarjetas ni métodos de pago a proveedores.
- Usar únicamente recursos gratuitos y créditos ya disponibles.
- Si una VM o servicio no puede garantizarse dentro de la capa gratuita
  sin riesgo de facturación, no desplegarlo. No activar Oracle Pay As You
  Go ni recursos de pago.
- El worker GitHub Actions existente se conserva: es efímero, gratuito
  dentro de las cuotas disponibles y ya tiene ejecuciones verificadas.
- La VM de escritorio persistente es un componente adicional deseado,
  no una sustitución del worker. Solo se podrá desplegar si el plan y
  configuración son genuinamente gratuitos y no requieren método de
  pago ni habilitan cargos.

## Worker Linux (2026-11-08)

- Rama `runtime-linux-worker-20261108` en
  `marcojpad-hash/agente-cero-costo`.
- Workflow `.github/workflows/runtime-linux-worker.yml` ejecuta
  `runtime/linux_probe.py` en `ubuntu-24.04`.
- Dos ejecuciones GitHub Actions verificadas: 42514758321 y
  42514838564, ambas SUCCESS.
- Runner observado: 4 CPU, 16.76 GB RAM decimal (15.61 GiB), disco
  efímero. El runner se destruye al finalizar el job.
- El worker todavía no ejecuta trabajos genéricos de Floot; falta
  integración OIDC claim/complete y prueba E2E.
- PR #13 permanece draft; no fusionar sin aprobación.
- Oracle ARM 4 OCPU/24 GB no está provisionada.

## Arquitectura objetivo

- Mantener GitHub Actions como worker efímero para pruebas y tareas
  automatizadas.
- Añadir, si se confirma una opción totalmente gratuita y sin riesgo
  de cargos, un escritorio Linux persistente con navegador y perfiles
  de sesión controlados por el usuario, accesible desde Android y
  operable por agentes autorizados.
- Conectar ambos entornos al orquestador y memoria compartida mediante
  tareas allowlisted, autenticación segura y evidencia persistente.
- No compartir contraseñas con modelos; el usuario realiza login/MFA.
- No ejecutar shell arbitrario ni usar infraestructura de pago.

