# Sistema de Información Penitenciario — Cárcel de Ocaña

> **Estado:** Fase de Análisis (documento base para proyecto universitario).  
> El contenido está elaborado únicamente con la información proporcionada y puede adaptarse en fases posteriores.

---

## Índice
- [Resumen](#resumen)  
- [Descripción del problema](#descripción-del-problema)  
- [Objetivo del sistema](#objetivo-del-sistema)  
- [Alcance](#alcance)  
- [Requisitos funcionales](#requisitos-funcionales)  
- [Requisitos no funcionales](#requisitos-no-funcionales)  
- [Actores del sistema](#actores-del-sistema)  
- [Modelo conceptual (entidades y atributos)](#modelo-conceptual-entidades-y-atributos)  
- [Observaciones y futuras ampliaciones](#observaciones-y-futuras-ampliaciones)  
- [Estado y notas finales](#estado-y-notas-finales)

---

## Resumen
Sistema de información orientado a organizar y gestionar la información sobre reclusos, celdas y pisos de la cárcel de la ciudad de Ocaña. Busca reemplazar el manejo manual actual por una solución digital que permita consultas rápidas, control de disponibilidad de celdas y seguimiento del tiempo de condena.

---

## Descripción del problema
La cárcel de Ocaña no dispone de un sistema digital para registrar y consultar datos de internos, celdas y pisos. La gestión manual actual genera:
- Desorden en los registros.
- Pérdida de tiempo en búsquedas y trámites.
- Dificultad para conocer con rapidez la ubicación exacta de un recluso (piso/celda).
- Problemas para ver disponibilidad real de celdas y el tiempo restante de condena.

---

## Objetivo del sistema
Desarrollar un sistema de información que permita organizar la estructura de la cárcel (pisos → celdas → reclusos), gestionar registros de internos y facilitar la administración y seguimiento mediante consultas y reportes básicos.

---

## Alcance
El sistema permitirá, como funcionalidad inicial:
- Registrar reclusos con datos personales y judiciales.  
- Asociar cada recluso a una celda y a un piso específico.  
- Consultar en qué piso/celda se encuentra un recluso.  
- Visualizar cuánto tiempo le falta de condena a cada interno.  
- Mostrar la disponibilidad de celdas (ocupadas y libres).  
- Generar reportes básicos de reclusos y celdas.

**Fuera del alcance actual (posible ampliación posterior):** historial de traslados, gestión de visitas, registro de conducta y sanciones.

---

## Requisitos funcionales
1. El sistema debe permitir registrar un nuevo recluso con sus datos personales y judiciales.  
2. El sistema debe asignar el recluso a una celda en un piso.  
3. El sistema debe permitir consultar un recluso por nombre o por código.  
4. El sistema debe mostrar el tiempo restante de condena de cada interno.  
5. El sistema debe mostrar el estado de las celdas (libres/ocupadas).  
6. El sistema debe permitir generar un reporte de ocupación de la cárcel.

---

## Requisitos no funcionales
- **Usabilidad:** Interfaz sencilla y accesible para el personal administrativo.  
- **Escalabilidad:** Soportar múltiples pisos, múltiples celdas y numerosos reclusos.  
- **Seguridad:** Acceso restringido a usuarios autorizados (roles).  
- **Disponibilidad:** Estar disponible para consultas rápidas cuando se necesite.

---

## Actores del sistema
- **Administrador de la cárcel:** Gestiona la información completa (reclusos, pisos, celdas, reportes).  
- **Guardias / Funcionarios:** Consultan la ubicación de reclusos y el tiempo de condena; realizan consultas operativas.  
- **Sistema:** Procesa y organiza la información; realiza cálculos (por ejemplo, tiempo restante de condena) y mantiene la integridad de los datos.

---

## Modelo conceptual (entidades y atributos)
A continuación se presenta un resumen de las entidades principales y sus atributos clave (basado en la información proporcionada):

- **Recluso**
  - ID
  - nombre
  - delito
  - condena total
  - tiempo cumplido
  - tiempo restante
  - estado (por ejemplo: activo, liberado, traslado)

- **Celda**
  - ID
  - número
  - capacidad
  - estado (libre / ocupada / mantenimiento)
  - referencia al piso

- **Piso**
  - ID
  - número de piso
  - cantidad de celdas

