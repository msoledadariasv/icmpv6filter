# Laboratorio ICMPv6 Security con Containerlab
---
La topología creada tiene por objetivo poveer un entorno controlado para el analisis de seguridad del protocolo IPv6.

# Requisitos previos
La imagen utilizada del switch ArubaOS-CX se provee como una VM basada en QEMU y requiere del proyecto vrnetlab para ejecutar la VM dentro de un contenedor docker, en pocas palabras se trata de
"una VM disfrazada de contenedor"
Siga los siguientes pasos:

* Crear una cuenta en Github e importar el repositorio https://github.com/ernestosv73/icmpv6filter.git
* Crear una cuenta en https://networkingsupport.hpe.com/
* Descargar la imagen Aruba_AOS-CX_Switch_Simulator_10.14.1000.ova desde https://networkingsupport.hpe.com/downloads/software/RmlsZTo3YmRlNGViZS01ZTY3LTExZWYtYTQzYy0wZjBjOGRmMzJkZmU%3D.
* Instalar VSCode e instalar las extensiones GitHub Codespaces y Dev Containers.
* Ejecutar la topología haciendo clic en "Run in codespace", lo que creará un nuevo espacio.
* Desde el directorio /workspaces ejecutar git clone https://github.com/hellt/vrnetlab.git para descargar los archivos requeridos para crear la imagen docker de ArubaOS-CX
* Para copiar la imagen .ova al repositorio remoto debemos iniciar sesión desde VSCode ejecutando Ctrl+Shift+P y escribir GitHub: Sign in  
