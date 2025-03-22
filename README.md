# Project Valkyrie

## 1. Introducción

Este documento describe el diseño y la fabricación de dos aviones RC impresos en 3D, equipados con Inteligencia Artificial (IA) para simular combates aéreos autónomos.

El proyecto se divide en varias fases, incluyendo el desarrollo de una emisora personalizada tipo HOTAS, un sistema FPV con seguimiento de cabeza y HUD, y la implementación de capacidades de vuelo autónomo y combate aéreo simulado.

## 2. Objetivos del Proyecto

Los objetivos del proyecto son:

* Diseñar y fabricar dos aviones RC utilizando tecnología de impresión 3D.
* Implementar IA en cada avión para el control autónomo y la simulación de combate aéreo.
* Desarrollar una emisora personalizada tipo HOTAS para el control manual de los aviones.
* Integrar un sistema FPV con seguimiento de cabeza para una experiencia de vuelo inmersiva.
* Interceptar y modificar la señal de video FPV para añadir un HUD.
* Implementar un sistema de vuelo autónomo con maniobras básicas y posicionamiento preciso.
* Simular combates aéreos entre los aviones, incluyendo estrategias y sistemas de daños.

## 3. Fases del Proyecto

El proyecto se desarrollará en las siguientes fases:

### 3.1 Fase 1: Inmersión FPV

* Implementación de un sistema FPV con giroscopio en las gafas y servos en la cámara para replicar el movimiento de la cabeza del piloto.
* Fabricación de una nueva emisora de radio con un módulo ESP32 NodeMCU.
* Conexión de la información del giroscopio y los potenciómetros de un joystick Thrustmaster a la ESP32.
* Envío de la información al avión mediante un módulo de radio.
* Utilización de un módulo transmisor con la tecnología ExpressLRS, conectado a la ESP32 mediante el protocolo CRSF.
* En el avión, se utilizará una placa Raspberry Pi 3 que gestionará, mediante ROS2, los cálculos para pasar de la información del giroscopio a grados, entre otras posibles implementaciones.
* Se utilizará una controladora de vuelo Pixhawk que se comunicará mediante MAVLink/MAVROS con la Raspberry Pi 3, y mediante SBUS con el receptor de radio.

### 3.2 Fase 2: Vuelo Autónomo e IA

* Implementación de un sistema de inteligencia artificial para vuelo autónomo.
* Desarrollo de maniobras de vuelo autónomo, incluyendo despegue, aterrizaje y vuelo en círculos.
* Desarrollo de un sistema para obtener la posición exacta del avión en tiempo real (altura, coordenadas, etc.).
* Integración de un sistema de alarmas realista, similar al de aviones como el F18.

### 3.3 Fase 3: Combate Aéreo Simulado

* Fabricación de un segundo avión con capacidad autónoma e IA.
* Implementación de un sistema de combate aéreo simulado.
* Desarrollo de maniobras y estrategias de combate aéreo (piloto vs IA e IA vs IA).
* Utilización de la información de posición de la Fase 2 para el combate simulado.
* Implementación de un sistema de daños que afecte el control del avión según el impacto simulado.
* Ampliación del sistema de alarmas con nuevos avisos.
