# Proyecto de Control y Simulación de Mecanismos con Simulink y Simscape

Este repositorio documenta el desarrollo, simulación y control de mecanismos físicos utilizando **Simulink**, **Simscape Multibody** y hardware de adquisición de datos. El proyecto se basa en prácticas de laboratorio con motores DC, sensores de corriente, encoders, y mecanismos físicos como péndulos invertidos, helicópteros y volantes.

##  Objetivo

Desarrollar un sistema de control en cascada para mecanismos físicos (posición y velocidad), integrando simulación en Simulink/Simscape con pruebas físicas mediante hardware-in-the-loop (HIL). El sistema debe ser capaz de controlar un mecanismo diseñado por el estudiante, el cual será accionado por un motor DC real.

##  Plataformas y Plantas Utilizadas

- **Péndulo Invertido**  
  Controlado mediante torque aplicado por un motor DC. Se busca estabilizarlo usando retroalimentación de posición angular.

- **Helicóptero 2 DOF**  
  Simula control de orientación en dos ejes. Se trabaja con sensores de posición y velocidad.

- **Volante con mecanismo de equilibrio**  
  Usa un tornillo sin fin para inclinar varillas que equilibran una esfera.

##  Componentes del Sistema

- **Motor DC** con driver de potencia y sensores integrados (corriente, encoder, velocidad).
- **Tarjeta de adquisición de datos (DAQ)** con entradas/salidas analógicas y digitales.
- **Sensores**:
  - Corriente (analógica)
  - Encoder (posición y velocidad)
  - Giroscopio y acelerómetro (en algunos kits)
- **Plantas físicas**:
  - Péndulo invertido
  - Helicóptero con 2 DOF
  - Volante con mecanismo de equilibrio

##  Herramientas Utilizadas

- **Simulink + Simscape Multibody**: para modelado físico.
- **Bloques HIL**:
  - HIL Init: Configura la comunicación con la tarjeta.
  - HIL Write: Envía señales de control (voltaje o PWM).
  - HIL Read: Lee sensores (corriente, velocidad, estado).
- **Simulación estructural previa** (opcional) en SolidWorks.

##  Flujo de Trabajo

1. Diseño del mecanismo físico (ligero, funcional, acoplado al eje del motor).
2. Modelado en Simscape.
3. Implementación del control en Simulink.
4. Simulación con gemelo digital.
5. Pruebas físicas con el motor real.
6. Captura y análisis de datos (corriente, velocidad, posición).

##  Resultados Esperados

- Curvas de corriente y velocidad del motor.
- Validación del control de posición y velocidad.
- Comparación entre simulación y comportamiento físico.
- Evaluación de eficiencia y precisión del sistema.

##  Consideraciones de Diseño

- El mecanismo debe cumplir una función real (ej. etiquetado, soldadura).
- Movimiento generado por un solo motor.
- Materiales ligeros para evitar sobrecarga.
- Acondicionamiento de señales (voltaje/PWM).
- Protección contra bloqueo mecánico (detección de errores).

##  Detalles del Proyecto

### Péndulo Invertido
- Simulación: Modelado en Simscape Multibody.
- Control: Cascada para estabilización vertical.
- Sensores: Posición angular.

### Helicóptero 2 DOF
- Simulación: Control de orientación en dos ejes.
- Sensores: Posición y velocidad.
- Control: Cascada para mantener orientación deseada.

### Volante con Equilibrio
- Simulación: Tornillo sin fin que inclina varillas.
- Control: Mantener equilibrio de una esfera.

##  Implementación Práctica

- Diseño del mecanismo: Materiales ligeros, montaje al eje del motor.
- Simulación: Validación previa en entorno digital.
- Control: Cascada con retroalimentación.
- Pruebas físicas: Validación con sensores reales.
- Análisis de datos: Curvas de corriente, velocidad, posición.

##  Conclusión

Este proyecto permite comprender la interacción entre modelos físicos y sistemas de control, integrando simulación y hardware real. La metodología HIL facilita el desarrollo de soluciones robustas y aplicables a sistemas reales, promoviendo el aprendizaje práctico en ingeniería de control y mecatrónica.

