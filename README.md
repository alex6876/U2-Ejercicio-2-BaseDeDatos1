# Ejercicio — Base de Datos de Gestión de Vuelos de Aerolínea



Proyecto enfocado en la modelación Entidad-Relación (DER / MER) e implementación de base de datos relacional para la gestión integral de operaciones de vuelo, reservas de pasajes, flota de aviones y personal de tripulación.

---

## Descripción

El sistema modela una estructura de datos relacional para administrar la logística operativa de una compañía aérea. Permite registrar los aviones de la flota con sus especificaciones técnicas, gestionar los vuelos programados con sus rutas y horarios, administrar las reservas de asientos efectuadas por los pasajeros, y coordinar la asignación del personal de empleados a los distintos vuelos.

---

## Funcionalidades e Implementación

### Entidades y Atributos

* Avión:


* id_Avión: Clave primaria identificadora del avión.


* Matricula: Código único de matrícula de la aeronave.


* modelo: Fabricante y modelo del avión.


* Capacidad máxima de pasajeros: Cantidad límite de asientos disponibles en la aeronave.


* autonomía de vuelo: Distancia o tiempo máximo de vuelo sin reabastecimiento.




* Vuelo:


* id_Vuelo: Clave primaria identificadora del vuelo.


* Ciudad de Origen: Punto de partida o aeropuerto de origen.


* Ciudad de Destino: Punto de llegada o aeropuerto de destino.


* Horario de Salida: Hora estipulada para el despegue.


* Horario de llegada: Hora estimada o real de aterrizaje.


* Fecha de vuelo: Fecha programada para la realización del itinerario.




* Pasajeros:


* id_Pasajero: Clave primaria identificadora del pasajero.


* Nombre: Nombre(s) del pasajero.


* Apellido: Apellido(s) del pasajero.


* Dni: Documento nacional de identidad o número de documento.


* Teléfono: Número telefónico de contacto.




* Reservas:


* id_Reservas: Clave primaria identificadora de la reserva.


* Asientos: Número de plaza o asiento asignado.


* id_Pasajero: Clave foránea que vincula la reserva con un pasajero registrado.


* id_Vuelo: Clave foránea que vincula la reserva con un vuelo específico.




* Empleados:


* id_Empleados: Clave primaria identificadora del empleado.


* Nombre: Nombre completo del empleado.


* DNI: Documento de identidad.


* Categoria Profesional: Rol o cargo (ej. piloto, copiloto, tripulante de cabina, personal técnico).


* Fecha de Ingreso: Fecha de incorporación a la empresa.





---

## Relaciones del Modelo

1. Avión ↔ Vuelo (Relación 1:N):


* Un avión específico realiza múltiples vuelos a lo largo del tiempo, mientras que un vuelo programado es operado por un solo avión.




2. Pasajeros ↔ Reservas (Relación 1:N):


* Un pasajero puede registrar múltiples reservas, pero cada reserva individual corresponde a un solo pasajero.




3. Reservas ↔ Vuelo (Relación N:1):


* Muchas reservas pueden realizarse para un mismo vuelo, pero cada reserva pertenece a un único vuelo determinado.




4. Empleados ↔ Vuelo (Relación N:M):


* Un empleado puede estar asignado a prestar servicio en múltiples vuelos, y a su vez, un vuelo requiere de un equipo compuesto por múltiples empleados.
