# Buscar archivos y directorios

- **find**: Permite encontrar archivos usando: **find** + **ruta** + **expresión** los resultados son en tiempo real.
- **locate**: Permite encontrar archivos y directorios más rápido que el comando **find** solo que los resultados no son en tiempo real.

## Opciones de búsqueda con el comando **find**

- **-name**: Buscar archivos y directorios que coincidan con el patrón. 
- **-iname**: Se utiliza al igual que **-name** solo que ignora letras mayúsculas. 
- **-ls**: Realiza una operación **ls** en cada elemento encontrado. 
- **-mtime**: Buscar archivos por hora de modificación. 
- **-size**:  Buscar archivos en función de tamaño.
- **-newer**: Buscar archivos/directorios que se crean después.
- **-exec {} \;**: Ejecuta el comando contra todos los archivos que hay.