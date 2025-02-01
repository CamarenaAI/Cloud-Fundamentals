# Identificar las consideraciones para los datos relacionales en Azure

## Caracteristicas de datos relacionales
En una base de datos relacional, las colecciones de entidades del mundo real se modelan en forma de tablas. \
Una _**entidad**_ puede ser cualquier elemento para el que quiere registrar informacion; por lo general, se trata de onjetos y eventos importantes

- Tablas: Formato para datos estructurados, cada fila de una tabla tiene las mismas columnas, en algunos casos no todas las tablas necesitan un valor
- Columnas: Almacena los datos en un tipo de datos especifico

## Normalizacion
Proceso de diseño de esquemas que reduce al minimo la duplicacion de los datos e impone la integridad de los datos
- Separar cada entidad en su propia tabla
- Separar cada atributo discreto en su propia columna
- Identificar de forma única cada instancia de entidad (fila) mediante una clave principal
- Usar columnas de clave externa para vincular entidades relacionadas

## Sentencias comunes de lenguaje de consulta estructurado (SQL)
**SQL**: Se usa para comunicarse con una base de datos relacional. Lenguage estandar para los sistemas de bases de datos relacionales

### Tipos de instrucciones SQL
- **Data Definition Language (DDL)** \
Se usa para crear, modificar y quitar tablas y otros objetos de una base de datos(tabla, procedimientos almacenados, vistas, etc.)
    - **CREATE**: Permite crear un nuevo objeto en la Base de Datos
    - **RENAME**: Permite cambiar el nombre de un objeto existente
    - **ALTER**: Permite modificar la estructura de un objeto
    - **DROP**: Permite quitar un objeto en la Base de Datos

- **Data Control Language (DCL)** \
Se usa para administrar el acceso a objetos de una base de datos mediante la consecion, denegacion o revocacion de permisos a usuarios o grupos especificos
    - **DENY**: Denegacion de permiso para llevar a cabo acciones especificas
    - **GRANT**: Consecion de permiso para llevar a cabo acciones especificas
    - **REVOKE**: Retirada de un permiso concedido

- **Data Manipulation Language (DML)** \
Se usa para manipular las filas en las tablas
    - **SELECT**: Lectura de filas de las tablas
    - **INSERT**: Permite insertar nuevas filas en una tabla
    - **UPDATE**: Modificacion de datos en filas existentes
    - **DELETE**: Eliminacion de filas existentes
    
## Objetos de base de datos
- **Vista**: Tabla virtual basada en los resultados de una consulta **SELECT**. Es como una ventana que muestra filas concretas en una o varias filas sunyacentes
- **Procedimiento Almacenado**: Define instrucciones SQL que se pueden ejecutar a peticion. Se usan para encapsular la logica de programacion de una base de datos para las acciones que las aplicaciones deben realizarse al trabajar con datos. Puede definir un procedimiento almacenado con parámetros a fin de crear una solución flexible para las acciones comunes que podrían tener que aplicarse a los datos en función de una clave o criterios específicos
- **Indice**: Ayuda a buscar datos en una tabla. Contiene un conjunto ordenado de contenido junto a las paginas en las que aparece

[Fundamentos de Datos Azure](https://github.com/CamarenaAI/Cloud-Fundamentals/tree/main/Azure/DP-900:%20Fundamentos%20de%20Datos%20Azure)
