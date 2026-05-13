# Boceto Workflow Principal

## Workflow 1 - Ingesta
Entrada mediante Webhook en n8n.

Datos:
- nombre
- correo
- asunto

## Workflow 2 - Procesamiento
Validación:
- campos vacíos
- prioridad automática

Reglas:
- urgente → prioridad alta
- normal → prioridad media

## Workflow 3 - Salida
Acciones:
- guardar ticket en PostgreSQL
- registrar logs
- registrar errores

## Manejo de errores
Workflow Error Trigger:
- captura excepciones
- registra errores en tabla errores