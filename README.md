# Conociendo el robot NAO V6 en la Unisabana
Laboratorio desarrollado en el Laboratorio LUX de la Universidad de la Sabana para la materia Fundamentos de Robótica Móvil 2024-1 de la Universidad Nacional de Colombia.

**Integrantes**
* Felipe Cruz Vásquez
* Juan Sebastián Daleman
* Luis Alejandro Durán Espitia
  
Tabla de Contenidos
---
- [Introducción](#introducción)
- [Instalaciones y equipo](#instalaciones-y-equipo)
- [Robot usado](#robot-usado)
- [Entorno de desarrollo: Choregraphe](#entorno-de-desarrollo-choregraphe)
- [Programa usado](#programa-usado)
- [Código](#código)
- [Resultados](#resultados)
  - [Simulación](#simulación)
  - [Movimiento del robot](#movimiento-del-robot)
- [Otras actividades realizadas](#otras-actividades-realizadas)
- [Interacción con los robots](#interacción-con-los-robots)
- [Analisis y reflexión](#analisis-y-reflexión)
  - [Aprendizajes clave](#aprendizajes-clave)
  - [Aplicaciones prácticas](#aplicaciones-prácticas)
  - [Sugerencias de mejora](#sugerencias-de-mejora)
- [Preguntas](#preguntas) 
- [Conclusiones](#conclusiones)
- [Opiniones personales](#opiniones-personales)
- [Anexos](#anexos)


## Introducción

El ejercicio realizado en el Laboratorio Lux de la Universidad de la Sabana como parte de la materia Fundamentos de Robótica Móvil 2024-1 de la Universidad Nacional de Colombia, brindó una valiosa oportunidad para explorar las capacidades del robot NAO V6. Este robot antropomorfo, dotado de una diversidad de sensores y actuadores, ofrece un amplio espectro de posibilidades en el ámbito de la robótica móvil.

El NAO V6 se ha consolidado como una pieza esencial en el semillero de robótica de la Universidad de la Sabana, donde se emplea para participar en partidos de fútbol dentro de la Liga RoboCup SPL. Dotado con una amplia gama de sensores y actuadores, el NAO V6 permite a los estudiantes de ingeniería abordar los desafíos de la programación robótica en un entorno competitivo y dinámico. Estas competiciones son posibles gracias a la capacidad del robot para interactuar con el balón y otros robots.

El enfoque principal del NAO V6 es el de imitar lo más fielmente posible a un ser humano, lo cual se refleja en su integración de sensores y algoritmos de inteligencia artificial que le permiten detectar elementos y personas en su entorno. El robot puede identificar a las personas que lo rodean y entablar interacciones con ellas mediante gestos, diálogos y adaptación de sus acciones según atributos como la edad y el sexo, detectados a través de sus sensores y algoritmos.

En este proyecto, se exploraron las capacidades de programación del NAO V6 utilizando el software Choregraphe 2.8.7.4 de Aldebaran Robotics. Se desarrolló un programa que combina movimientos físicos del robot con mensajes verbales, demostrando así su capacidad para interactuar de manera multimodal con su entorno y con los usuarios.

## Instalaciones y equipo

El Laboratorio de Experiencias de Usuario, LUX (por su nombre en inglés), es un espacio interactivo y flexible construido para el acercamiento de los estudiantes a las herramientas informáticas. Aquí, los estudiantes desarrollan las prácticas de las clases fundamentales de la carrera de Ingeniería Informática, y tienen su primer contacto con la investigación en esta rama. El desarrollo de software y aplicaciones, el estudio de redes y comunicación así como la Introducción a la robótica, son solo tres de los múltiples campos trabajados en este laboratorio. El laboratorio LUX fue diseñado y construido como un ambiente adaptable a las necesidades de sus usuarios. Su tecnología permite una gran diversidad de posibilidades en la estructura de la enseñanza de las distintas clases allí impartidas, enmarcando un ambiente de aprendizaje continuo, en una atmósfera moderna y divertida para los estudiantes, investigadores y profesores.

En el laboratorio se tienen diferentes equipos importantes como un proyector para las presentaciones, diferentes puntos de conexión eléctrica para los equipos utilizados (robots y PC) así como puntos de conexión Ethernet para acceso a internet. Los equipos más relevantes disponibles en el laboratorio son los robots NAO y robot Bioloid para la enseñanza de robótica.

![Bioloid](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/a7c82372-bdf1-4987-b8a8-5bfbc2c56768)

## Robot usado

**NAO V6**

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/167ac246-14ec-4741-b303-95b04a9ac879)

Este es un robot antropomorfo el cual posee 25 grados de libertad, 7 sensores táctiles, 4 micrófonos y parlantes, reconocimiento de voz en 20 idiomas diferentes y 2 cámaras. Cuenta con diferentes API's de programación siendo compatible con Visual Studio Code, CLion y PyCharm; siendo posible programarlo con Java, Lenguaje de bloques, Python y C++.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/ef0b1bbe-e690-4ca6-88be-6a64a2abc70a)

## Entorno de desarrollo: Choregraphe

![Diapositiva1](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/0bf1d5be-691e-47e6-a15e-c4752a3ce47f)

En este entorno de desarrollo tenemos varios elementos como:
- **Barra de opciones:** En esta tenemos varias pestañas para manejo de conexión, archivos, edición del software, opciones de visualización y soporte para el uso del software.
- **Opciones de edición y conexión:** Acá encontramos herramientas para crear, abrir y guardar proyectos, desahacer y rehacer acciones, conexión al robot, cargar, depurar y ejecutar código.
- **Árbol de archivos del proyecto:** En esta sección visualizamos los archivos usados en el proyecto.
- **Bloques de programación:** En esta sección exploramos y vemos todos los bloques de programación disponibles para diferentes rutinas del robot.

![Diapositiva2](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/699c4995-cab7-4652-9b22-3ff3e77657bd)


- **Espacio de programación:** En este espacio es donde se arrastran los bloques y se conectan para progrmar el robot.
- **Linea de ejecución:** En esta parte podemos ver cómo se ejecuitará el código y los detalles en el tiempo de las acciones que se realizarán.
- **Ventan de simulación:** En esta parte veremos cómo actúa el robot de forma simulada con el código.

## Programa usado

Para programar el robot se usó el software Choregraphe 2.8.7.4 de la empresa Aldebaran, la cual es la creadora del robot NAO, el cual permite simular las acciones del robot y programarlo por medio de bloques. Adicionalmente, tienen diferentes bloques de movimientos de pruba como bailes o expresiones que puede tener el robot.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/b43ad82e-40f6-4126-9870-a49187e03e9f)


## Código

A continuación se muestra el programa en bloques que se usó, el cual consiste en que el robot diga una sarie de mensajes mientras realiza diferentes movimientos como sentarse, pararse y mover los brazos.

![image](https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/0fa04320-ced3-4f85-b00d-c0316ad7b9cc)

La secuencia empieza sentándose (sit down), luego se para (stand up), hace varios movimientosa de brazos y por último termina en la postura inical de pie.

## Resultados

### Simulación 

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/55536ab6-1ede-4aba-b40a-66d390bd6e8b

### Movimiento del robot

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/70998067/580b8fe2-9ebd-4d23-a884-60d549abe01a

## Otras actividades realizadas

A continuación, se presentan algunos videos que muestran otras capacides y rutinas del robot. Lo presentado a continuación son videos que se tomaron el día de la práctica, mas no fueron rutinas programadas por nosotros.

Este video muestra el último paso de una rutina predeterminada de Thai Chi:

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/96d65aa0-57eb-4f0c-b3fc-d6bf9931fdb5

Este video muestra los movimientos que realiza el robot en posición de arquero de fútbol:

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/c01edcb9-d1a6-47c4-aa64-41a82bd444ca

Este video muestra la interacción estándar predefinida cuando le tocan los pies al robot (el robot detecta el contacto y dirige la mirada hacia dónde lo tocaron):

https://github.com/JSDaleman/Robotica-movil-LabSabana/assets/45526932/31cf79ee-894e-40f0-a216-f912a85ca107

Asimismo se hicieron otras rutinas con el robot como:

- Comandos de voz donde se mostraba cómo el robot podía identificar palabras dadas por una persona.
- Control remoto donde se vió cómo a través de una conexión por SSH se podía manejar el robot de forma remota.
- Reconocimiento facial donde el robot con sus cámaras identificaba la presencia de rostros.

## Interacción con los robots

**Experencia práctica:** La interacción con los robots en las diferentes actividades fue con comandos de voz, por medio de cable Ethernet en el caso de programación propia, interacción con reconocimiento de una portería y el robot como portero, uso de luces y paralantes del robot para interacciones de baile y sonidos de acciones que realizaba.

**Desafíos encontrados:** La conexión entre el PC y el robot, debido al desconocimiento de la IP del robot, este no se podía configurar correctamente, lo cual se solucionó al oprimir el botón del pecho el robot. Al presionar dicho botón, el robot dictó su dirección IP para realizar la conexión.

**Resultados obtenidos:** Como se mostró en la sección de resultados, se logró crear una rutina de movimiento funcional en la cual el robot generaba sonidos mientras realizaba acciones. Se logró la familiaridad con el entorno de desarrollo Choregraphe. Se obtuvo la comprensión de la complejidad que tienen los robots humanoides con sistemas que utilizan diferentes mecanismos y eslabones para sus movimientos.

## Analisis y reflexión

### Aprendizajes clave

Entre los aprendizajes obtenidos de la visita, está el comprender que los robots humanoides poseen sistemas complejos cuyo análisis puede ser extenso dado que, según las condiciones y elementos del mecanismo, puede ser necesario tomar diferentes análisis para la comprensión completa. En cuanto a la progrmación, esta puede ser extensa y con diferentes consideraciones por la gran cantidad de elementos a controlar en el mecanismo, como sensores para mediciones de elementos del entorno del robot. Además, se debe tener cuidado de elementos del entorno como obstáculos o las interacciones con otros robots para actividades como jugar fútbol.

### Aplicaciones prácticas

**Entretenimiento:** El robot puede ser utilizado para el entretenimiento de los usuarios, desde niños hasta adultos. Su gran cantidad de acciones permiten que este interactúe con los usuarios como si fuera otro ser humano, generando entretención de las personas.

**Deportes:** Los robots pueden participar en actividades deportivas de equipo, tal como se vió en la Robo Cup de fútbol. Además, al ser robots humanoides, pueden adaptarse para realizar los movimientos requeridos de casi cualquier deporte.

**Acompañamiento:** El robot es bastante carismático, lo cual permite que sea usado como un elemento en el acompañamiento de personas. Este acompañamiento puede hacerse en niños (siendo el robot un juguete), o incluso en personas que se encuentren hospitalizadas. Es importante recalcar que el robot no suple la presencia humana, pero permite aligerar la soledad de una persona durante algún tiempo.

### Sugerencias de mejora

Para próximas visitas o actividades, se recomienda tener una guía para revisar previamente, que permita la instalación del software y entornos necesarios, con explicaciones sobre su funcionamiento. Asimismo, saber qué elementos o equipos propios (como PC) son necesarios en las prácticas, para que todos los estudiantes tengamos la posibilidad de llevar lo necesario.

## Preguntas

- ¿Por qué es importante estudiar y trabajar con robots humanoides en el campo de la robótica?
  - Pueden utilizar herramientas y dispositivos diseñados para humanos, facilitando su integración en entornos ya existentes sin necesidad de modificaciones significativas.
  - Su forma y comportamiento humanoides permiten una interacción más intuitiva y efectiva con las personas, aprovechando el lenguaje corporal y expresiones faciales para mejorar la comunicación.
  - Proporcionan plataformas complejas para desarrollar y probar algoritmos avanzados de inteligencia artificial, incluyendo el reconocimiento de voz, visión por computadora y toma de decisiones autónomas.
  - Integran una amplia gama de sensores y actuadores que imitan los sentidos y movimientos humanos, lo cual es crucial para la investigación en percepción y control.
  - Son especialmente útiles en entornos dinámicos y no estructurados, como hogares, hospitales y oficinas, donde pueden realizar diversas tareas que requieren adaptabilidad y flexibilidad.
  - Pueden realizar una variedad de tareas desde manipulación de objetos hasta asistencia a personas, lo que los hace extremadamente versátiles en comparación con otros tipos de robots.
  - La construcción de robots humanoides impulsa la innovación en áreas como el diseño mecánico, control de movimientos y equilibrio, proporcionando soluciones que pueden aplicarse a otros tipos de robots.
  - Estudiar y replicar el movimiento humano en robots lleva a un mejor entendimiento de la biomecánica y puede tener aplicaciones en medicina y rehabilitación.
  - Los robots humanoides tienen un gran potencial en mercados como el de servicios personales, salud y educación, donde pueden mejorar la calidad de vida y aliviar la carga de trabajo humano.

- ¿Qué características distintivas tienen los robots NAO que los hacen útiles para la enseñanza y la investigación?
  - **Apariencia No Intimidante:** El diseño amigable y compacto de NAO (58 cm de altura) lo hace atractivo y no intimidante para estudiantes de todas las edades, facilitando su uso en entornos educativos.
  - **Articulaciones y Movimientos Humanos:** NAO cuenta con 25 grados de libertad (DOF), lo que le permite realizar una amplia gama de movimientos y gestos humanos, enriqueciendo las interacciones.
  - **Choregraphe:** Esta herramienta de software permite a los usuarios programar NAO a través de una interfaz gráfica intuitiva, ideal para principiantes y aquellos sin experiencia previa en programación.
  - **Soporte Multilenguaje:** NAO es compatible con varios lenguajes de programación, incluyendo Python, C++, Java y MATLAB, ofreciendo flexibilidad a los investigadores y educadores para elegir el entorno que mejor se adapte a sus necesidades.
  - **Sensores Integrados:** La amplia gama de sensores que tiene integrado desde cámaras, micrófonos, sensores táctiles en la cabeza, manos y pies, junto con sensores de fuerza en las articulaciones, permiten la interacción física y la retroalimentación sensorial.
  - **Conexión Inalámbrica:** NAO puede conectarse a redes Wi-Fi, lo que facilita la comunicación remota y la integración con otros dispositivos y sistemas.
  - **Batería Recargable:** La batería de larga duración de NAO permite sesiones prolongadas de uso sin interrupciones frecuentes, esencial para la enseñanza y los experimentos continuos.
  - **Documentación Extensa:** NAO viene con una documentación detallada y recursos educativos que ayudan a los usuarios a maximizar su potencial en la enseñanza y la investigación.

## Conclusiones

El desarrollo de este proyecto nos permitió adquirir una comprensión más profunda de las capacidades y limitaciones del robot NAO V6, así como de las herramientas de programación disponibles para trabajar con él. Algunas de las conclusiones clave que obtuvimos incluyen:

- **Versatilidad del NAO V6:** El robot demostró una amplia gama de capacidades, desde movimientos físicos complejos hasta reconocimiento y generación de voz.
- **Facilidad de programación:** El software Choregraphe proporcionó una interfaz intuitiva para programar el robot mediante bloques, lo que facilitó el desarrollo del programa.
- **Interacción multimodal:** Logramos crear una experiencia de interacción multimodal, combinando movimientos físicos con mensajes verbales, lo que resalta el potencial del NAO V6 para aplicaciones de asistencia y entretenimiento.
- **Motivación:** Los robots NAO V6 generan motivación en estudiantes para interactuar con ellos, realizar pruebas y aprender, debido a su apariencia física con tecnología de punta.

## Opiniones personales

- **Juan Daleman:** Esta experencia considero que es importante ya que la interacción con equipos robóticos permite comprender de una mejor manera las aplicaciones que se han estudiado en el curso, además de que la experencia con los NAO por sus características lo devuelven a uno a como cuando era niño con un juguete despertando la curiosidad no solo de cómo funciona sino de cómo usarlo. Despierta un interés grande en cómo usar y programar un robot ya sea para hacer rutinas sencillas o solo para ver ciertos comportamientos autómatas interesantes como puede ser hacer Tai Chi o bailar, me recordó mucho el cómo me comenzó a interesar la robótica y la belleza de ver cómo funcionan las máquinas.
- **Felipe Cruz:** Yo ya conocía los robots NAO de la Universidad de la Sabana, los conocí cuando estaba buscándo dónde estudiar y a qué universidad entrar. En su momento, me llenó de interés ver cómo se mueven los robots e interactúan con su entorno, pero no entendía nada de la tecnología que hay detrás. Después de esta experiencia en el laboratorio LUX, me alegra haber cursado toda la carrera de Ingeniería Mecatrónica y poder entender el trasfondo tecnológico que hay detrás de los robots, en especial los NAO. Me motiva a seguir adelante con la investigación en robótica, pues entiendo la tecnología que se utiliza, y me interesa seguir utilizando elementos investigativos como el robot NAO, desarrollando nuevos algoritmos que puedan aplicarse en la solución de problemas reales.
- **Alejandro Durán:** Como se ha tratado ya varias veces en el desarrollo del curso, me parece muy enriquecedor para el aprendizaje poder ver la aplicación práctica de los temas vistos en clase, así como esta oportunidad de dispner de un espacio nuevo en el que también se observan los avances de colegas de otras universidades, a nivel personal me pareció bastante interesante todo el asunto de las competencias en las que ha participado este equipo, y así mismo cómo nos describieron estos espacios, los cuales escuchando lo estimulante y propicios para el conocimiento que son por la manera en que se trata de que todos presenten sus avances con todos para generar un mayor impacto en este dearrollo de proyectos, me motiva incluso a plantearme la posibilidad de alguna vez con un proyecto interesante presentarme yo mismo en estos espacios de ser posible.
## Anexos

- [Guia de usuario](https://www.aldebaran.com/en/support/nao-6/1-meet-nao)
- [Robocup](https://www.youtube.com/watch?v=LBTdMKiuRvY)
- [Documentación del NAO V6](http://doc.aldebaran.com/2-8/home_nao.html)


