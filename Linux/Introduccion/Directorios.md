# Directorios comunes en Linux

- **/**: Raiz de todos los archivos y directorios del sistema.
- **/bin**: Binarios escenciales para el funcionamiento basico del sistema.
- **/boot**: Archivos necesarios para el arranque del sistema operativo.
- **/dev**: Dispositivos de hardware representados como archivos especiales.
- **/etc**: Archivos de configuracion y scripts del inicio del sistema.
- **/home**: Directorios personales de cada usuario en el sistema.
- **/lib**: Bibliotecas compartidas para binarios en **/bin** y **/sbin**.
- **/media**: Puntos de montaje para dispositivos externos (usb, cd-room).
- **/mnt**: Montaje temporal de sistemas de archivos manualmente.
- **/opt**: Software adicional y aplicaciones opcionales instaladas manualmente.
- **/proc**: Informacion del kernel y procesos en forma de archivos.
- **/root**: Directorio personal del usuario **root** (administrador del sistema).
- **/run**: Archivos de datos de aplicaciones desde el inicio del sistema.
- **/sbin**: Binarios del sistema para administracion y mantenimiento.
- **/srv**: Datos de servicios ofrecidos por el sistema (Web, File Transfer Protocol).
- **/sys**: Informacion del kernel y dispositivos conectados al sistema.
- **/tmp**: Archivos temporales eliminados automaticamente al reiniciar.
- **/usr**: Utilidades y aplicaciones para usuarios del sistema.
- **/var**: Archivos variables como logs, colas de impresion y caches.

# Estructuras de directorios de las aplicaciones

La aplicaciones que no son parte del sistema operativo pueden instalarse en:

- **usr/local**:
    - usr/local/doc/bin
    - usr/local/doc/etc
    - usr/local/doc/lib
    - usr/local/doc/logs

- **opt**:
    - opt/doc/bin
    - opt/doc/etc
    - opt/doc/lib
    - opt/doc/logs

A partir de ahi tendran su propia estructura de subdirectorios.