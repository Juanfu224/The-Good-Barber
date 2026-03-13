# Propuesta Formal de Proyecto Final

## The Good Barber

**Autor:** Juan Felipe Arias Aguirre
**Ciclo:** CFGS Desarrollo de Aplicaciones Web (DAW)  
**Centro:** IES Rafael Alberti
**Fecha:** 13 de marzo de 2026

---

## Índice

1. [Identificación de necesidades](#1-identificación-de-necesidades-criterio-1c)
2. [Oportunidades de negocio](#2-oportunidades-de-negocio-criterio-1d)
3. [Tipo de proyecto](#3-tipo-de-proyecto-criterio-1e)
4. [Características específicas](#4-características-específicas-criterio-1f)
5. [Obligaciones legales y prevención](#5-obligaciones-legales-y-prevención-criterio-1g)
6. [Ayudas y subvenciones](#6-ayudas-y-subvenciones-criterio-1h)
7. [Guión de trabajo](#7-guión-de-trabajo-criterio-1i)
8. [Referencias](#referencias)

---

## Introducción

**The Good Barber** es una aplicación web orientada a la gestión digital de reservas para una barbería de barrio. El proyecto nace de una necesidad real: reducir el absentismo en citas, mejorar la organización diaria del negocio y ofrecer a los clientes una experiencia de reserva sencilla, rápida y adaptada al uso móvil.

La idea inicial contempla una plataforma SaaS con automatizaciones por WhatsApp, llamadas de voz, gamificación y personalización administrativa completa. Dado que el desarrollo será realizado por una única persona y el tiempo real disponible es de **2 meses**, la viabilidad del proyecto no se basará en eliminar estos pilares funcionales, sino en **delimitar con precisión el contexto de implantación**: una única barbería, una única sede, un catálogo acotado de servicios y un flujo operacional bien definido. De este modo, el proyecto mantiene sus características diferenciales y sigue siendo **terminado, desplegable y evaluable** dentro del plazo disponible.

El proyecto permitirá demostrar competencias de análisis, diseño, desarrollo frontend y backend, modelado de datos, seguridad, despliegue y mantenimiento, cumpliendo con los resultados de aprendizaje esperados en el ciclo de DAW.

---

## 1. Identificación de necesidades (Criterio 1c)

### Problema o necesidad detectada

Muchos pequeños negocios de servicios personales, como barberías, siguen gestionando sus citas mediante teléfono, mensajería instantánea o agendas manuales. Este modelo genera varios problemas operativos:

- Pérdida de tiempo en la gestión manual de reservas y cancelaciones.
- Dificultad para mantener el horario actualizado en tiempo real.
- Alto riesgo de errores humanos o solapamientos de citas.
- Falta de datos históricos para analizar ingresos, horas punta o nivel de absentismo.
- Pérdida económica derivada de clientes que reservan pero finalmente no acuden.

En una barbería de volumen medio, cada hueco perdido impacta directamente en la facturación diaria, ya que se trata de un negocio basado en la ocupación de franjas horarias concretas. Por ello, el absentismo no es solo una molestia organizativa, sino un problema económico real.

### Cómo se ha detectado la necesidad

La necesidad se identifica a partir de tres fuentes:

1. **Observación del funcionamiento habitual de barberías locales**, donde todavía es frecuente gestionar reservas de manera manual o semi-manual a través de teléfono, WhatsApp o agenda física.
2. **Análisis del flujo de trabajo del negocio**, detectando puntos críticos como la confirmación de citas, los huecos no aprovechados, la dificultad para reorganizar cancelaciones de última hora y la falta de automatización.
3. **Revisión de soluciones existentes en el mercado**, comprobando que muchas plataformas están pensadas para negocios de mayor tamaño, incluyen costes recurrentes elevados o no están adaptadas a una implantación sencilla y personalizada para un comercio local.

Estas evidencias permiten delimitar un problema concreto y verificable: la barbería necesita una herramienta propia que centralice la reserva, reduzca la gestión manual y actúe de forma automática ante el riesgo de absentismo.

### Usuarios o beneficiarios de la solución

Los usuarios principales del sistema serán:

- **Administrador del negocio (barbero o propietario):**
  - Gestionará servicios, horarios, citas, clientes y configuración básica.
  - Consultará métricas simples de ocupación, cancelaciones y citas completadas.
  - Reducirá el tiempo dedicado a tareas administrativas repetitivas.

- **Clientes de la barbería:**
  - Podrán consultar disponibilidad y reservar cita de forma rápida.
  - Recibirán recordatorios automáticos para confirmar o cancelar.
  - Tendrán acceso a un historial básico y a un sistema de fidelización simple.

- **Beneficiario indirecto:**
  - El propio negocio, al incrementar la organización, la trazabilidad de la actividad y la rentabilidad por franja horaria.

### Delimitación del problema

El proyecto se enfoca inicialmente en **una única barbería**, no en una plataforma multiempresa completa. Esta decisión responde a criterios de viabilidad técnica y temporal. El objetivo del proyecto final no será construir un gran SaaS generalista, sino una **solución vertical funcional**, con arquitectura preparada para crecer posteriormente.

---

## 2. Oportunidades de negocio (Criterio 1d)

### Análisis de mercado

En el mercado existen soluciones consolidadas para reservas y gestión de negocios de estética y peluquería, entre ellas:

- **Booksy**
- **Fresha**
- **Treatwell**
- **Timify**
- Herramientas genéricas de reservas integradas en webs corporativas

Estas plataformas demuestran que existe una necesidad real y un mercado consolidado. No obstante, presentan varias limitaciones para pequeños negocios:

- Costes recurrentes por suscripción o comisión.
- Exceso de funcionalidades para un comercio local pequeño.
- Menor capacidad de personalización específica.
- Dependencia de plataformas externas para la relación con el cliente.
- Escasa adaptación a un flujo sencillo centrado en reducir el absentismo de forma económica.

### Propuesta de valor diferencial

La propuesta de **The Good Barber** se diferencia por los siguientes aspectos:

- Está pensada desde el inicio para un **negocio concreto y real**, no como una plataforma genérica.
- Se centra en el problema más costoso del servicio por cita: **el absentismo**.
- Ofrece una experiencia de reserva simple, rápida, orientada a móvil y reforzada con una interfaz gamificada.
- Incluye un **panel CRM propio y personalizable** para controlar horarios, servicios, citas, precios, contenidos y apariencia visual de la web sin depender de terceros.
- Incorpora un sistema de **confirmación anti-absentismo multicanal** con WhatsApp, llamada automatizada y cancelación/liberación automática del hueco.
- Añade una **capa de fidelización gamificada**, útil para reforzar recurrencia y aumentar la retención del cliente.

### Ajuste de la idea a la viabilidad real

La idea inicial incluía:

- Integración con WhatsApp API.
- Llamadas automáticas con Twilio.
- Panel CRM muy avanzado.
- Personalización completa de la web como plantilla SaaS.
- Arquitectura headless separada.
- Sistema de gamificación amplio.

Para que este planteamiento sea viable en **2 meses de desarrollo individual**, el proyecto se acotará sin renunciar a sus funcionalidades nucleares. La estrategia será la siguiente:

- Implantación para **una única barbería** y un único panel de administración.
- Un solo flujo de negocio principal: reserva, confirmación, asistencia o cancelación.
- Catálogo inicial reducido a los servicios esenciales de la propuesta: corte, barba y lavado.
- Integraciones externas limitadas a las estrictamente necesarias para el motor anti-absentismo: **WhatsApp API de Meta** y **Twilio Voice API**.
- Analítica y personalización completas a nivel de proyecto final, pero sin extender el alcance a multiempresa, marketplace ni pagos online.
- Desarrollo por iteraciones cerradas, priorizando primero el flujo operativo y después la capa de personalización y analítica.

#### MVP del proyecto

El MVP incluirá:

- Web pública responsive y PWA con información del negocio, galería, precios y ubicación.
- Registro e inicio de sesión de clientes.
- Reserva, consulta y cancelación de citas en tiempo real.
- Gestión de franjas horarias, disponibilidad y servicios.
- Panel visual de gamificación y progreso de fidelización en la home y en el área de cliente.
- Integración real con WhatsApp Business API.
- Llamadas automáticas con Twilio Voice.
- Recordatorios automáticos con confirmación, cancelación y liberación automática de huecos.
- Panel CRM para gestionar citas, servicios, horarios, clientes, analíticas y configuración de la web.
- Sistema de puntos o recompensas por citas completadas con canje automático.
- Métricas de negocio y analíticas de ingresos y absentismo.
- Personalización de branding desde panel: colores, logotipo, imágenes, textos y parámetros de fidelización.


#### Futuras implementaciones

Quedarán fuera del alcance del proyecto final, pero contempladas como evolución:

- Plataforma multi-tenant para varias barberías.
- Gestión multi-barbero y multi-sede.
- Pagos online y anticipos.
- Cuadros de mando avanzados con comparativas históricas y exportación.
- Sistema de reseñas y campañas promocionales segmentadas.
- Integración con calendarios externos y recordatorios push complementarios.

### Potencial de la solución

El potencial del proyecto es razonable por tres motivos:

1. **Aplicación inmediata en un caso real:** una barbería con gestión de citas recurrentes.
2. **Escalabilidad funcional:** la arquitectura puede evolucionar hacia un producto SaaS sectorial.
3. **Transferibilidad del modelo:** el mismo enfoque podría adaptarse a peluquerías, centros de estética, clínicas o negocios con cita previa.

Desde el punto de vista académico y profesional, el proyecto resulta sólido porque combina una necesidad real, un alcance viable y una posible evolución comercial futura.

---

## 3. Tipo de proyecto (Criterio 1e)

### Tipo de aplicación

El proyecto será una **aplicación web SPA/PWA de arquitectura headless cliente-servidor**, optimizada para uso móvil y pensada para que la mayor parte de las reservas se realicen desde teléfono. La solución combinará una capa pública interactiva, un backend desacoplado con API propia y un panel CRM de administración.

### Justificación del tipo de proyecto

Este tipo de aplicación es el más adecuado porque:

- Permite acceso universal desde navegador sin instalar software.
- Facilita la reserva rápida desde dispositivos móviles y su posible instalación como PWA.
- Reduce la barrera de entrada para usuarios no técnicos.
- Separa claramente la lógica de negocio del frontend público y del panel CRM.
- Permite evolucionar la solución hacia un modelo SaaS más amplio sin rehacer la base técnica.
- Se alinea con la necesidad de integrar automatizaciones, colas, analíticas y personalización del portal.

Una arquitectura cliente-servidor bien diseñada permite además demostrar competencias técnicas propias del ciclo DAW: consumo de datos, autenticación, validación, gestión de sesiones, persistencia, seguridad, diseño responsive y despliegue.

### Arquitectura propuesta

Se propone una **arquitectura headless avanzada**, separando de forma estricta el frontend interactivo, el backend de negocio y el panel CRM. Esta decisión responde a la naturaleza del proyecto, que requiere un motor de automatización desacoplado, una interfaz pública con identidad visual propia y una base técnica escalable para una futura evolución SaaS.

#### Arquitectura lógica

- **Frontend web y PWA:** interfaz de reserva, gamificación, consulta y confirmación para clientes.
- **Backend de negocio:** lógica de reservas, horarios, fidelización, confirmaciones, llamadas de rescate y estados de cita; actuará como fuente de verdad del sistema.
- **Panel CRM:** gestión administrativa, analítica y personalización visual y funcional de la plataforma.
- **Capa de automatización:** orquestación de integraciones externas y flujos automáticos mediante n8n, conectada con Laravel mediante webhooks y endpoints internos.
- **Base de datos relacional:** persistencia de usuarios, servicios, horarios, citas, eventos de confirmación y recompensas.
- **Sistema de colas y tareas programadas:** ejecución del motor anti-absentismo, mensajería y actualización automática de estados.

### Stack tecnológico seleccionado

#### Backend y automatización

- **Laravel 12**
- **PHP 8.3**
- **PostgreSQL 18**
- **Redis** para colas y caché
- **Laravel Scheduler** para tareas programadas
- **Laravel API Resources** para exponer la lógica de negocio
- **Carbon** para la orquestación temporal de citas y recordatorios
- **n8n** como plataforma de automatización para integrar y orquestar flujos con servicios externos

#### Frontend

- **Angular 21+ standalone**
- **Signals y Zoneless**
- **Angular CDK**
- **SASS con ITCSS y metodología BEM**

#### Panel de administración

- **FilamentPHP**

#### Integraciones externas

- **WhatsApp API de Meta** integrada a través de workflows de n8n para recordatorios y confirmaciones
- **Twilio Voice API** integrada mediante n8n para llamadas automatizadas de rescate

#### Infraestructura y despliegue

- **Docker con Laravel Sail** para entorno local
- **GitHub** para control de versiones
- **GitHub Actions** para integración continua
- **Laravel Forge** para despliegue continuo
- **Despliegue en VPS Linux** con Nginx, PHP-FPM, PostgreSQL, Redis y una instancia autohospedada de n8n

### Justificación técnica del stack

La combinación **Angular + Laravel + Filament + Redis + n8n** se considera adecuada para este proyecto por las siguientes razones:

- **Angular 21 standalone** permite construir un frontend moderno, estructurado y orientado a componentes, idóneo para una PWA rica en interacción.
- **Signals y Zoneless** ayudan a mantener rendimiento y reactividad con una base tecnológica actual.
- **Laravel 12** ofrece un backend sólido para reglas de negocio, colas, API, autenticación y tareas programadas.
- **Filament** acelera de forma decisiva la implementación del panel CRM, reduciendo el coste de desarrollo del backoffice.
- **Redis** encaja con la necesidad de gestionar colas, eventos y automatizaciones temporales sin bloquear procesos críticos.
- **n8n** reduce el tiempo de integración con servicios externos como WhatsApp y Twilio, al permitir construir workflows visuales reutilizables y conectarlos con Laravel mediante webhooks y endpoints internos.
- **PostgreSQL** garantiza integridad relacional y robustez para un sistema de citas, recompensas y métricas.
- La separación headless permite que el frontend público y el panel administrativo evolucionen con cierta independencia.
- La lógica crítica del negocio permanece centralizada en Laravel, mientras que n8n se utiliza únicamente como capa de automatización e integración, lo que mejora la mantenibilidad y la trazabilidad del sistema.
- El uso de n8n autohospedado evita depender de un proveedor adicional de automatización y permite controlar mejor el flujo de datos, las credenciales y la auditoría técnica del proyecto.

Por tanto, se prioriza una arquitectura **moderna, escalable y coherente con la propuesta original**, manteniendo la viabilidad gracias a la delimitación del dominio y al uso de herramientas que aceleran el desarrollo.

---

## 4. Características específicas (Criterio 1f)

### Objetivo funcional del MVP

El objetivo del MVP es disponer de una aplicación web completamente funcional para una barbería concreta, integrando el flujo completo de reserva, fidelización y rescate de citas mediante automatización por WhatsApp, llamada telefónica y cancelación automática, junto con un panel CRM personalizable y una interfaz pública móvil de alta conversión.

### Funcionalidades principales del MVP

#### Funcionalidades obligatorias

1. **Web pública del negocio**
   - Página de inicio con descripción del servicio.
   - Listado de servicios y precios.
   - Información de ubicación y contacto.
   - Galería de imágenes del local y trabajos realizados.
   - Sticky CTA para favorecer la conversión a reserva.
   - Diseño responsive mobile first con base PWA.
   - Panel visible de progreso de fidelización.

2. **Gestión de usuarios**
   - Registro de clientes.
   - Inicio y cierre de sesión.
   - Edición básica de perfil.

3. **Sistema de reservas**
   - Selección de servicio.
   - Selección de fecha y hora disponibles.
   - Generación automática de franjas según horario configurado.
   - Confirmación inmediata de reserva.
   - Consulta del estado de la cita.
   - Cancelación por parte del cliente dentro de un plazo definido.
   - Aplicación automática de recompensa cuando el cliente tenga un canje disponible.

4. **Motor automatizado anti-absentismo**
   - Envío de recordatorio por WhatsApp 24 horas antes mediante la API de Meta, orquestado desde n8n.
   - Registro de confirmación o ausencia de respuesta en Laravel como fuente de verdad.
   - Activación de llamada automatizada mediante Twilio Voice, disparada desde n8n si no existe confirmación previa.
   - Confirmación o cancelación mediante teclado numérico o interacción guiada.
   - Recepción de respuestas y eventos mediante webhooks seguros conectados al backend.
   - Cancelación y liberación automática de la franja si no hay respuesta a ninguna vía.

5. **Panel CRM y SaaS personalizable**
   - Gestión de servicios y precios.
   - Gestión de horarios de apertura.
   - Gestión de citas y estados.
   - Gestión de clientes.
   - Gestión de imágenes, logotipo, textos y galería.
   - Configuración de colores de marca y parámetros de fidelización.
   - Visualización de analíticas de ingresos y absentismo.

6. **Gamificación y fidelización**
   - Registro de citas completadas.
   - Acumulación de puntos o contador de visitas.
   - Desbloqueo de recompensas configurables, por ejemplo, lavado gratis al llegar a 6 cortes.
   - Visualización del progreso del cliente en home y área privada.

7. **Información estática y analítica operativa**
   - Publicación de precios del negocio: corte, barba y lavado.
   - Información de ubicación del local en Jerez de la Frontera.
   - Número de reservas por periodo.
   - Citas completadas, canceladas, confirmadas y rescatadas.
   - Vista resumida de ocupación e ingresos mensuales.

### Funcionalidades opcionales o futuras

1. Multiempresa o multi-tenant.
2. Gestión de varios empleados o barberos.
3. Pasarela de pago o señal para reserva.
4. Programa de fidelización avanzado con niveles y recompensas variables.
5. Reseñas de clientes.
6. Analítica avanzada con gráficos comparativos y exportación.
7. Notificaciones push complementarias y sincronización con calendarios externos.

### Priorización del alcance

| Prioridad | Funcionalidad                         | Inclusión en el proyecto final |
| --------- | ------------------------------------- | ------------------------------ |
| Alta      | Web pública responsive y PWA          | Sí                             |
| Alta      | Registro e inicio de sesión           | Sí                             |
| Alta      | Reserva y cancelación de citas        | Sí                             |
| Alta      | Gestión de horarios y servicios       | Sí                             |
| Alta      | WhatsApp API                          | Sí                             |
| Alta      | Twilio Voice                          | Sí                             |
| Alta      | Panel CRM personalizable              | Sí                             |
| Alta      | Gamificación y recompensas            | Sí                             |
| Alta      | Analíticas de ingresos y absentismo   | Sí                             |
| Media     | Marca configurable desde el CRM       | Sí                             |
| Media     | SaaS multi-tenant                     | No                             |
| Media     | Gestión multi-barbero                 | No                             |
| Baja      | Pagos online                          | No                             |

### Requisitos técnicos

#### Requisitos funcionales

- El cliente podrá reservar una cita desde móvil o escritorio.
- El sistema evitará reservas en franjas no disponibles.
- El administrador podrá modificar servicios, horarios y citas.
- El sistema enviará confirmaciones automáticas por WhatsApp y realizará llamadas de rescate cuando proceda.
- El sistema almacenará el historial de reservas y el progreso de fidelización.
- El administrador podrá personalizar la apariencia y los contenidos visibles de la web.
- El backend deberá registrar el resultado de cada interacción automática recibida desde n8n, WhatsApp o Twilio.

#### Requisitos no funcionales

- Interfaz responsive y usable en móvil.
- Soporte de instalación progresiva como PWA.
- Rendimiento adecuado en conexiones normales.
- Seguridad en autenticación y tratamiento de datos.
- Consistencia de la información en base de datos.
- Código estructurado y mantenible.
- Despliegue real en servidor accesible por Internet.
- Tolerancia a fallos en colas y tareas programadas.
- Idempotencia en los webhooks y en la actualización de estados para evitar acciones duplicadas.

#### Integraciones previstas en el MVP

- n8n como orquestador de workflows de automatización e integración.
- WhatsApp API de Meta para recordatorios y confirmaciones, conectada a través de n8n.
- Twilio Voice API para llamadas automatizadas de rescate, integrada mediante n8n.
- Endpoints y webhooks internos en Laravel para sincronizar estados de cita y respuestas de automatización.
- Servicio de almacenamiento de imágenes.
- Despliegue en servidor Linux con HTTPS.

### Viabilidad del alcance

El alcance final se ha definido con un criterio de **verticalidad funcional**: se implementan todos los pilares diferenciales de la idea original, pero en un contexto controlado y con una única implantación real. La viabilidad se apoya en cuatro decisiones: limitar el dominio a una sola barbería, mantener en Laravel toda la lógica crítica y el estado real de las citas, utilizar n8n solo como capa de integración externa y planificar el trabajo en iteraciones donde primero se resuelve el flujo crítico de negocio y después las capas de personalización y analítica.

---

## 5. Obligaciones legales y prevención (Criterio 1g)

### Normativa aplicable

#### Reglamento General de Protección de Datos (RGPD)

El sistema tratará datos personales de clientes, entre ellos:

- Nombre y apellidos
- Correo electrónico
- Teléfono
- Historial de reservas
- Información relacionada con servicios contratados
- Registros de confirmación y cancelación de citas

Por ello, será necesario cumplir con el RGPD y la normativa española de protección de datos, aplicando principios de:

- Licitud, lealtad y transparencia
- Limitación de la finalidad
- Minimización de datos
- Exactitud
- Limitación del plazo de conservación
- Integridad y confidencialidad

#### LOPDGDD

Además del RGPD, se tendrá en cuenta la **Ley Orgánica de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD)**, como desarrollo español complementario.

#### LSSI-CE

Al tratarse de una aplicación web con presencia pública, será de aplicación la **Ley de Servicios de la Sociedad de la Información y de Comercio Electrónico (LSSI-CE)**, especialmente en lo referente a:

- Identificación del titular del sitio
- Información de contacto
- Política de privacidad
- Política de cookies, si se utilizan cookies no técnicas
- Información clara sobre uso del servicio

#### Encargados de tratamiento y transferencias internacionales

Al integrar servicios de terceros como **Meta WhatsApp API** y **Twilio**, será necesario identificar correctamente a los encargados de tratamiento, revisar sus condiciones de procesamiento de datos y verificar las garantías aplicables en caso de transferencias internacionales de datos.

### Medidas de seguridad y protección de datos

Se contemplan las siguientes medidas:

- Contraseñas cifradas con algoritmos seguros.
- Comunicación cifrada mediante HTTPS.
- Control de acceso por roles diferenciando cliente y administrador.
- Validación estricta de entradas en frontend y backend.
- Protección frente a CSRF, XSS y consultas maliciosas.
- Limitación de intentos de acceso y medidas anti abuso.
- Copias de seguridad periódicas.
- Registro mínimo de actividad administrativa relevante.
- Gestión segura de credenciales y tokens de APIs externas mediante variables de entorno.
- Trazabilidad de los eventos de confirmación, cancelación y llamadas automatizadas.
- Registro y supervisión de ejecuciones automáticas entre Laravel, n8n y los servicios externos.
- Protección de endpoints y webhooks internos mediante autenticación, firma o claves compartidas.
- Política de minimización de datos: solo se solicitarán los datos estrictamente necesarios para reservar y gestionar la cita.

Además, se informará al usuario sobre:

- Finalidad del tratamiento.
- Base jurídica del tratamiento.
- Tiempo de conservación.
- Posibilidad de ejercer derechos de acceso, rectificación, supresión, oposición, limitación y portabilidad.
- Uso de canales de comunicación automatizada para recordatorios y rescate de citas.

### Accesibilidad web

El proyecto tendrá en cuenta criterios de accesibilidad conforme a las pautas **WCAG 2.2 nivel AA**, al menos en los aspectos más relevantes para el MVP:

- Contraste suficiente entre texto y fondo.
- Navegación mediante teclado.
- Formularios con etiquetas claras.
- Mensajes de error comprensibles.
- Estructura semántica HTML correcta.
- Estados visibles de foco.
- Botones y enlaces identificables.
- Diseño adaptable a distintos tamaños de pantalla.

### Prevención y buenas prácticas de desarrollo

Desde un enfoque de prevención técnica, se aplicarán buenas prácticas como:

- Uso de control de versiones.
- Desarrollo por ramas y revisiones periódicas.
- Entorno de pruebas antes de producción.
- Separación de configuración sensible mediante variables de entorno.
- Evitar dependencias innecesarias.
- Pruebas funcionales básicas de los flujos críticos.

---

## 6. Ayudas y subvenciones (Criterio 1h)

### Ayudas disponibles potencialmente aplicables

Aunque el proyecto se desarrolla con finalidad académica, resulta relevante identificar líneas de apoyo que podrían facilitar su implantación posterior en un entorno real. En todos los casos, la concesión dependerá de la **convocatoria vigente**, de los requisitos del solicitante y de la disponibilidad presupuestaria en el momento de la implantación.

#### Kit Digital

El **Kit Digital** es una ayuda orientada a la digitalización de pymes y autónomos. Aunque no está pensado para financiar directamente un proyecto académico, sí puede ser relevante para la barbería destinataria si decide implantar la solución en un entorno real tras su validación.

Aplicabilidad al proyecto:

- Puede encajar en las categorías de presencia en internet, gestión de procesos o gestión de clientes.
- Resulta útil como argumento de viabilidad económica futura.
- Refuerza el interés de la propuesta como solución real para un negocio pequeño.
- Sus requisitos habituales se orientan a autónomos o pequeñas empresas legalmente constituidas.
- Sus plazos dependen de cada convocatoria, por lo que habría que revisar la disponibilidad en el momento de solicitar la ayuda.

#### ENISA

Las líneas de financiación de **ENISA** están orientadas a empresas emergentes e iniciativas con potencial de crecimiento. No resultan aplicables a corto plazo para el desarrollo del TFG, pero sí podrían considerarse en una fase posterior si la solución evoluciona hacia un producto comercializable multiempresa.

Aplicabilidad al proyecto:

- Solo tendría sentido en una fase de producto y empresa, no durante el desarrollo académico inicial.
- Exigiría una estructura empresarial y un plan de negocio más avanzados que los contemplados en esta propuesta.

#### Programas de apoyo al emprendimiento

También pueden considerarse, en una etapa posterior:

- Programas de **Andalucía Emprende**
- Recursos de **CADE**
- Programas de **Acelera pyme**
- Apoyo de cámaras de comercio o viveros empresariales

Estas vías pueden resultar útiles para mentoría, validación de negocio, acompañamiento al emprendimiento o apoyo a la digitalización, aunque su alcance económico y sus requisitos son variables.

### Aplicabilidad real en este proyecto

A corto plazo, la ejecución del proyecto no dependerá de ayudas públicas. La estrategia de viabilidad se basará en:

- Tecnologías open source.
- Infraestructura de bajo coste.
- Alcance técnico controlado.
- Posible despliegue en una barbería real como caso de validación.

Esto es coherente con el objetivo académico del proyecto: demostrar que la solución puede desarrollarse y mantenerse con costes razonables.

### Recursos gratuitos o de bajo coste

Para minimizar costes, se emplearán recursos como:

- **Angular, Laravel, PostgreSQL, Redis, Docker y Filament**, todos ellos con versiones de uso libre.
- **n8n Community Edition** como plataforma de automatización de código abierto.
- **GitHub** para repositorio y control de versiones.
- **GitHub Actions** para automatización básica.
- **Cloudflare** en plan gratuito para DNS y capa básica de protección.
- **Meta WhatsApp Cloud API** para la mensajería automatizada.
- **Twilio Voice API** para llamadas automatizadas, con un coste inicial asumible para pruebas y validación.
- **VPS Linux de bajo coste** para despliegue final.
- **Figma** o herramienta equivalente para prototipado.
- **Draw.io** para diagramas.
- **Postman o Bruno** para pruebas de endpoints.
- **Toggl Track** o herramienta similar para seguimiento del tiempo.

### Valoración económica resumida

El MVP puede desarrollarse con una inversión muy reducida, centrada principalmente en:

- Dominio web
- VPS de producción
- Recursos de servidor suficientes para ejecutar Laravel, base de datos, Redis y n8n
- Saldo inicial para Twilio Voice
- Posibles costes asociados a la configuración y uso de WhatsApp API
- Tiempo de dedicación del desarrollador

Esto refuerza la viabilidad del proyecto como solución realista para un pequeño negocio local.

---

## 7. Guión de trabajo (Criterio 1i)

### Enfoque de planificación

El proyecto se desarrollará en **8 semanas**, equivalentes a **4 sprints de 2 semanas**, siguiendo una planificación incremental. Este enfoque permite:

- Entregar valor funcional desde fases tempranas.
- Revisar el alcance con frecuencia.
- Detectar riesgos pronto.
- Reservar tiempo para pruebas, correcciones y despliegue.

### Fases principales del desarrollo

1. Análisis y definición funcional
2. Diseño técnico y modelado de datos
3. Implementación del núcleo de reservas
4. Implementación del panel de administración
5. Automatización de recordatorios, webhooks e integración con n8n
6. Pruebas, accesibilidad y seguridad
7. Despliegue y documentación final

### Cronograma general

| Sprint / Semana       | Objetivos principales                                                                                                                                    | Entregables                                                                            |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Sprint 1. Semanas 1-2 | Análisis, benchmark, historias de usuario, arquitectura headless, definición del reparto de responsabilidades entre Laravel y n8n, modelo entidad-relación, wireframes, diseño del flujo anti-absentismo y entorno Docker | Documento de requisitos, backlog inicial, diseño de BD, prototipos y base del proyecto |
| Sprint 2. Semanas 3-4 | Desarrollo del frontend Angular, autenticación, web pública, panel de fidelización, servicios, horarios y sistema de reservas en tiempo real             | Flujo completo de registro, visualización y reserva funcionando en desarrollo          |
| Sprint 3. Semanas 5-6 | Backend Laravel, Filament CRM, personalización de branding, colas con Redis, despliegue de n8n e integración de WhatsApp API y Twilio Voice             | Backoffice funcional y motor anti-absentismo operativo                                 |
| Sprint 4. Semanas 7-8 | Analíticas, pulido PWA, pruebas funcionales, validación de accesibilidad, hardening de seguridad, despliegue y memoria técnica                            | MVP desplegado, probado y documentado                                                  |

### Hitos y entregas intermedias

#### Hito 1: Validación funcional del proyecto

Al final de la semana 2 deberá estar aprobado el alcance definitivo del MVP, con base de datos diseñada y arquitectura cerrada.

#### Hito 2: Reserva operativa de extremo a extremo

Al final de la semana 4 el sistema deberá permitir registrar usuarios y reservar citas correctamente.

#### Hito 3: Gestión administrativa y automatización

Al final de la semana 6 el administrador deberá poder gestionar la barbería, personalizar la web y el sistema deberá ejecutar el flujo de WhatsApp y llamada automatizada.

#### Hito 4: Cierre del MVP

Al final de la semana 8 el producto deberá estar desplegado, estable y listo para demostración.

### Herramientas de gestión del proyecto

Se utilizarán las siguientes herramientas:

- **GitHub Projects** para organizar tareas por columnas y prioridades.
- **GitHub Issues** para desglosar historias de usuario, bugs y mejoras.
- **Git** para control de versiones.
- **Toggl Track** o equivalente para medir tiempos reales de dedicación.
- **Figma** para wireframes y decisiones visuales.
- **Draw.io** para modelado y diagramas.
- **Notion o documento de seguimiento** para registrar decisiones técnicas y riesgos.

### Metodología de trabajo

La ejecución se organizará con un enfoque **iterativo e incremental**, inspirado en prácticas ágiles. A nivel operativo se combinarán:

- **Kanban** para visualizar el estado de las tareas y controlar el flujo de trabajo.
- **Sprints de dos semanas** para fijar objetivos cerrados y revisables.
- **Revisión al final de cada iteración** para comprobar avance real, riesgos y necesidad de reajustar prioridades.

Esta metodología es adecuada para un proyecto individual porque permite mantener control del alcance, detectar bloqueos con rapidez y asegurar que siempre exista una versión funcional en progreso.

### Criterios de control del alcance

Para evitar desviaciones, se aplicarán estas reglas:

- Todo lo que no forme parte del MVP definido quedará fuera del desarrollo principal.
- Las integraciones externas se abordarán desde el inicio porque forman parte del núcleo diferencial del proyecto.
- Se reservará tiempo específico para pruebas y despliegue, evitando dedicar las últimas semanas únicamente a programar.
- La prioridad será tener una versión estable y demostrable antes que añadir funcionalidades accesorias.

### Riesgos principales y mitigación

| Riesgo                                  | Impacto | Medida de mitigación                              |
| --------------------------------------- | ------- | ------------------------------------------------- |
| Exceso de alcance                       | Alto    | Definir MVP cerrado desde el inicio               |
| Problemas con integraciones externas    | Alto    | Implementar pruebas tempranas, usar n8n para aislar conectores y disponer de mocks de desarrollo |
| Complejidad operativa por nuevas piezas | Medio   | Mantener a Laravel como fuente de verdad y limitar n8n a la automatización externa |
| Duplicidad de eventos o webhooks        | Medio   | Diseñar endpoints idempotentes y registrar trazas por cita y ejecución |
| Retrasos en frontend                    | Medio   | Reutilizar componentes simples y diseño modular   |
| Complejidad del panel de administración | Medio   | Usar Filament para acelerar desarrollo            |
| Falta de tiempo para pruebas            | Alto    | Reservar la última iteración para QA y despliegue |

### Resultado esperado al finalizar los 2 meses

Al final del periodo de desarrollo se espera disponer de:

- Una aplicación web desplegada y accesible online.
- Un flujo completo de reserva y cancelación.
- Un panel CRM operativo y personalizable.
- Un sistema completo de automatización anti-absentismo con WhatsApp, llamada y cancelación automática.
- Un sistema de gamificación funcional y visible para el cliente.
- Un conjunto de pruebas y documentación suficiente para defender el proyecto ante tribunal.

---

## Conclusión

**The Good Barber** responde a una necesidad real de digitalización en pequeños negocios de cita previa, centrada especialmente en la reducción del absentismo y la mejora de la gestión diaria. La propuesta ha sido redimensionada con criterio técnico para que sea **viable, completa y defendible en un plazo de 2 meses por una sola persona**.

El proyecto combina valor de negocio, aplicabilidad real y un stack tecnológico moderno, pero razonable para el contexto de un estudiante de DAW. No pretende abarcar todas las posibilidades de una plataforma SaaS madura, sino construir una primera versión sólida con capacidad de evolucionar.

Desde el punto de vista académico, la propuesta permite demostrar competencias de análisis, diseño, desarrollo full stack, integración de APIs externas, automatización, seguridad, accesibilidad, despliegue y planificación. Desde el punto de vista profesional, plantea una solución con utilidad inmediata y potencial de crecimiento.

---

## Referencias

- Parlamento Europeo y Consejo de la Unión Europea. Reglamento (UE) 2016/679, Reglamento General de Protección de Datos (RGPD).
- Ley Orgánica 3/2018, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD).
- Ley 34/2002, de servicios de la sociedad de la información y de comercio electrónico (LSSI-CE).
- W3C. Web Content Accessibility Guidelines (WCAG) 2.2.
- Documentación oficial de Laravel.
- Documentación oficial de Angular.
- Documentación oficial de FilamentPHP.
- Documentación oficial de n8n.
- Documentación oficial de PostgreSQL.
- Documentación oficial de Redis.
- Documentación oficial de WhatsApp Cloud API (Meta).
- Documentación oficial de Twilio Voice API.
- Análisis de mercado de plataformas de reserva online: Booksy, Fresha, Treatwell y Timify.
