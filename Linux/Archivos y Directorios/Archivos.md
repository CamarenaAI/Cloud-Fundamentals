# Visualizar archivos usando el comando **ls**

## Opciones con el comando **ls**
- **ls -a**: Ver información detallada, incluida información oculta.
- **ls --color**: Ver información con color.
- **ls -d**: Ver nombre del directorio, no el contenido.
- **ls -F**: Ver información del tipo de archivos.
- **ls -l**: Ver información detallada.
- **ls -r**: Ver información invirtiendo el orden.
- **ls -R**: Ver contenido del directorio actual y subdirectorios.
- **ls -t**: Ver información por tiempo.

## Salida del comando **ls -l**

    drwxr-xr-x 1 admin users 4096 Jan 6 15:05 Python

| Elemento                        | Valor          |
| :------------------------------ | :------------- |
| `Permisos`                      | drwxr-xr-x     |
| `Numero en enlaces`             | 1              |
| `Nombre del propietario`        | admin          |
| `Nombre del grupo`              | users          |
| `Numero de bytes en el archivo` | 4096           |
| `Ultima modificación`           | Jan  6 15:05   |
| `Nombre del archivo`            | Python         |

## Archivos por tipo usando el comando **ls -F**
- **/**: Directorio.
- **@**: Link.
- _*_: Archivo ejecutable.

## Comando **tree**
Similar al comando **ls -R**, pero crea salidas visuales.
- **tree -d**: Lista los directorios.
- **tree -C**: Colorea la salida.

## Espacios en archivos o directorios
No utilizar espacios en los nombres de archivos y directorios, mejor utilizar **-**, **_**, **CamelCase (Escribir en mayúscula la primera letra de cada palabra)**.

Para leer/abrir un archivo o directorio que contiene un espacio podemos usar **''** o **""**.