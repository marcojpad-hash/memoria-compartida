# Filtro transversal de privacidad y minimización de huella

**Obligatorio para todo modelo, agente, bot y sesión que trabaje con este stack.** Aplicar antes de enviar prompts, consultar servicios externos, crear issues, commits, logs, artifacts o documentos.

## Objetivo y límite
Reducir la exposición de datos personales y metadatos innecesarios. Este filtro no oculta la IP, cuenta, dispositivo, cookies ni telemetría que la plataforma o la red ya reciben; tampoco evita cuotas, rate limits o controles antiabuso. No usar proxies, rotación de IP ni identidades falsas para eludir restricciones.

## Antes de transmitir
1. Minimizar: enviar solo los datos imprescindibles para la tarea.
2. Sustituir nombres personales, correos, teléfonos, direcciones, ubicación precisa, IDs de cuenta y rutas locales por etiquetas neutras cuando no sean necesarios.
3. No incluir credenciales, tokens, cookies, claves, encabezados de autorización, datos financieros ni identificadores sensibles en prompts, issues, commits, logs o artifacts.
4. No adjuntar conversaciones completas ni perfiles personales. Extraer únicamente el fragmento técnico necesario.
5. Revisar archivos, capturas y metadatos adjuntos; eliminar EXIF, nombres de usuario, rutas y otros metadatos identificables cuando no sean necesarios.
6. Conservar nombres de repositorios, ramas, commits y rutas técnicas cuando sean indispensables para ejecutar o auditar la tarea; no confundirlos con datos personales.
7. Si un servicio necesita un dato identificador para autenticación o autorización, usar su conector/secret manager; nunca pegar el secreto en el prompt o en Git.

## Durante y después
- No inferir ni revelar ubicación, identidad o huella del usuario si no es necesaria.
- No copiar datos personales de un contexto a otro por conveniencia.
- En reportes, registrar el mínimo de evidencia técnica suficiente y preferir IDs de ejecución sobre datos personales.
- Si un envío contiene datos innecesarios, detenerse y sanitizar antes de transmitir.
- Si una tarea exige compartir datos personales, explicar qué dato es indispensable y con qué servicio se compartirá antes de hacerlo.

## Diagnóstico de restricciones
No atribuir una cuota agotada a la IP sin evidencia del proveedor. Distinguir límites de plan/acciones, rate limits por cuenta, límites por API key, límites de red/IP y bloqueos de seguridad. Registrar el mensaje exacto del proveedor y la ventana de reinicio. Este filtro protege la información que los modelos transmiten; no modifica la telemetría ni los controles internos de los proveedores.
