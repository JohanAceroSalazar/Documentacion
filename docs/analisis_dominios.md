# Análisis de Dominios Funcionales

El modelo de base de datos se encuentra organizado en múltiples dominios funcionales claramente separados, lo cual evidencia una arquitectura orientada a escalabilidad y mantenibilidad.

## 1. Geografía y datos de referencia
Incluye:
- continent
- country
- state_province
- city
- district
- address
- time_zone
- currency

Responsabilidad:
Gestionar información geográfica y monetaria base para el sistema.

---

## 2. Aerolínea
Incluye:
- airline

Responsabilidad:
Representar las aerolíneas que operan en el sistema.

---

## 3. Identidad
Incluye:
- person
- person_type
- document_type
- person_document
- contact_type
- person_contact

Responsabilidad:
Gestionar la información personal y de contacto de los usuarios.

---

## 4. Seguridad
Incluye:
- user_account
- user_status
- security_role
- security_permission
- user_role
- role_permission

Responsabilidad:
Control de acceso, autenticación y autorización.

---

## 5. Clientes y fidelización
Incluye:
- customer
- loyalty_program
- loyalty_account
- loyalty_tier
- miles_transaction
- customer_benefit

Responsabilidad:
Gestión de clientes y programas de fidelización.

---

## 6. Aeropuerto
Incluye:
- airport
- terminal
- boarding_gate
- runway
- airport_regulation

Responsabilidad:
Infraestructura aeroportuaria.

---

## 7. Aeronaves
Incluye:
- aircraft
- aircraft_model
- aircraft_manufacturer
- aircraft_cabin
- aircraft_seat
- maintenance_event

Responsabilidad:
Gestión de flota y mantenimiento.

---

## 8. Operaciones de vuelo
Incluye:
- flight
- flight_segment
- flight_status
- flight_delay

Responsabilidad:
Planificación y ejecución de vuelos.

---

## 9. Ventas y reservas
Incluye:
- reservation
- reservation_passenger
- sale
- ticket
- ticket_segment
- fare

Responsabilidad:
Gestión comercial del sistema.

---

## 10. Abordaje
Incluye:
- check_in
- boarding_pass
- boarding_validation

Responsabilidad:
Proceso de embarque de pasajeros.

---

## 11. Pagos
Incluye:
- payment
- payment_transaction
- refund

Responsabilidad:
Gestión de pagos.

---

## 12. Facturación
Incluye:
- invoice
- invoice_line
- tax
- exchange_rate

Responsabilidad:
Facturación y contabilidad.