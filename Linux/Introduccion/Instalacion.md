# Instalación

## 🚀 1. Instalación nativa (Dual Boot o única instalación)
### Requisitos:
- USB booteable (Usar **Rufus** o **Balena Etcher**)
- Descarga una distribución de Linux:
  - [Ubuntu](https://ubuntu.com/download)
  - [Debian](https://www.debian.org/download)
  - [Fedora](https://fedoraproject.org//#editions)

### Pasos:
1. Crear el USB booteable con Rufus o Balena Etcher.
2. Reiniciar la PC y entrar a la BIOS/UEFI (F2, F12, Del o Esc).
3. Configurar el arranque desde USB y guardar cambios.
4. Iniciar desde el USB y seleccionar "Instalar Linux".
5. Elegir tipo de instalación:
    - Dual Boot: Instalar junto con Windows/macOS.
    - Borrar todo el disco (CUIDADO, borra todo).
6. Configurar particiones (Opcional).
7. Elegir zona horaria y usuario.
8. Esperar la instalación y reiniciar.

## 🖥 2. Instalación en Máquina Virtual (VM)
### Requisitos:
- [VirtualBox](https://www.virtualbox.org/) o [VMware](https://www.vmware.com/products/workstation-player.html)

### Pasos:
1. Descargar e instalar VirtualBox o VMware.
2. Descargar la ISO de Linux (Ver enlaces anteriores).
3. Crear una nueva máquina virtual y asignar:
    - RAM: Al menos 2GB (recomendado 4GB o más).
    - Disco virtual: 20GB o más.
4. Montar la ISO como unidad de arranque.
5. Iniciar la máquina virtual e instalar Linux normalmente.
6. Configurar usuario y contraseña.
7. Finalizar la instalación y reiniciar.

## 🏆 3. Windows Subsystem for Linux (WSL)
### Requisitos:
- Windows 10/11 actualizado.
- WSL habilitado.

### Pasos:
1. Abrir PowerShell como administrador.
2. Ejecutar:
   ```powershell
   wsl --install -d Ubuntu
3. Esperar la instalación y reiniciar.
4. Abrir "Ubuntu" desde el menú de inicio.
5. Configurar nombre de usuario y contraseña.
6. ¡Listo! Puedes usar Linux desde la terminal de Windows.

## 🔥 4. Live USB (Modo en vivo)
### Requisitos previos:
- USB de 8GB o más.
- Herramienta para crear USB booteable.

### Pasos:
1. Descargar la ISO de Linux (Ver enlaces anteriores).
2. Usar Balena Etcher o Rufus para crear el USB booteable.
3. Reiniciar la PC y arrancar desde el USB.
4. Seleccionar "Probar Linux sin instalar".
5. Explorar Linux y, si lo deseas, instalarlo desde ahí.

## 🐳 5. Instalación en Docker
### Requisitos previos:
- Docker Desktop instalado:
    - Descargar Docker

### Pasos:
1. Instalar Docker en Windows/macOS/Linux.
2. Abrir una terminal y ejecutar:
    - docker run -it ubuntu bash
3. Se abrirá un contenedor con Ubuntu listo para usar.
4. Para salir, escribe exit.