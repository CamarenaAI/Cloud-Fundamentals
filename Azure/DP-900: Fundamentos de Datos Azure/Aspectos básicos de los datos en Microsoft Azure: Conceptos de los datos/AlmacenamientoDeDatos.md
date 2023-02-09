# Almacenamiento de archivos

## Formatos de archivo comunes

- **Archivos de texto delimitado** \
Se almacenan como texto sin formato con delimitadores de campo y terminadores de fila específicos
    - **Comma-Separated Values (CSV)**: Los campos están separados por comas y las filas finalizan con un retorno de carro o una nueva línea
                                  Opcionalmente, la primera línea puede incluir los nombres de campo
    - **Tab-Separated Values (TSV)**: Se usan tabulaciones o espacios para separar los campos
                                Datos de ancho fijo en los que a cada campo se le asigna un número fijo de caracteres 
                                
    El texto delimitado es una buena opcion para los datos estructurados

- **JavaScript Object Notation (JSON)** \
Formato omnipresente en el que se usa un esquema de documento jerárquico para definir entidades de datos (objetos) que tienen varios atributos. 
Cada atributo puede ser un objeto (o una coleccion de objetos) \
El formato JSON es un formato flexible adecuado tanto a datos estructurados como semiestructurados \
Los objetos se incluyen entre llaves ({..}) \
Las colecciones se incluyen entre corchetes ([..]) \
Los atributos se representan mediante pares nombre:valor y se separan por comas (,)

- **Extensible Markup Language (XML)** \
Formato de datos legible entre 1990 y 2000\
El formato XML es una opcion para los datos semiestructurados \
Usa etiquetas entre corchetes angulares (../) para definir elementos y atributos

- **Binary Large Object (BLOB)** \
Almacenan los datos como datos binarios sin formato que las aplicaciones deben interpretar y representar \
Los tipos comunes de datos almacenados como datos binarios incluyen imágenes, vídeo, audio y documentos específicos de aplicaciones \
Cuando trabajan con datos de este tipo, los profesionales de datos suelen hacer referencia a estos archivos de datos como BLOB (Binary Large Objects)

## Tipos de Bases de Datos

- **Bases de datos relacionales** \
Suelen usarse para almacenar y consultar datos estructurados \
Los datos se almacenan en tablas que representan entidades \
A cada instancia de una entidad se le asigna una clave principal que la identifica de forma única; estas claves se usan para hacer referencia a la instancia de entidad en otras tablas \
El uso de claves para hacer referencia a entidades de datos permite normalizar(eliminacion de valores de datos duplicados) una base de datos relacional \
Las tablas se administran y consultan mediante SQL(Structured Query Language)

- **Bases de datos no relacionales** \
Sistema de administración de datos que no aplican un esquema relacional a los datos \
Suelen conocerse como Bases de datos NoSQL (No Structured Query Language) \
Hay cuatro tipo de bases de datos no relacionales que se usan habitualmente:
    - **Bases de datos de clave-valor**: Cada registro consta de una clave única y un valor asociado, que puede estar en cualquier formato
    - **Bases de datos de documentos**: Forma específica de base de datos de clave-valor
                                        El valor es un documento JSON (que el sistema está optimizado para analizar y consultar)
    - **Bases de datos de familia de columnas**: Almacenan datos tabulares con filas y columnas, pero con la posibilidad de dividir esas columnas en grupos
                                                 Cada familia de columnas contiene un conjunto de columnas que tienen una relación lógica entre sí
    - **Bases de datos de grafos**: Almacenan entidades como nodos con vínculos para definir relaciones entre ellas