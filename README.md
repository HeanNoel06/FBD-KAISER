# FBD-KAISER
Nombre del Proyecto
TimeRoute

##Descripción

TimeRoute es un sistema de control y monitoreo de rutas de transporte basado en puntos de chequeo (checadores) con cálculo dinámico del tiempo estimado de llegada.
El sistema permite registrar en tiempo real la llegada de un chofer a cada punto de la ruta. Cada registro almacena la fecha y hora exacta en la base de datos, lo que permite calcular automáticamente el tiempo transcurrido entre checadores y actualizar los siguientes puntos.
Los alumnos pueden consultar desde un portal web cuánto tiempo falta para que el transporte llegue a su parada, mejorando la organización y reduciendo tiempos de espera innecesarios.

##Motivación

El transporte escolar o institucional frecuentemente presenta retrasos o adelantos que no pueden predecirse con horarios estáticos. Esto genera:
Incertidumbre para los alumnos
Tiempo de espera innecesario
Falta de información en tiempo real
Dificultad para monitorear el cumplimiento de rutas
TimeRoute nace con la finalidad de digitalizar el control de rutas y ofrecer un sistema dinámico que se adapte a las condiciones reales del trayecto, mejorando la experiencia tanto para estudiantes como para administradores y choferes.

##Objetivos del Proyecto

Controlar rutas mediante checadores ordenados.
Registrar tiempos reales de llegada.
Calcular tiempos promedio entre puntos.
Recalcular automáticamente el ETA después de cada registro.
Permitir consulta en línea del tiempo estimado.
Adaptarse dinámicamente ante retrasos o adelantos en la ruta.

##Tecnologias utilizadas

Java
JavaFX
CSS 
Backend Web
PHP
MySQL

##Arquitectura

Aplicación de escritorio en JavaFX para el registro de checadores.
Servidor PHP que expone servicios y gestiona la lógica de negocio.
Base de datos centralizada en MySQL.
Portal web para consulta de alumnos.

##Funcionamiento del Sistema

El administrador crea rutas y define los checadores en orden.
Se asigna una ruta, chofer y unidad para una fecha determinada.
El chofer inicia sesión en la aplicación JavaFX.
Al llegar a cada checador, registra su llegada.
El sistema guarda la fecha y hora real en MySQL.
Se calcula el tiempo transcurrido entre checadores.
Se recalculan automáticamente los tiempos estimados de llegada.
Los alumnos consultan desde el portal web en tiempo real.
