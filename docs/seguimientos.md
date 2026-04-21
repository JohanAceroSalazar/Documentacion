# 📊 Seguimiento Técnico del Proyecto

## 🧾 Información General
- Proyecto: Sistema de Gestión Aerolínea (Base de Datos)
- Autor: Johan Acero Salazar
- Tecnología: PostgreSQL + Liquibase + Docker
- Enfoque: Control de cambios, datos de prueba y gestión por dominios

---

## 📅 Registro de Actividades

### 🔹 Fase 1 – Modelado y Creación de Base de Datos (DDL)

**Actividades realizadas:**
- Diseño del modelo relacional completo.
- Creación de todas las tablas organizadas por dominios:
  - Geography
  - Airline
  - Identity
  - Security
  - Customer
  - Airport
  - Aircraft
  - Flight
  - Sales
  - Boarding
  - Payment
  - Billing
  - Notifications
- Definición de:
  - Claves primarias (UUID)
  - Claves foráneas
  - Restricciones (`CHECK`, `UNIQUE`, `NOT NULL`)

**Resultado:**
- Script `modelo_postgresql.sql` funcional.
- Integración con Liquibase mediante changeSets DDL.

---

### 🔹 Fase 2 – Datos de Prueba (DML)

**Actividades realizadas:**
- Creación de scripts de inserción por dominio:
  - `001-insert-geography.sql`
  - `002-insert-airline.sql`
  - `003-insert-identity.sql`
  - `004-insert-security.sql`
  - `005-insert-customer.sql`
  - `006-insert-airport.sql`
  - `007-insert-aircraft.sql`
  - `008-insert-flight.sql`
  - `009-insert-sales.sql`
  - `010-insert-boarding.sql`
  - `011-insert-payment.sql`
  - `012-insert-billing.sql`
  - `013-insert-notifications.sql`

- Creación de changelog DML (`0000changelog.yaml`).
- Organización por orden de dependencias entre tablas.

---

## ⚠️ Problemas Encontrados y Soluciones

### ❌ Error 1: Violación de constraint en `flight_segment`
**Problema:**
```
origin_airport_id = destination_airport_id
```

**Solución:**
- Ajuste del insert usando aeropuertos distintos (`LIMIT` y `OFFSET`).

---

### ❌ Error 2: `destination_airport_id` NULL

**Problema:**
- Solo existía un aeropuerto.

**Solución:**
- Inserción de un segundo aeropuerto antes del dominio Flight.

---

### ❌ Error 3: Re-ejecución de inserts

**Problema:**
- Liquibase no ejecuta changeSets ya aplicados.

**Solución:**
- Uso de rollback o creación de nuevos changeSets.

---

### ❌ Error 4: Duplicados por restricciones UNIQUE

**Problema:**
- Inserciones repetidas en tablas de seguridad.

**Solución:**
- Uso de:
```
WHERE NOT EXISTS (...)
```

---

## 🔹 Fase 3 – Seguridad (DCL)

**Actividades realizadas:**
- Creación de roles de base de datos:
  - `app_admin`
  - `app_user`
  - `app_readonly`

- Asignación de permisos:
  - `GRANT ALL` → admin
  - `SELECT, INSERT, UPDATE` → user
  - `SELECT` → readonly

- Configuración de privilegios por defecto.

- Integración mediante changeSet `014-dcl-database-roles`.

---

## 🔹 Fase 4 – Control de Cambios (Liquibase)

**Actividades realizadas:**
- Organización por capas:
  - `01_ddl`
  - `02_dml`
  - `03_dcl`
  - `05_rollbacks`

- Uso de:
  - `changeSet`
  - `sqlFile`
  - `rollback`

---

## ✅ Validaciones Realizadas

- Integridad referencial verificada.
- Restricciones (`CHECK`, `UNIQUE`) funcionando correctamente.
- Dependencias entre tablas respetadas.
- Ejecución correcta de changeSets.
- Corrección de errores durante inserciones.

---

## 📌 Estado Actual del Proyecto

✔ Base de datos creada  
✔ Datos de prueba insertados  
✔ Errores de integridad solucionados  
✔ Roles de base de datos implementados  
✔ Liquibase funcionando correctamente  

---

## 🚀 Conclusión

El proyecto se encuentra organizado por dominios, con control de versiones mediante Liquibase, datos de prueba coherentes con las dependencias del modelo y una estrategia básica de seguridad implementada a nivel de base de datos.

Se garantiza la integridad de los datos y la correcta ejecución de migraciones.