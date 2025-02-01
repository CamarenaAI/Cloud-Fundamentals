# Servicios de datos relacionales de Azure

## Azure SQL
Es un término colectivo para referirse a una familia de servicios de base de datos basados en Microsoft SQL Server en Azure. \
Los servicios específicos de Azure SQL incluyen los siguientes:

- **Azure SQL Database** \
Servicio de Base de datos PaaS (Platform as a Service) totalmente administrado y altamente escalable que se ha diseñado para la nube. \
Incluye capacidades de bases de datos SQL Server Local, buena opcion cuando hay que crear una aplicacion en la nube
    - Base de datos única
        - Configurar y ejecutar rápidamente una sola base de datos de SQL Server
        - Puede crear y ejecutar un servidor de bases de datos en la nube y acceder a la base de datos a través de este servidor
        - Puede escalar la base de datos (si necesita más espacio de almacenamiento, memoria o potencia de procesamiento)
        - Los recursos están preasignados y se le cobra por hora por los recursos solicitados
        - Puede especificar una configuración sin servidor.
        En esta configuración, Microsoft crea su propio servidor, que se puede compartir entre las bases de datos que pertenecen a otros suscriptores de Azure.
        Microsoft garantiza la privacidad de su base de datos
        - Su base de datos se escala automáticamente y los recursos se asignan o desasignan según sea necesario 
        
    - Grupo elástico
        - Varias bases de datos pueden compartir los mismos recursos (como la memoria, el espacio de almacenamiento de datos y la capacidad de procesamiento mediante la arquitectura multiinquilino)
        - Hace referencia a los recursos como un grupo. Al crear un grupo, solo sus bases de datos pueden usarlo
        - Permite usar los recursos disponibles en el grupo y liberarlos una vez que se haya completado el procesamiento
    
- **Azure SQL Managed Instance** \
Opción PaaS (Platform as a Service) que proporciona una compatibilidad casi completa con instancias de SQL Server locales 
y permite abstraer el hardware y el sistema operativo subyacentes. 
Este servicio incluye administración automatizada de actualizaciones de software, copias de seguridad y otras tareas de mantenimiento, 
lo que reduce la carga administrativa que supone admitir una instancia de servidor de bases de datos \
Las instancias administradas dependen de otros servicios de Azure, como:
    - Azure Storage para las copias de seguridad 
    - Azure Event Hubs para la telemetría
    - Azure Active Directory para la autenticación
    - Azure Key Vault para el cifrado de datos transparente (TDE) \
    
    y un par de servicios de la plataforma de Azure que proporcionan características de seguridad y compatibilidad. 
    Las instancias administradas realizan conexiones con estos servicios.
    
- **SQL Server en Azure Virtual Machines** \
Solucion IaaS (Infrastructure as a Service) permite virtualizar la infraestructura de hardware para proceso, almacenamiento y redes en Azure,
se ejecuta en Azure con una instalacion de SQL Server. permite usar versiones completas de SQL Server en la nube sin tener que administrar ningún hardware local


|                             | Azure Virtual Machines | Azure SQL Managed Instance | Azure SQL Database |
| --------------------------- | ---------------------- | -------------------------- | ------------------ |
| Tipo de servicio en la nube | IaaS | PaaS | PaaS |
| Compatibilidad con SQL Server | Es totalmente compatible con instalaciones físicas y virtualizadas locales. Las aplicaciones y bases de datos se pueden migrar fácilmente usando el método lift-and-shift y sin cambios | Es casi completamente compatible con SQL Server. La mayoría de las bases de datos locales se pueden migrar con cambios mínimos en el código mediante el servicio Azure Database Migration | Admite la mayoría de las funcionalidades básicas de base de datos de SQL Server. Es posible que algunas características de las que dependa una aplicación local no estén disponibles |
| Arquitectura | Las instancias de SQL Server se instalan en una máquina virtual. Cada instancia puede admitir varias bases de datos | Cada instancia administrada puede admitir varias bases de datos. Además, los grupos de instancias se pueden usar para compartir recursos de forma eficaz entre instancias más pequeñas | Puede aprovisionar una base de datos única en un servidor dedicado y administrado (lógico); también puede usar un grupo elástico para compartir recursos entre varias bases de datos y aprovechar la escalabilidad a petición |
| Disponibilidad | 99.99%	| 99.99% | 99.995 % |
| Administración | Debe administrar todos los aspectos del servidor, incluidos el sistema operativo y SQL Server, la configuración, las copias de seguridad y otras tareas de mantenimiento | Actualizaciones, copias de seguridad y recuperación totalmente automatizados | Actualizaciones, copias de seguridad y recuperación totalmente automatizados |
| Casos de uso | Use esta opción cuando necesite migrar o ampliar una solución de SQL Server local y conservar el control total sobre todos los aspectos de la configuración del servidor y la base de datos | Use esta opción para la mayoría de los escenarios de migración a la nube, especialmente cuando necesite cambios mínimos en las aplicaciones existentes | Use esta opción para nuevas soluciones en la nube o para migrar aplicaciones que tengan dependencias mínimas de instancia |

## Servicios de base de datos de Azure para sistemas de base de datos de código abierto
- **Azure Database for MySQL** (LAMP) \
Implementación PaaS de MySQL en la nube de Azure \
Proporciona un sistema de base de datos global que se puede escalar verticalmente a bases de datos grandes sin necesidad de administrar el hardware, 
los componentes de red, los servidores virtuales, las revisiones de software y otros componentes subyacentes \
Los servidores de Azure Database for MySQL proporcionan funcionalidades de supervisión para agregar alertas y para ver las métricas y los registros.

- **Azure Database for PostgreSQL** (Hibrido) \
Implementación PaaS de PostgreSQL en la nube de Azure \
Base de datos híbrida de objetos relacionales. 
Una base de datos de PostgreSQL permite almacenar datos en tablas relacionales, pero también tipos de datos personalizados con sus propias propiedades no relacionales. 
El sistema de administración de bases de datos es extensible, se pueden agregar módulos de código a la base de datos, 
los cuales pueden ejecutarse mediante consultas

- **Azure Database for MariaDB** (Oracle) \
Implementación del sistema de administración de bases de datos MariaDB adaptada para ejecutarse en Azure \
Compatibilidad integrada con los datos temporales. 
Una tabla puede contener varias versiones de datos, lo que permite que una aplicación consulte los datos tal y como aparecían en algún momento del pasado

[Fundamentos de Datos Azure](https://github.com/CamarenaAI/Cloud-Fundamentals/tree/main/Azure/DP-900:%20Fundamentos%20de%20Datos%20Azure)
