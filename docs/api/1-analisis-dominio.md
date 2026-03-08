# Análisis del Dominio – Sistema de Reservas

El sistema de reservas permite a los usuarios reservar recursos disponibles como salas o equipamiento.

## Tabla reservas

Campos principales:

- id (integer, PK)
- usuario_id (integer)
- recurso_id (integer)
- fecha_inicio (date)
- fecha_fin (date)
- num_personas (integer)
- estado (string)
- notas (text)
- creado_en (datetime)
- actualizado_en (datetime)

## Tabla usuarios

- id
- nombre
- email

## Tabla recursos

- id
- nombre
- tipo
- capacidad

## Campos expuestos en la API

La API mostrará:

- id
- usuario_id
- recurso_id
- fecha_inicio
- fecha_fin
- num_personas
- estado
- notas
- creado_en
- actualizado_en

## Validaciones

El backend validará:

- fecha_inicio < fecha_fin
- fechas futuras
- num_personas > 0
- recurso existente
