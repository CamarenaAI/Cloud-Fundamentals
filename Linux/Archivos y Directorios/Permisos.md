# Permisos

    -rw-r--r-- 1 admin users 35 Nov 14 20:26 hello_world.py
    drwxr-xr-x 2 admin users 4096 Jan 28 13:54 Azure
    lrwxrwxrwx 1 admin users 20 oct 15 12:00 enlace_documento.txt

| Simbolo    | Tipo                |
| :--------- | :------------------ |
| `-`        | Archivo regular     |
| `d`        | Directorio          |
| `l`        | Enlace simbolico    |

| Simbolo    | Permisos    |
| :--------- | :---------- |
| `r`        | Leer        |
| `w`        | Escribir    |
| `x`        | Ejecutar    |

## Permisos en archivos y directorios

| Permiso               | Archivo                                 | Directorio                                                     |
| :-------------------- | :-------------------------------------- | :------------------------------------------------------------- |
| `Leer (r)`            | Permite leer un archivo                 | Permite leer los nombres de los archivos en el directorio      |
| `Escribir (w)`        | Permite modificar un archivo            | Permite modificar entradas dentro del directorio               |
| `Ejecutar (x)`        | Permite la ejecución de un archivo      | Permite el acceso a los contenidos y metadatos de las entradas |

## Categorias de permisos

| Simbolo    | Categoria    |
| :--------- | :----------- |
| `u`        | Usuario      |
| `g`        | Grupo        |
| `o`        | Otro         |
| `a`        | Todos        |

## Grupos

Son usados para organizar a los usuarios. Los usuarios pertenecen al menos a un grupo pero pueden pertenecer a otros grupos

Los siguientes comandos muestran los grupos del usuario
- **groups**
- **id -Gn**

##  

| Tipo                  | Usuario  | Grupo    | Otro     |
| :-------------------- | :----    | :------- | :------- |
| `-` `,` `d` `,` `l`   | **rw-**  | **r--**  | **r--**  |

## Cambiar permisos
- **chmod**: Permite cambiar los permisos en archivos y directorios.
- **+**: Agregar permiso.
- **-**: Quitar permiso.
- **=**: Establecer permiso.

| Octal   | Binario  | Caracter   | Descripcion                    |
| :------ | :------- | :--------- | :----------------------------- |
| `0`     | `0`      | `---`      | Sin permisos                   |
| `1`     | `1`      | `--x`      | Solo ejecutar                  |
| `2`     | `10`     | `-w-`      | Solo escritura                 |
| `3`     | `11`     | `-wx`      | Escritura y Ejecutar           |
| `4`     | `100`    | `r--`      | Solo lectura                   |
| `5`     | `101`    | `r-x`      | Lectura y Ejecutar             |
| `6`     | `110`    | `rw-`      | Lectura y Escritura            |
| `7`     | `111`    | `rwx`      | Lectura, Escritura y Ejecutar  |

Ejemplo de como cambiar los permisos usando **chmod** con **caracteres** y en **octal**

    chmod u=rwx,g=rx,o=rx Documents

    chmod 755 Documents

