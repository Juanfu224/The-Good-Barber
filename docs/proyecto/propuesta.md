# The Good Barber

Tu barbería de confianza desde 2013

## 1. Descripción

La web de The Good Barber es la plataforma digital de una peluquería de caballeros y barbería low cost situada en Jerez de la Frontera (Cádiz). Su función principal es ofrecer una solución de gestión integral (SaaS) que digitaliza y automatiza por completo el negocio.

Para potenciar al máximo la rentabilidad del negocio y reducir drásticamente el absentismo, es decir, los clientes que reservan pero no asisten, el core de la aplicación es un motor automatizado basado en eventos y colas que gestiona el rescate de citas. La plataforma permite a los clientes gestionar reservas en tiempo real interactuando con un sistema de fidelización gamificado, mientras que el administrador obtiene un control total del negocio a través de un panel CRM completo, desde el cual puede personalizar la web al completo y analizar el rendimiento del local.

## 2. Funcionalidades Principales

- Gestión de reservas en tiempo real: funcionalidad clave para agendar, consultar o cancelar cortes de pelo o arreglos de barba desde una interfaz web interactiva y altamente optimizada.
- Motor automatizado anti-absentismo: sistema backend robusto diseñado para garantizar la asistencia y optimizar el calendario del barbero.
  - Aviso 24h: un día antes de la cita, el cliente recibe una notificación automática por WhatsApp utilizando la API de Meta para confirmar su asistencia.
  - Llamada automatizada de rescate: si el cliente no confirma mediante WhatsApp, el sistema se conecta a la API de Twilio para realizar una llamada telefónica automatizada en la que el usuario podrá confirmar o cancelar usando su voz o el teclado numérico.
  - Cancelación y liberación automática: si no hay respuesta a ninguna de las vías anteriores, el sistema cancela la cita automáticamente liberando el hueco en tiempo real.
- Panel CRM y SaaS personalizable: el administrador dispone de un panel de control donde gestionará analíticas de ingresos y absentismo. Además, este panel permite una personalización total estilo plantilla: cambiar horarios, precios, parámetros de fidelización, colores de la web, logotipo, imágenes de la galería y textos.
- Frontend interactivo con gamificación: sistema de fidelización donde el cliente acumula puntos por asistencia y desbloquea servicios gratuitos, por ejemplo lavado gratis al llegar a 6 cortes, incentivando la retención sin generar carga manual al barbero.
- Información estática clara: listado de precios (Corte 9.50 euros, Barba 6.50 euros, Lavado 2.00 euros) e información de ubicación en la Plaza Princi Jerez.

## 3. Objetivos y flujo del usuario

El objetivo primordial es ofrecer una herramienta SaaS robusta que garantice la máxima asistencia y rentabilidad para el negocio, a la vez que el usuario final consigue su cita de forma rápida y se fideliza mediante la gamificación.

### Flujo de usuario estándar (Frontend web)

1. Home y gamificación: el usuario entra y visualiza un panel interactivo y motivacional con su progreso de fidelización, por ejemplo: Llevas 4 de 6 cortes.
2. Reserva en tiempo real y canje: navega a la sección de reservas, selecciona fecha y hora disponible y, si tiene una recompensa desbloqueada, el sistema le aplica el descuento automáticamente, por ejemplo dejándolo a 0.00 euros.
3. Confirmación: el cliente recibe la validación instantánea de su cita en pantalla.

### Flujo de confirmación anti-absentismo (Backend)

- 24 horas antes: el sistema ejecuta un job en cola que envía un WhatsApp con un mensaje como: Hola, te recordamos tu cita mañana a las 17:30 para arreglo de barba. ¿Nos confirmas que asistes? Responde SÍ o NO.
- 4 horas antes, si no hay confirmación: el motor activa la API de voz de Twilio y realiza una llamada con un mensaje como: Hola, te llamamos de The Good Barber. Tienes una cita hoy a las 17:30. Pulsa 1 para confirmar, pulsa 2 para cancelar.
- Si no contesta: se envía un mensaje por WhatsApp indicando que se intentó confirmar la cita, no hubo respuesta y la reserva se ha cancelado automáticamente, invitando a volver a reservar desde la página web.

### Flujo del Administrador (SaaS/CRM)

1. Accede al panel de control para revisar las gráficas de ingresos mensuales y la tasa de citas rescatadas por el sistema automatizado.
2. Accede a la configuración web para actualizar una foto de la galería, cambiar el color principal de la marca o modificar el precio de un servicio, viéndose reflejado en el frontend al instante.

## 4. Decisiones de Diseño y Experiencia de Usuario (UX)

Para garantizar el éxito comercial de la plataforma, el desarrollo será mobile first.

- Modernización visual y personalización: diseño atractivo con una paleta de colores y tipografías que el propio dueño del negocio puede adaptar desde el CRM. Se incluye prueba social mediante galería y reseñas.
- Fidelización en primer plano: el panel visual de progreso estará siempre accesible de forma clara, motivando a los clientes a volver y aumentando drásticamente la retención.
- Interactividad sin fricción: interfaces de reserva muy limpias, con uso de un sticky CTA, es decir, un botón flotante, para facilitar la conversión en cualquier punto de la navegación.

## 5. Arquitectura, tecnología y herramientas

El proyecto empleará una arquitectura headless avanzada para separar estrictamente el complejo motor del backend, el frontend interactivo y el panel CRM.

### Frontend (Web y PWA)

- Framework: Angular 21+ standalone con Signals y Zoneless para asegurar una PWA ultraligera y de carga inmediata.
- Estilos y componentes: ITCSS + SASS con metodología BEM para una arquitectura de estilos modular y adaptable desde el panel de control, junto a Angular CDK para accesibilidad e interacciones.

### Backend (Lógica core, motor anti-absentismo y CRM)

- Framework core: Laravel 12 con API Resource. Actuará como orquestador central, manejando la compleja lógica de tiempos con Carbon.
- Arquitectura de automatización: uso intensivo de Cron Jobs y Redis para el manejo de colas y eventos asíncronos. Este sistema será el encargado de escanear constantemente las citas y disparar los flujos de WhatsApp, llamadas automatizadas y auto-cancelaciones sin saturar el servidor.
- Panel de administración (CRM): FilamentPHP. Proporcionará la interfaz completa de gestión, analíticas y personalización SaaS para el administrador.
- Base de datos: PostgreSQL 18 para garantizar la integridad y fiabilidad relacional de las reservas, usuarios y métricas.

### Integraciones Externas y APIs

- WhatsApp API (Meta): para el envío automatizado de recordatorios 24 horas antes de la cita de forma gratuita.
- Twilio Voice API: integración fundamental para la ejecución y recolección de interacciones mediante teclado o voz en las llamadas de rescate telefónico. Se necesita un monto inicial de 20 dólares para poder utilizar esta API.

### Infraestructura (DevOps)

- Entorno: Docker con Laravel Sail para garantizar una paridad exacta entre el desarrollo local y producción.
- CI/CD y testing: GitHub Actions y Laravel Forge para el despliegue continuo.