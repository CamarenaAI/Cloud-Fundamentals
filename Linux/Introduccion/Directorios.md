# Directorios

## Lista de directorio completo

- **/**: Raíz de todos los archivos y directorios del sistema.
- **/bin**: Binarios esenciales para el funcionamiento básico del sistema.
- **/boot**: Archivos necesarios para el arranque del sistema operativo.
- **/cdrom**: Punto de montaje para discos ópticos (CD/DVD) cuando se insertan.
- **/cgroup**: Sistema de control de recursos utilizado para limitar el uso de CPU, memoria y otros recursos por parte de los procesos.
- **/dev**: Dispositivos de hardware representados como archivos especiales (discos, teclados, ratón, etc.).
- **/etc**: Archivos de configuración y scripts del inicio del sistema.
- **/export**: Directorio utilizado para compartir recursos a través de NFS (Network File System).
- **/home**: Directorios personales de cada usuario en el sistema.
- **/lib**: Bibliotecas compartidas para binarios en **/bin** y **/sbin**.
- **/lib64**: Bibliotecas de 64 bits compartidas para programas del sistema.
- **/lost+found**: Área de recuperación de archivos corruptos tras un fallo del sistema de archivos.
- **/media**: Puntos de montaje automáticos para dispositivos extraíbles (USB, CD/DVD, discos externos).
- **/mnt**: Punto de montaje temporal para sistemas de archivos montados manualmente.
- **/opt**: Software adicional y aplicaciones opcionales instaladas manualmente.
- **/proc**: Sistema de archivos virtual que contiene información sobre los procesos y el kernel.
- **/root**: Directorio personal del usuario **root** (administrador del sistema).
- **/run**: Archivos de datos de aplicaciones y procesos en ejecución desde el inicio del sistema.
- **/sbin**: Binarios del sistema utilizados para administración y mantenimiento.
- **/selinux**: Configuraciones y políticas del sistema de seguridad SELinux (si está habilitado).
- **/srv**: Datos de servicios ofrecidos por el sistema (servidores web, FTP, etc.).
    - **/srv/www**: Directorios para los archivos de los servidores web.
    - **/srv/ftp**: Directorio de almacenamiento para un servidor FTP.
- **/sys**: Información sobre el hardware y el kernel en tiempo real.
- **/tmp**: Archivos temporales eliminados automáticamente al reiniciar.
- **/usr**: Utilidades y aplicaciones para los usuarios del sistema.
    - **/usr/bin**: Programas y comandos ejecutables de uso general.
    - **/usr/lib**: Bibliotecas compartidas necesarias para programas en **/usr/bin**.
    - **/usr/local**: Aplicaciones y programas instalados manualmente por el usuario.
    - **/usr/sbin**: Herramientas administrativas del sistema que no son esenciales para el arranque.
- **/var**: Archivos variables como logs, colas de impresión y cachés.
    - **/var/log**: Archivos de registro del sistema y de aplicaciones.


## Estructuras de directorios de las aplicaciones

Las aplicaciones que no son parte del sistema operativo pueden instalarse en:

- **usr/local**:
    ```powershell
    /usr/local/apache/bin
    /usr/local/apache/etc
    /usr/local/apache/lib
    /usr/local/apache/logs

- **opt**:
    ```powershell
    /opt/apache/bin
    /opt/apache/etc
    /opt/apache/lib
    /opt/apache/logs

A partir de ahí tendrá su propia estructura de subdirectorios.