# FBD-KAISER
#### Nombre del Proyecto
TimeRoute

### Descripción

TimeRoute es un sistema de control y monitoreo de rutas de transporte basado en puntos de chequeo (checadores) con cálculo dinámico del tiempo estimado de llegada.
El sistema permite registrar en tiempo real la llegada de un chofer a cada punto de la ruta. Cada registro almacena la fecha y hora exacta en la base de datos, lo que permite calcular automáticamente el tiempo transcurrido entre checadores y actualizar los siguientes puntos.
Los alumnos pueden consultar desde un portal web cuánto tiempo falta para que el transporte llegue a su parada, mejorando la organización y reduciendo tiempos de espera innecesarios.

### Motivación

El transporte escolar o institucional frecuentemente presenta retrasos o adelantos que no pueden predecirse con horarios estáticos. Esto genera:
Incertidumbre para los alumnos
Tiempo de espera innecesario
Falta de información en tiempo real
Dificultad para monitorear el cumplimiento de rutas
TimeRoute nace con la finalidad de digitalizar el control de rutas y ofrecer un sistema dinámico que se adapte a las condiciones reales del trayecto, mejorando la experiencia tanto para estudiantes como para administradores y choferes.

### Objetivos del Proyecto

Controlar rutas mediante checadores ordenados.
Registrar tiempos reales de llegada.
Calcular tiempos promedio entre puntos.
Recalcular automáticamente el ETA después de cada registro.
Permitir consulta en línea del tiempo estimado.
Adaptarse dinámicamente ante retrasos o adelantos en la ruta.

### Herramientas utilizadas Tech Stack

## 1. Aplicación de Escritorio 

## Java 17
Java fue implementado como lenguaje principal para el desarrollo de la aplicación de escritorio. Permite estructurar el sistema bajo programación orientada a objetos, garantizando estabilidad, rendimiento y compatibilidad multiplataforma. Su versión LTS proporciona soporte a largo plazo y confiabilidad.

## JavaFX
JavaFX fue implementado como framework principal para la construcción de la interfaz gráfica. Permite el desarrollo de una interfaz moderna mediante FXML y CSS.

Funciones principales dentro del sistema:
- Inicio de sesión del chofer.
- Visualización de la ruta activa.
- Registro de llegada a checadores.
- Indicador dinámico del tiempo estimado de llegada (ETA).
- Separación entre lógica y diseño (arquitectura tipo MVC).

## Swing
Swing fue incorporado como librería complementaria para componentes gráficos adicionales. Proporciona soporte para ventanas secundarias, cuadros de diálogo y elementos específicos que requieren compatibilidad con componentes clásicos de Java.

## AWT
AWT forma parte de la base gráfica del entorno Java. Fue implementado como soporte para manejo de eventos, integración con el sistema operativo y funcionalidades gráficas fundamentales.

## 2. Backend – API REST

## PHP 8
PHP fue implementado como lenguaje del lado del servidor para gestionar la lógica de negocio del sistema. Centraliza el procesamiento de solicitudes y la comunicación entre los distintos componentes.

Permite:
- Autenticación de usuarios.
- Gestión de rutas y checadores.
- Registro de tiempos reales.
- Cálculo dinámico del ETA.
- Procesamiento de solicitudes HTTP.

## Apache (WampServer)
Apache fue implementado como servidor web dentro del entorno WampServer. Permite ejecutar los scripts PHP y administrar las peticiones HTTP provenientes de la aplicación de escritorio y del portal web.

## API REST
La arquitectura REST fue implementada para estructurar la comunicación entre clientes y servidor mediante métodos HTTP (GET, POST, PUT, DELETE).

Este enfoque permite:
- Separación entre frontend y backend.
- Escalabilidad del sistema.
- Integración futura con otras plataformas.

## JSON
JSON fue implementado como formato de intercambio de datos entre la aplicación JavaFX, el portal web y el backend. Permite una comunicación ligera y estructurada.

## 3. Base de Datos

## MySQL 8
MySQL fue implementado como sistema gestor de base de datos relacional para el almacenamiento estructurado de la información del sistema.

Gestiona:
- Rutas.
- Checadores.
- Choferes y unidades.
- Asignaciones.
- Registros de llegada.
- Historial de tiempos para cálculos promedio.

### Modelo Entidad–Relación (MER)
El modelo entidad–relación fue implementado como base conceptual para el diseño de la base de datos, definiendo claramente las entidades y sus relaciones.

Permite:
- Integridad referencial.
- Reducción de redundancia.
- Definición de relaciones 1:N y N:M.

## Modelo Relacional
El modelo relacional fue implementado para traducir el diseño conceptual en tablas estructuradas con claves primarias y foráneas, garantizando consistencia y normalización.

## 4. Portal Web (Alumno / Administrador)

## HTML5
HTML5 fue implementado para estructurar el contenido del portal web y organizar la información de consulta y administración.

## CSS3 (Personalizado)
CSS3 fue implementado para el diseño visual del portal, permitiendo una identidad gráfica propia sin el uso de frameworks externos.

## JavaScript (Vanilla JS)
JavaScript fue implementado para proporcionar interactividad en el lado del cliente.

Permite:
- Consulta del ETA en tiempo real.
- Actualización automática de datos.
- Comunicación con la API REST.

## Fetch API
Fetch API fue implementada para realizar solicitudes HTTP desde el navegador hacia la API REST, facilitando el intercambio de información en formato JSON.

## Chart.js
Chart.js fue implementado para la visualización gráfica de estadísticas y reportes, representando tiempos promedio y niveles de puntualidad.

## 5. Herramientas de Desarrollo

## Visual Studio Code
Visual Studio Code fue implementado como entorno principal de desarrollo para el backend, el portal web y la gestión general del proyecto.

## WampServer
WampServer fue implementado como entorno de desarrollo local, integrando Apache, PHP y MySQL en un solo entorno para pruebas e integración del sistema.

## Git
Git fue implementado como sistema de control de versiones, permitiendo el seguimiento de cambios y la gestión organizada del desarrollo.

## GitHub
GitHub fue implementado como plataforma de alojamiento del repositorio remoto, facilitando la documentación, control de versiones y presentación profesional del proyecto.

### Funcionamiento del Sistema

El administrador crea rutas y define los checadores en orden.
Se asigna una ruta, chofer y unidad para una fecha determinada.
El chofer inicia sesión en la aplicación JavaFX.
Al llegar a cada checador, registra su llegada.
El sistema guarda la fecha y hora real en MySQL.
Se calcula el tiempo transcurrido entre checadores.
Se recalculan automáticamente los tiempos estimados de llegada.
Los alumnos consultan desde el portal web en tiempo real.
