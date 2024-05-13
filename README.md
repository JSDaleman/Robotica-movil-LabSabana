# Conociendo el robot NAO V6 en la Unisabana
Laboratorio desarrollado en el Laboratorio LUX de la Universidad de la Sabana para la materia Fundamentos de Robótica Móvil 2024-1 de la Universidad Nacional de Colombia.

**Integrantes**
* Felipe Cruz Vásquez
* Juan Sebastián Daleman
* Luis Alejandro Durán Espitia
  
Tabla de Contenidos
---
- [Introducción](#introducción)
- [Robot usado](#robot-usado)
- [Programa usado](#programa-usado)
- [Código](#código)
- [Resultados](#resultados)
  - [Simulación](#simulación)
  - [Movimiento del robot](#movimiento-del-robot) 
- [Conclusiones](#conclusiones)
- [Videos extra](#videos-extra)


## Introducción

El ejercicio realizado en el Laboratorio Lux de la Universidad de la Sabana como parte de la materia Fundamentos de Robótica Móvil 2024-1 de la Universidad Nacional de Colombia, brindó una valiosa oportunidad para explorar las capacidades del robot NAO V6. Este robot antropomorfo, dotado de una diversidad de sensores y actuadores, ofrece un amplio espectro de posibilidades en el ámbito de la robótica móvil.

El NAO V6 se ha consolidado como una pieza esencial en el semillero de robótica de la Universidad de la Sabana, donde se emplea para participar en partidos de fútbol dentro de la Liga RoboCup SPL. Dotado con una amplia gama de sensores y actuadores, el NAO V6 permite a los estudiantes de ingeniería abordar los desafíos de la programación robótica en un entorno competitivo y dinámico. Estas competiciones son posibles gracias a la capacidad del robot para interactuar con el balón y otros robots.

El enfoque principal del NAO V6 es el de imitar lo más fielmente posible a un ser humano, lo cual se refleja en su integración de sensores y algoritmos de inteligencia artificial que le permiten detectar elementos y personas en su entorno. El robot puede identificar a las personas que lo rodean y entablar interacciones con ellas mediante gestos, diálogos y adaptación de sus acciones según atributos como la edad y el sexo, detectados a través de sus sensores y algoritmos.

En este proyecto, se exploraron las capacidades de programación del NAO V6 utilizando el software Choregraphe 2.8.7.4 de Aldebaran Robotics. Se desarrolló un programa que combina movimientos físicos del robot con mensajes verbales, demostrando así su capacidad para interactuar de manera multimodal con su entorno y con los usuarios.

## Robot usado
**NAO V6**

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/167ac246-14ec-4741-b303-95b04a9ac879)

Este es un robot antropomorfo el cual posee 25 grados de libertad, 7 sensores táctiles, 4 micrófonos y parlantes, reconocimiento de voz en 20 idiomas diferentes y 2 cámaras. Cuenta con diferentes API's de programación siendo compatible con Visual Studio Code, CLion y PyCharm; siendo posible programarlo con Java, Lenguaje de bloques, Python y C++.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/ef0b1bbe-e690-4ca6-88be-6a64a2abc70a)

## Programa usado

Para programar el robot se usó el software Choregraphe 2.8.7.4 de la empresa Aldebaran, la cual es la creadora del robot NAO, el cual permite simular las acciones del robot y programarlo por medio de bloques. Adicionalmente, tienen diferentes bloques de movimientos de pruba como bailes o expresiones que puede tener el robot.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/b43ad82e-40f6-4126-9870-a49187e03e9f)


## Código

A continuación se muestra el programa en bloques que se usó, el cual consiste en que el robot diga una sarie de mensajes mientras realiza diferentes movimientos como sentarse, pararse y mover los brazos.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/0fa04320-ced3-4f85-b00d-c0316ad7b9cc)

La secuencia empieza sentándose, luego se para, hace varios movimientosa de brazos y por ultimo termina en la postura inical de pie.

## Resultados

### Simulación 

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/55536ab6-1ede-4aba-b40a-66d390bd6e8b

### Movimiento del robot

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/580b8fe2-9ebd-4d23-a884-60d549abe01a

## Conclusiones

El desarrollo de este proyecto nos permitió adquirir una comprensión más profunda de las capacidades y limitaciones del robot NAO V6, así como de las herramientas de programación disponibles para trabajar con él. Algunas de las conclusiones clave que obtuvimos incluyen:

- **Versatilidad del NAO V6:** El robot demostró una amplia gama de capacidades, desde movimientos físicos complejos hasta reconocimiento y generación de voz.
- **Facilidad de programación:** El software Choregraphe proporcionó una interfaz intuitiva para programar el robot mediante bloques, lo que facilitó el desarrollo del programa.
- **Interacción multimodal:** Logramos crear una experiencia de interacción multimodal, combinando movimientos físicos con mensajes verbales, lo que resalta el potencial del NAO V6 para aplicaciones de asistencia y entretenimiento.

## Videos extra

A continuación, se presentan algunos videos que muestran otras capacides y rutinas del robot. Lo presentado a continuación son videos que se tomaron el día de la práctica, mas no fueron rutinas programadas por nosotros.

Este video muestra el último paso de una rutina predeterminada de Thai Chi:

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/96d65aa0-57eb-4f0c-b3fc-d6bf9931fdb5

Este video muestra los movimientos que realiza el robot en posición de arquero de fútbol:

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/c01edcb9-d1a6-47c4-aa64-41a82bd444ca

Este video muestra la interacción estándar predefinida cuando le tocan los pies al robot (el robot detecta el contacto y dirige la mirada hacia dónde lo tocaron):

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/31cf79ee-894e-40f0-a216-f912a85ca107
