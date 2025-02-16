# Visualización y edición de archivos

- **cat**: Muestra el contenido del archivo.
- **more**: Permite desplazarte por el contenido de un archivo sin necesidad de retroceder.
- **less**: Permite desplazarte en ambas direcciones, hacer búsquedas avanzadas o ver archivos en tiempo real.
- **head**: Muestra la parte inicial o superior de un archivo.
- **tail**: Muestra la parte final o inferior de un archivo.
    - **tail -f**: Muestra los datos a medida que se escriben en el archivo. 

_**Nota**_: Por defecto el comando **head** y **tail** muestran solo muestran 10 líneas.
Puede cambiar este comportamiento con **-n**  siendo **n** igual al número de líneas.

    head -10 file.txt
    tail -10 file.txt

## Editor Nano

Editor de texto simple e intuitivo que se ejecuta en la terminal. Ideal para quienes no tienen experiencia con editores en línea de comandos.

Abrir un archivo:

    nano file.txt

### Comandos esenciales

- **Ctrl + O**: Guardar cambios. 
- **Ctrl + X**: Salir. 
- **Ctrl + K**: Cortar una línea. 
- **Ctrl + U**: Pegar.
- **Ctrl + W**: Buscar 

## Editor Vi/Vim

Editores avanzados y eficientes, requieren aprender algunos comandos para usarlos de manera eficiente.

### Modos en Vim
- Modo normal (para navegar y ejecutar comandos).
- Modo de inserción (para escribir texto).
- Modo de comando (para operaciones avanzadas).

Abrir un archivo

    vi file.txt
    vim file.txt

### Comandos esenciales

- **i**: Entrar en el modo de inserción.
- **Esc**: Salir del modo de inserción.
- **:wq**: Guardar cambios y salir.
- **:q!**: Salir sin guardar.
- **:w**: Guardar sin salir.
- **/"insertar búsqueda"**: Buscar texto.
- **:%s/viejo/nuevo/g**: Sustituir texto.  

## Editor Emacs

Editor poderoso y personalizable. Mas complejo que el editor **nano**. Emacs puede usarse como entorno de desarrollo, ya que permite instalar plugins y configurar su comportamiento con Lisp.

Abrir un archivo

    emacs file.txt

### Comandos esenciales

- **Ctrl + X, Ctrl + F**: Abrir archivo.
- **Ctrl + X, Ctrl + S**: Guardar archivo.
- **Ctrl + X, Ctrl + C**: Salir.
- **Ctrl + K**: Cortar (kill).
- **Ctrl + Y**: Pegar (yank). 
- **Ctrl + X, u**: Deshacer.
- **Ctrl + S**: Buscar.

## Editores Gráficos

Si prefieres una interfaz más amigable, hay varios editores gráficos disponibles en Linux:

### Gedit (Sencillo y eficiente)
Editor por defecto en GNOME.

    gedit archivo.txt

- Soporta resaltado de sintaxis.
- Ideal para edición básica de texto.

### Kate (Poderoso y liviano)

Editor avanzado de KDE.

    kate archivo.txt

- Soporta pestañas y sesiones de trabajo.
- Resaltado de sintaxis.

### VS Code (Moderno y con muchas extensiones)

Editor popular para programación con soporte para múltiples lenguajes.

    code archivo.txt

- Extensible con plugins.
- Soporte para Git, depuración y más.

### Sublime Text (Ligero y rápido)

Editor con interfaz minimalista y muchas funciones avanzadas.

    subl archivo.txt

- Rápido y con autocompletado inteligente.