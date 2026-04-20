# Plan de Trabajo Inicial

## Objetivo
Organizar la construcción de la base de datos por dominios de forma controlada y sin errores de dependencias.

---

## Fases

### Fase 1 – Estructura base (DDL)
- Crear carpetas:
  - 01_ddl
  - 02_dml
  - 03_dcl
- Configurar `changelog.yaml`
- Crear scripts por dominio

---

### Fase 2 – Creación de tablas

Orden de ejecución:

1. Geografía
2. Aerolínea
3. Identidad
4. Seguridad
5. Clientes
6. Aeropuerto
7. Aeronaves
8. Vuelos
9. Ventas
10. Abordaje
11. Pagos
12. Facturación
13. Notificaciones

---

### Fase 3 – Inserción de datos
- Crear scripts en `02_dml/00_inserts`
- Insertar datos mínimos por dominio
- Validar con SELECT

---

### Fase 4 – Seguridad (DCL)
- Crear roles en:
  - `03_dcl/00_roles`
- Crear permisos en:
  - `03_dcl/01_grants`

---

### Fase 5 – Validación
- Ejecutar todos los scripts con Liquibase
- Verificar:
  - Integridad referencial
  - Constraints
  - Relaciones entre dominios

---

## Herramientas

- PostgreSQL
- Liquibase
- Visual Studio Code

---

## Resultado esperado

- Base de datos completamente estructurada
- Dominios independientes pero relacionados
- Scripts organizados y reutilizables