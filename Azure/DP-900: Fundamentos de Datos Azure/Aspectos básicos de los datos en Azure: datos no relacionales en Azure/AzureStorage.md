# Azure Storage

## Azure Blob Storage
Servicio que le permite almacenar grandes cantidades de datos no estructurados como objetos binarios grandes, o blobs, en la nube. Los BLOBs se almacenan en contenedores.
- Contenedor: Manera cómoda de agrupar blobs relacionados. Puede controlar quién puede leer y escribir blobs dentro de un contenedor en el nivel de contenedor

![Azure Blob Storage](https://learn.microsoft.com/es-mx/training/wwl-data-ai/explore-provision-deploy-non-relational-data-services-azure/media/azure-blob-storage.png)

### Tipos de BLOBs
- **Blobs en bloques** \
Conjunto de bloques. Almacena BLOBs discretos que cambian con poca frecuencia.
100 MB - 4.7TB, Un blob en bloques puede contener hasta 50 000 bloques

- **Blobs en páginas** \
Colección de páginas. Implementa el almacenamiento de discos virtuales de las máquinas virtuales.
512 bytes - 8TB, un blob en páginas está optimizado para admitir operaciones de lectura y escritura aleatorias; 

- **Blobs en anexos** \ 
Ooperaciones de anexión. Solo puede agregar bloques al final de un blob en anexos.
No se admite la actualización o eliminación de bloques existentes, 4 MB - 195 GB

### Niveles de acceso
- Frecuente: Acceso con frecuencia
- Esporadico: Acceso con poca frecuencia
- Archivo: Datos historicos

Puede crear directivas de administración que traslada automáticamente un blob de acceso frecuente a acceso esporádico y, a continuación, al nivel de acceso de archivo,
también puede organizarse para eliminar blobs obsoletos

### Azure Data Lake Storage Gen2
Servicio independiente para el almacenamiento jerárquico de los datos de lagos de datos analíticos que, 
con frecuencia, usan las denominadas soluciones de análisis de macrodatos que funcionan con datos estructurados, semiestructurados y no estructurados, almacenados en archivos
se integra en Azure Storage. \
Permite aprovechar la escalabilidad del almacenamiento en blobs y el control de costos de los niveles de almacenamiento, 
combinado con las capacidades del sistema de archivos jerárquico y la compatibilidad con los principales sistemas de análisis de Azure Data Lake Store

![ADLS](https://learn.microsoft.com/es-mx/training/wwl-data-ai/explore-provision-deploy-non-relational-data-services-azure/media/azure-data-lake.png)

Sistemas como Hadoop en Azure HDInsight, Azure Databricks y Azure Synapse Analytics pueden montar un sistema de archivos distribuido hospedado en Azure Data Lake Store Gen2 y usarlo para procesar grandes volúmenes de datos. \
Crear un sistema de archivos de Azure Data Lake Store Gen2:
- Habilitar la opción Espacio de nombres jerárquico de una cuenta de Azure Storage 

Puede hacerlo al crear inicialmente la cuenta de almacenamiento, o bien puede actualizar una cuenta de Azure Storage ya existente para que admita Data Lake Gen2. 
La actualización es un proceso unidireccional: después de actualizar una cuenta de almacenamiento para que admita un espacio de nombres jerárquico de almacenamiento de blobs, 
no se puede revertir a espacio de nombres plano

## Azure Files Storage
Manera de crear recursos compartidos de red basados en la nube, para que los documentos y otros archivos estén a disposición de varios usuarios.
Permite compartir hasta 100 TB de datos en una sola cuenta de almacenamiento. El tamaño máximo de un solo archivo es de 1 TB, 
se puede establecer cuotas para limitar el tamaño de cada recurso compartido por debajo de esta cifra

![Azure Files](https://learn.microsoft.com/es-mx/training/wwl-data-ai/explore-provision-deploy-non-relational-data-services-azure/media/azure-files.png)

### Niveles de Rendimiento
- Estándar: Usa hardware basado en disco duro en un centro de datos 
- Premium: Usa discos de estado sólido, mayor rendimiento, se cobra a una tarifa superior

### Protocolos Comunes de uso compartido
- Bloque de mensajes del servidor (SMB): Windows, Linux, MacOs
- Network File System (NFS): Linux y MacOS, cuenta premium. Crear y configurar una red virtual

## Azure Table Storage
Solución de almacenamiento NoSQL que usa tablas que contienen elementos de datos de clave-valor.
![Azure Table Storage](https://learn.microsoft.com/es-mx/training/wwl-data-ai/explore-provision-deploy-non-relational-data-services-azure/media/azure-tables.png)

Permite almacenar datos semiestructurados. Todas las filas de una tabla deben tener una clave única (compuesta de una clave de partición y una clave de fila)
- Clave de particion: Identifica la particion que contiene la fila
- Clave de fila: Unica para cada fila de la misma particion

Los datos en Azure Table Storage se desnormalizan y cada fila contiene los datos completos de una entidad lógica, 
Azure Table Storage divide una tabla en particiones, para agrupar filas relacionadas según una propiedad común o clave de partición
