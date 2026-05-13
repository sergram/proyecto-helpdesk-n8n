# Semana 3–5: MVP Funcional

# Proyecto
Sistema Help Desk Automatizado con n8n

# Objetivo
Implementar un flujo mínimo viable (MVP) capaz de recibir, procesar y almacenar tickets técnicos automáticamente utilizando n8n y PostgreSQL.

# Arquitectura del MVP

Página Web → Webhook n8n → Validaciones → PostgreSQL → Logs

# Componentes implementados

## Frontend Local
Se desarrolló una página web HTML local para el ingreso de tickets técnicos.

Campos:
- nombre
- correo
- asunto

La página envía la información mediante fetch() hacia un webhook de n8n.

## Workflow 1 — Ingesta
Se implementó un Webhook POST en n8n capaz de recibir solicitudes JSON desde la página web local.

Endpoint:
```text
/webhook-test/nuevo-ticket