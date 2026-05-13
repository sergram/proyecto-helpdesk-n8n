# Semana 1–2: Ideación y Base Técnica

# Proyecto
Sistema Help Desk Automatizado con n8n

# Problema
En organizaciones pequeñas y medianas los reportes técnicos suelen gestionarse manualmente, provocando pérdida de información, falta de seguimiento y ausencia de auditoría.

# Solución propuesta
Desarrollar un sistema automatizado utilizando n8n ejecutándose localmente mediante Docker.

El sistema permitirá:
- Recepción automática de tickets
- Validación de datos
- Clasificación de prioridad
- Registro automático en base de datos PostgreSQL
- Manejo de errores y logs

# Alcance
El proyecto funcionará completamente en entorno local utilizando:
- Docker
- n8n
- PostgreSQL
- Adminer

# Arquitectura propuesta

Usuario → n8n → PostgreSQL → Logs / Errores

# Tecnologías
- Docker Compose
- PostgreSQL
- n8n
- VSCode
- GitHub

# Objetivo
Automatizar el flujo de recepción y procesamiento de tickets técnicos de manera local, reproducible y escalable.

# Autor
Sergio Gramajo Pineda