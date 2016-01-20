# Curso Basico de Spring
=
Antes de iniciar con el curso de Sping lo primero es definir que es un framework y que es Spring Framework

¿Que es un framework?
--------------

En ocaciones cuando trabajamos en cualquier plataforma solemos utilizar algún tipo de framework. Estos framework no son ni mas ni menos que un conjunto de clases que nos facilitan el trabajo cotidiano. Utilizamos el framework para crear un conjunto de objetos que nuestra aplicación necesita.

En la mayoría de las ocasiones para desarrollar la aplicación que necesitamos no nos es suficiente con usar un único framework sino que necesitamos utilizar varios frameworks.

Introducción a Spring Framework
---------------------

Este framework se caracteriza por el manejo de componentes a travez de **inyeccion de dependencias**

Inyección de dependencias
------

El objetivo es lograr un acoplamiento entre los objetos de nuestra aplicación. Con este patrón de diseño, los objetos no crean o buscan sus dependencias sino que éstas son dadas al objeto. El contenedor (la entidad que coordina cada objeto en el sistema) es el encargado de realizar este trabajo al momento de instanciar el objeto. Se invierte la responsabilidad en cuanto a la manera en que un objeto obtiene la referencia a otro objeto.

De esta manera, los objetos conocen sus dependencias por su interfaz. Así la dependencia puede ser intercambiada por distintas implementaciones a través del contenedor. En resumen, programaremos orientado a interfaces e inyectaremos las implementaciones a través del contenedor.
Programación orientada a aspectos

Se trata de un paradigma de programación que intenta separar las funcionalidades secundarias de la lógica de negocios. En inglés denominan a estas funcionalidades “cross-cutting concerns” algo que se traduciría como “preocupaciones transversales”. Por ejemplo los loggers, la seguridad, el manejo de transacciones, etc., son funcionalidades que atraviesan nuestro programa en varias abstracciones de éste. Por lo tanto corremos el riesgo de caer en la repetición de código y el acoplamiento entre nuestra lógica de negocios y la implementación de los cross-cutting concerns.

La AOP (Aspect-Oriented Programming) busca modularizar estos servicios y aplicarlos de manera declarativa a los componentes que deban afectar.

Módulos de Spring
--

<p align="center">
<img src="http://s14.postimg.org/p9fgl7yc1/Spring_Modulos.png">
</p>

El diagrama muestra los módulos con los que cuenta Spring (hasta la versión 2.5). En su núcleo (Core) se encuentra el BeanFactory – el contenedor fundamental de Spring y quien se encarga de la inyección de dependencias. El contenedor ApplicationContext se basa en BeanFactory y extiende su funcionalidad con soporte para i18n, eventos de ciclo de vida, validación y mejor integración con AOP.

- AOP – provee la implementación de AOP, permitiéndonos desarrollar interceptores de método y puntos de corte para desacoplar el código de las funcionalidades transversales.

- DAO – Provee una capa de abstracción sobre JDBC, abstrae el código de acceso a datos de una manera simple y limpia. Tiene una capa de expeciones sobre los mensajes de error provistos por cada servidor específico de base de datos. Además cuenta con manejo de transacciones a través de AOP.

- ORM – Provee la integración para las distintas APIs de mapeo objeto-relacional incluyendo JPA, JDO, Hibernate e iBatis.

- JEE – Provee integración con aplicaciones Java Enterprise Edition así como servicios JMX, JMS, EJB, etc.

- Web – Módulo que aporta clases especiales orientadas al desarrollo web e integración con tecnologías como Struts y JSF. Cuenta con el paquete Spring MVC, una implementación del conocido patrón de diseño aplicando los principios de Spring.
