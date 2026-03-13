# 1. Introduccion, objetivos y antecedentes

## 1.1 Contexto y origen del proyecto

**The Good Barber** nace como respuesta a una necesidad operativa real detectada en barberias de barrio: la gestion manual de citas sigue siendo frecuente (telefono, mensajeria instantanea o agenda fisica), lo que genera solapamientos, huecos no aprovechados y una alta dependencia del tiempo del propietario para tareas administrativas repetitivas.

El caso de uso del proyecto se situa en una barberia local de Jerez de la Frontera, lo que permite trabajar sobre un contexto concreto, verificable y alineado con una implantacion realista.

En este contexto, el absentismo (clientes que reservan y no asisten) tiene impacto directo en la facturacion diaria, porque el modelo de negocio depende de la ocupacion de franjas horarias concretas. Cada cita perdida supone una venta no recuperable en ese tramo de tiempo.

La propuesta inicial se planteo como una solucion SaaS amplia, con automatizaciones multicanal, panel de administracion avanzado, gamificacion y personalizacion del portal. Para asegurar viabilidad dentro del marco academico y del tiempo disponible de desarrollo individual, el proyecto se acota a una implantacion vertical: **una unica barberia, una unica sede y un flujo de negocio claramente delimitado**.

## 1.2 Motivacion del proyecto

La motivacion principal es construir una aplicacion web que aporte valor real al negocio desde el primer despliegue, no solo como ejercicio tecnico. Esto implica:

- Reducir la carga manual de gestion de reservas y cancelaciones.
- Disminuir el absentismo mediante recordatorios y confirmaciones automatizadas.
- Mejorar la experiencia de reserva desde movil, priorizando rapidez y simplicidad.
- Aumentar la recurrencia de clientes con un sistema de fidelizacion visible y comprensible.
- Disponer de datos de operacion (ocupacion, cancelaciones, citas completadas, ingresos) para apoyar decisiones del negocio.

Desde el punto de vista formativo (CFGS DAW), el proyecto tambien permite demostrar competencias integradas de frontend, backend, modelado de datos, seguridad, despliegue y documentacion tecnica.

## 1.3 Objetivo general

Desarrollar y desplegar una aplicacion web SPA/PWA para una barberia real que digitalice el ciclo completo de reserva y seguimiento de citas, incorporando un motor automatizado anti-absentismo y un panel CRM para gestion operativa y personalizacion del servicio.

## 1.4 Objetivos especificos

1. Implementar una web publica responsive orientada a conversion de reservas desde movil y escritorio.
2. Permitir a clientes registrarse, iniciar sesion, reservar, consultar y cancelar citas en tiempo real.
3. Gestionar disponibilidad de servicios y franjas horarias sin solapamientos.
4. Integrar recordatorios y confirmaciones por WhatsApp, y llamadas de rescate por voz cuando no exista confirmacion previa.
5. Liberar automaticamente huecos no confirmados para reducir perdida de capacidad operativa.
6. Incorporar un panel CRM para gestionar citas, servicios, horarios, clientes, branding y contenido visible del sitio.
7. Incluir un sistema de fidelizacion con progreso visible y recompensas configurables.
8. Registrar metricas clave de negocio (ingresos, ocupacion, cancelaciones, citas rescatadas y completadas).

## 1.5 Alcance inicial y delimitacion

Para mantener un alcance realista y evaluable, el proyecto **no** se plantea en esta fase como plataforma multiempresa. Se implementa una solucion vertical con enfoque MVP funcional, priorizando:

- Flujo critico: reserva -> recordatorio -> confirmacion/cancelacion -> asistencia.
- Integraciones externas estrictamente necesarias (WhatsApp API y Twilio Voice).
- Persistencia y trazabilidad centralizadas en el backend como fuente de verdad.
- Despliegue real en entorno accesible por Internet.

Quedan fuera del alcance del proyecto final: multi-tenant, gestion multi-sede/multi-barbero, pagos online y cuadros de mando avanzados de evolucion comercial.

## 1.6 Expectativas y resultados esperados

Al finalizar el proyecto se espera disponer de un producto:

- **Funcional:** usable por clientes y administrador en un caso real.
- **Reproducible:** desplegable de forma consistente con documentacion tecnica.
- **Mantenible:** con arquitectura separada y decisiones tecnicas justificadas.
- **Medible:** con indicadores de actividad y absentismo para evaluar impacto.

Indicadores de exito esperados para el MVP:

- Reserva completa en pocos pasos desde movil.
- Confirmacion de citas previa al servicio por canal automatico.
- Reduccion de citas no asistidas frente a una gestion manual sin recordatorios.
- Capacidad del administrador para ajustar servicios, horarios y contenido sin cambios de codigo.
- Registro de estados de cita (pendiente, confirmada, cancelada, completada) para analizar el flujo de negocio.

Evidencias de validacion previstas para defensa y evaluacion:

- Demostracion funcional en entorno desplegado con flujo completo de reserva y gestion.
- Capturas o video corto del comportamiento del sistema ante confirmacion/no confirmacion.
- Registro de pruebas manuales de casos clave (reserva, cancelacion, confirmacion y liberacion de hueco).

## 1.7 Antecedentes y analisis comparativo breve

El mercado ya valida la demanda de herramientas de reserva para estetica y barberia. Existen soluciones consolidadas como **Booksy**, **Fresha**, **Treatwell** y **Timify**, ademas de sistemas de reservas genericos integrados en webs corporativas.

Estas referencias se consideran antecedentes funcionales porque ya cubren la necesidad de reserva digital, pero su enfoque suele estar orientado a escenarios mas amplios que el de una barberia individual con requerimientos de personalizacion y automatizacion muy especificos.

### Comparativa resumida

| Solucion | Fortalezas habituales | Limitaciones para pequena barberia |
| --- | --- | --- |
| Booksy / Fresha / Treatwell / Timify | Ecosistema maduro, buena base funcional, presencia de mercado | Coste recurrente o comisiones, funcionalidades sobredimensionadas para un negocio local, menor control de personalizacion profunda |
| Sistemas genericos de reserva en web | Implantacion rapida y sencilla | Cobertura limitada de flujos complejos, escasa automatizacion anti-absentismo, poca trazabilidad operativa |
| The Good Barber (propuesta) | Enfoque en absentismo, flujo pensado para un negocio concreto, CRM personalizable, fidelizacion integrada, arquitectura preparada para crecer | Alcance inicial deliberadamente acotado a una sola barberia y una unica sede |

### Posicionamiento del proyecto

El valor diferencial de **The Good Barber** no se basa en competir por amplitud funcional con plataformas generalistas, sino en resolver de forma precisa un problema de alto impacto economico en un contexto real: la perdida de citas por falta de confirmacion.

Por ello, la propuesta combina tres ejes:

- **Operacion:** reservas y disponibilidad en tiempo real.
- **Prevencion de absentismo:** automatizacion multicanal con reglas claras de confirmacion y liberacion.
- **Retencion:** gamificacion y fidelizacion para incentivar recurrencia.

Este enfoque permite entregar un producto academica y tecnicamente solido, con impacto demostrable y base escalable para futuras ampliaciones.
