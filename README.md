# Proyecto 0 Gestion de tareas y categorias

El objetivo de este proyecto es desarrollar una aplicación web de listas y gestión de tareas que
permita a los usuarios crear, organizar y seguir el progreso de sus tareas diarias. La aplicación
constará de tres componentes principales: una API REST para la lógica del negocio, una base de
datos para almacenar la información de los usuarios y sus tareas, y una interfaz web para que los
usuarios interactúen con la aplicación.

## Tabla de Contenidos


1. Instalación
2. AWS
3. Endpoints

## Instalación
Este paso a  paso va enfocado al despliegue de la aplicación en una máquina ya sea física o virtual

1. Clonar el repositorio
   ```bash
   git clone https://github.com/DiegoGonzalez2807/Proyecto0-Uniandes-CLOUD.git
2. Entrar a la carpeta del repositorio clonado y ejecutar el siguiente comando:
   ```bash
   pip install -r requirements.txt
   ```
   ##### Lo que se hace con este comando es instalar las librerias necesarias para que el Frontend y el Backend se ejecuten de manera correcta.
   ##### Tener en cuenta que en caso de estar haciendo la instalación de los requerimientos de estos servicios en una instancia virtual EC2 primero se tiene que ejecutar el siguiente código ya que una EC2 no tiene por defecto pip. Después de esto devolverse a ejecutar el comando pip y seguir con los siguientes pasos
   ```bash
   sudo apt-get update
   sudo apt install python3-pip
   ```
4. Mediante consola dirigirse a la carpeta flaskr y ejecutar el servicio
   ```bash
   cd Proyecto0-Uniandes-CLOUD
   cd flaskr
   ```
   ##### Subir el servicio. Se pone los parámetros de puerto y host para definir por donde va a escuchar el servicio Backend
   ```bash
   flask run --port=5000 --host=0.0.0.0
   ```
5. devolverse a la carpeta Proyecto0-Uniandes-CLOUD
6. Mediante consola dirigirse a la carpeta frontend y ejecutar el servicio
   ```bash
   cd Proyecto0-Uniandes-CLOUD
   cd frontend
   ```
   ##### Subir el servicio frontend. En el momento de subir este servicio puede ser tanto python3 como python, asi revisar que caso es el que corresponde de acuerdo a la máquina
   ```bash
   python3 ./main.py
   ```
## AWS
#### Debido a que se están levantando las instancias virtuales en una cuenta educativa, estas al pasar las 4 horas del laboratorio detienen la instancia, bajando ambos servicios. Es por este motivo que se explicará como subir los servicios a una nueva instancia:
1. Levantar la instancia EC2 de su preferencia. Debe ser Ubuntu 22.04 la imagen de la instancia
2. agregar reglas de seguridad: Se debe habilitar los puertos 8080 y 5000 en las reglas de seguridad de entrada de tráfico
3. Seguir las instrucciones del apartado de instalación de este readme.


## Endpoints
Los endpoints son una parte fundamental de este proyecto debido a que se están mandando y recibiendo peticiones constantemente de tipo GET, POST, PUT, DELETE. Es por eso que se anexa el siguiente link. Esta es una documentación de Postman detallada sobre todos los endpoints que usa el aplicativo
[Documentación Postman](https://documenter.getpostman.com/view/32617811/2sA2r3Z6EG)
