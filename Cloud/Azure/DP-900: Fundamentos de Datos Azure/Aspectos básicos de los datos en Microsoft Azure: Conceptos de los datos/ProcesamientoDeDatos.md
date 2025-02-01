# Procesamiento de datos

## Procesamiento de datos transaccionales

Función principal de la informática empresarial \
Un sistema transaccional registra las transacciones que encapsulan eventos específicos de los que la organización quiere realizar un seguimiento \
Los sistemas transacionales suelen ser de gran volumen; a veces, controlan muchos millones de transcaciones en un solo dia \
El trabajo que realizan los sistemas transaccionales se conoce como _**OnLine Transactional Processing (OLTP)**_

Las soluciones OLTP se basan en un sistema de base de datos en el que el almacenamiento de datos está optimizado 
tanto para las operaciones de lectura como para las de escritura \
Con el fin de admitir cargas de trabajo transaccionales en las que se crean, recuperan, actualizan y eliminan registros de datos \
Estas operaciones se aplican transaccionalmente, de una forma que garantiza la integridad de los datos almacenados en la base de datos (ACID)

- **Atomicity** (Atomicidad): Cada transacción se trata como una unidad única, la cual se completa correctamente o produce un error general
- **Consistency** (Coherencia): Las transacciones solo pueden pasar los datos de la base de datos de un estado válido a otro
- **Isolation** (Aislamiento): Las transacciones simultáneas no pueden interferir entre sí y deben dar lugar a un estado coherente de la base de datos
- **Durability** (Durabilidad): Cuando se ha confirmado una transacción, permanece confirmada

Los sistemas OLTP suelen usarse para admitir aplicaciones activas que procesan datos empresariales, a menudo denominadas aplicaciones _**Line Of Business (LOB)**_

## Procesamiento de datos analíticos

Usa sistemas de solo lectura (o principalmente de lectura) que almacenan grandes volúmenes de datos históricos o métricas empresariales \
Los análisis pueden basarse en una instantánea de los datos en un momento concreto o en una serie de instantáneas

### Arquitectura común para el análisis a escala empresarial

- Los archivos de datos se pueden almacenar en un lago de datos central para analizarlos
- Un proceso de extracción, transformación y carga (**ETL**) permite copiar datos de archivos y bases de datos OLTP en 
  un almacenamiento de datos optimizado para la actividad de lectura
- Los datos del almacenamiento de datos se pueden agregar y cargar en un modelo _**OnLine Analytical Processing (OLAP)**_ o un cubo.
  Los valores numericos agregados (medidas) de las tablas de hechos se calculan para intersecciones de dimensiones a partir de tablas de dimensiones
- Los datos del lago de datos, el almacenamiento de datos y el modelo analítico se pueden consultar para generar informes, visualizaciones y paneles

Los lagos de datos (_**Data lakes**_) son comunes en escenarios de procesamiento analítico de datos modernos, 
en los que se debe recopilar y analizar un gran volumen de datos basados en archivos

Los almacenamientos de datos (_**Data warehouses**_) son un recurso establecido para almacenar datos en un esquema 
relacional optimizado para operaciones de lectura, principalmente consultas para admitir informes y visualización de datos

Un _**modelo OLAP**_ es un tipo agregado de almacenamiento de datos optimizado para cargas de trabajo analíticas. Las 
agregaciones de datos se encuentran en diferentes dimensiones y distintos niveles, lo que permite rastrear agrupando 
datos y explorar en profundidad las agregaciones en varios niveles jerárquicos. Dado que los datos de OLAP se agregan 
previamente, las consultas para devolver los resumenes que contiene se pueden ejecutar rapidamente

### Diferentes tipos de usuario

- Los _**científicos de datos**_ pueden trabajar directamente con archivos de datos en un lago de datos para explorar los datos y crear modelos a partir de estos
- Los _**analistas de datos**_ pueden consultar tablas directamente en el almacenamiento de datos para generar informes y visualizaciones complejos
- _**Los usuarios profesionales**_ pueden consumir datos agregados previamente en un modelo analítico como informes o paneles

[Fundamentos de Datos Azure](https://github.com/CamarenaAI/Cloud-Fundamentals/tree/main/Azure/DP-900:%20Fundamentos%20de%20Datos%20Azure)