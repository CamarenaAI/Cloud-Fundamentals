# Obtener datos desde orígenes de datos

## Identificar un origen de datos y conectarse a él

[Orígenes de datos en Power BI Desktop](https://learn.microsoft.com/es-es/power-bi/connect-data/desktop-data-sources)
[Conectores en Power Query](https://learn.microsoft.com/es-es/power-query/connectors/)

### Obtención de datos de archivos
Un archivo plano (flat file) es aquel que solo tiene una tabla de datos y en el que cada fila de datos está en la misma estructura. (El archivo no contiene jerarquías)
- Tipos más comunes de archivos planos:
    - **Comma-Separated Values (.csv)**
    - **Delimited Text (.txt)**
    - **Libros de microsoft Excel (.xlsx)**
    - **Archivos de ancho de fijo**

#### Ubicación del archivo plano
- **Local**
- **OneDrive para la empresa**
- **OneDrive - Personal**
- **SharePoint**

#### Conexión a los datos de un archivo
- En Power BI, en la pestaña Inicio, seleccione **Obtener datos (Get Data)**.
- En la lista que se muestra, seleccionar la opción que necesite, como Texto o CSV o XML. (_**_Se abrira la ventana Navegador_**_)
- Activar las casillas de las tablas que se quieran incluir en Power BI.
- Puedes seleccionar el boton **Cargar (Load)** para cargar los datos automáticamente en el modelo de Power BI o seleccionar el boton **Transformar datos (Transform Data)** para iniciar el Editor de Power Query en el que puede revisar y limpiar los datos antes de cargarlos en el modelo de Power BI.

_**_En función de la selección, deberá buscar y abrir el origen de datos. Es posible que se le pida que inicie sesión en un servicio, como OneDrive, para autenticar su solicitud._**_

### Obtención de datos de orígenes de datos relacionales
#### Conexión a los datos de una base de datos relacional
- En Power BI, en la pestaña Inicio, seleccione **Obtener datos (Get Data)**.
- Seleccionar la opción aplicable para la base de datos relacional.
- Escribir el nombre del **servidor (server)** de base de datos y un nombre de **base de datos (database)**.
    - Las opciones del modo de conectividad de datos son:
        - Importar (Import) opción recomendada y seleccionada de forma predeterminada.
        - DirectQuery.
- Iniciar sesión con un nombre de usuario y una contraseña y seleccione **Conectar (Connect)**.
    - Opciones de inicio de sesión:
        - **Windows**
        - **Bases de datos**
        - **Cuenta de Microsoft**
- En la ventana Navegador se muestran los datos que están disponibles en el origen de datos.
- Seleccionar una tabla o entidad para obtener una vista previa de su contenido y asegurarse de que se cargan los datos correctos en el modelo de Power BI.
- Activar las casillas de las tablas que quiere incluir en Power BI Desktop y seleccione la opción **Cargar (Load)** o **Transformar datos (Transform Data)**.

### Obtención de datos de una base de datos NoSQL
#### Conexión con una base de datos NoSQL
- En Power BI, en la pestaña Inicio, seleccione **Obtener datos (Get Data)**.
- Seleccionar la opcion **Más... (More...)** para buscar el tipo de base de datos que usa y conectarse a ella.
- En la ventana **Conector de vista previa (Preview Connector window)**, seleccione Continuar y, luego, escriba las credenciales de la base de datos.
- En la ventana Navegador se mostrara una lista de las bases de datos de esa cuenta.
- Seleccionar la tabla que se quiere importar.
- Seleccionar el botón **Editar (Edit)** para abrir los registros en Power Query.
- En Power Query, seleccione el botón expansor situado a la derecha del encabezado Column1 para mostrar el menú contextual con una lista de campos. 
- Seleccionar los campos que quiere cargar en Power BI Desktop, desactive la casilla Usar el nombre de columna original como prefijo y seleccione Aceptar.
- Revisar los datos seleccionados para asegurarse de estár satisfecho con ellos y seleccione Cerrar y aplicar para cargar los datos en Power BI Desktop.

_**_Si se va a conectar a un punto de conexión por primera vez, asegúrese de especificar la clave de la cuenta. Si trabaja con datos almacenados en formato JSON, a menudo es necesario extraer y normalizar primero los datos, los datos JSON se suelen almacenar con un formato anidado o no estructurado, lo que dificulta el análisis o la elaboración de informes directamente por lo que debe transformar esos datos antes de cargarlos en Power BI Desktop._**_

### Obtención de datos de servicios en línea
#### Conexión con los datos de una aplicación
- Seleccionar la característica Obtener datos en Power BI Desktop. 
- Seleccionar la opcion **Más... (More...)** elijir la opción que se necesite en la categoría Servicios en línea y conectarse al servicio. 
- Una vez que haya seleccionado Conectar, se le pedirá la dirección URL.
- Después de especificar la dirección URL, seleccione Aceptar. Power BI debe autorizar la conexión. 
- Por lo tanto, inicie sesión y seleccione Conectar.
- Aparecerá la ventana Navegador, en la ventana se muestran las tablas y entidades del servicio en linea. 
- Seleccionar la lista que se quiere cargar en Power BI Desktop.
- Puede seleccionar la opción de cargar los datos automáticamente en un modelo de Power BI o iniciar el Editor de Power Query para transformar los datos antes de cargarlos.

### Obtener datos de Azure Analysis Services
#### Conexión con los datos de Azure Analysis Services
- En Power BI, en la pestaña Inicio, seleccione **Obtener datos (Get Data)**.
- Seleccionar la opcion **Más... (More...)**, seleccionar Azure y Azure Analysis Services.
- Al seleccionar Analysis Services, se le solicitará la dirección del servidor y el nombre de la base de datos con dos opciones: 
    - **Importar (Import)** 
    - **Conectar en directo (Conect Live)**

## Cambiar la configuración del origen de datos, incluidas las credenciales, los niveles de privacidad y las ubicaciones del origen de datos


## Selección de un modelo semántico compartido o creación de un modelo de datos local
El modelo semántico proporciona a los usuarios una forma más fácil y rápida de analizar datos ad hoc mediante herramientas como Power BI.

## Elegir entre DirectQuery, Importar y modo dual


## Cambiar el valor en un parámetro

