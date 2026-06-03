# Proyecto Final - Análisis de Sistemas I

## Mesa de Ayuda (Help Desk) Local utilizando n8n

### Autor

Sergio Gramajo Pineda

---

## Descripción General

Este proyecto implementa una Mesa de Ayuda (Help Desk) local utilizando n8n, PostgreSQL y Docker Compose.

El sistema automatiza el proceso de recepción, clasificación, priorización, almacenamiento y generación de reportes relacionados con tickets de soporte técnico.

La solución permite registrar incidencias mediante un formulario web HTML y procesarlas automáticamente mediante workflows diseñados en n8n.

---

## Objetivos

### Objetivo General

Automatizar la gestión de tickets de soporte técnico mediante una solución local basada en workflows.

### Objetivos Específicos

* Registrar tickets mediante un formulario HTML.
* Validar la información recibida.
* Clasificar tickets por categoría.
* Asignar prioridades automáticamente.
* Registrar auditorías del sistema.
* Registrar errores operativos.
* Generar reportes semanales automáticos.
* Enviar reportes mediante correo electrónico.

---

## Tecnologías Utilizadas

### Backend

* n8n
* PostgreSQL 16

### Infraestructura

* Docker Compose
* Linux

### Frontend

* HTML
* CSS
* JavaScript

### Herramientas

* GitHub
* Adminer

---

## Arquitectura General

Formulario HTML

↓

Webhook (WF-01)

↓

Procesamiento (WF-02)

↓

PostgreSQL

↓

Reportes (WF-03)

↓

Correo Electrónico

---

## Base de Datos

El sistema utiliza PostgreSQL como motor de almacenamiento principal.

Tablas implementadas:

* tickets
* audit_log
* error_log

---

## Workflows Implementados

### WF-01 Ingesta de Datos

Funciones:

* Recepción de tickets
* Validación de correo electrónico
* Validación de campos obligatorios
* Respuesta HTTP al usuario

### WF-02 Procesamiento

Funciones:
* Clasificación por categoría
* Priorización automática
* Registro en PostgreSQL
* Auditoría de operaciones

### WF-03 Reportes

Funciones:

* Estadísticas de tickets
* Estadísticas por categoría
* Estadísticas por prioridad
* Estadísticas de errores
* Generación de reporte HTML
* Envío por correo electrónico

---

## Seguridad

El proyecto utiliza variables de entorno mediante archivo .env para evitar credenciales hardcodeadas.

Variables utilizadas:

* POSTGRES_USER
* POSTGRES_PASSWORD
* POSTGRES_DB
* N8N_PORT
* ADMINER_PORT
* POSTGRES_PORT
* TZ

---

## Manejo de Errores

El sistema registra errores en la tabla error_log para permitir trazabilidad y auditoría.

Los errores registrados son incluidos posteriormente en los reportes semanales generados por WF-03.

---

## Ejecución del Proyecto

### Levantar servicios

docker compose up -d

### Verificar contenedores

docker ps

### Acceder a n8n

http://localhost:5678

### Acceder a Adminer

http://localhost:8080

---

## Resultados Obtenidos

* Automatización completa del flujo de tickets.
* Persistencia local de datos.
* Clasificación automática.
* Priorización automática.
* Auditoría de operaciones.
* Reportes automáticos.
* Uso de contenedores Docker.
* Uso de variables de entorno.

---

## Conclusiones

La implementación de una Mesa de Ayuda basada en n8n permitió automatizar procesos que normalmente se realizan manualmente, mejorando la trazabilidad, organización y generación de reportes relacionados con soporte técnico.

El proyecto demuestra la aplicación práctica de conceptos de análisis de sistemas, bases de datos, automatización de procesos y administración de infraestructura local.
