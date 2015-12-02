Plataforma ARDUINO y JAVASCRIPT

Instalación de un entorno de desarrollo y generación de un proyecto arduino usando **node.js y johnny-five.js**

[[TOC]]

# Sistema operativo

**Ubuntu 14.04.3 LTS**

[Ubuntu 14.04.3 LTS Desktop (64-bit) ](http://releases.ubuntu.com/14.04.3/ubuntu-14.04.3-desktop-amd64.iso.torrent)

# Instalación JAVA

**sudo apt-get update **

**sudo apt-get install default-jre**

**sudo apt-get install default-jdk**

# Instalación Arduino

## Instalación de dependencias

**sudo apt-get update **

**sudo apt-get install arduino arduino-core**

## Open-source Arduino Software

**wget ****https://www.arduino.cc/download_handler.php?f=/arduino-1.6.5-linux64.tar.xz**

**tar xvfJ arduino-1.6.5-linux64.tar.xz**

## Error permiso denegado

Si te encuentras con un error de este tipo:

Error opening serial port '/dev/ttyACM0'. (Permission denied)

Usar el siguiente comando:

**sudo usermod -a -G tty <usuario>**

**sudo usermod -a -G dialout <usuario>**

**sudo chmod a+rw /dev/ttyACM0**

## Establecer el StandardFirmata 

Abrir y ejecutar el siguiente sketch desde Arduino Software:

**~/arduino-1.6.5/libraries/Firmata/examples/StandardFirmata/StandardFirmata.ino**

# Instalación Node.js

## Eliminar paquetes de node instalados previamentes

**dpkg --get-selections | grep node**

**sudo apt-get remove --purge node**

## Instalación de node y npm

**sudo apt-get install nodejs**

**sudo apt-get install npm**

**sudo ln -s /usr/bin/nodejs /usr/bin/node**

## Error npm install -g [package]

**sudo chown -R $USER /usr/local**

# Crear un proyecto 

## Instalación Yeoman

**npm install -g yo**

## Instalación Johnny-five yeoman generator

**npm install -g generator-johnny-five**

## Generación del proyecto

**mkdir <directorio del proyecto>**

**cd <directorio del proyecto>**

**yo johnny-five**

![image alt text](img/image_0.png)

![image alt text](img/image_1.png)

![image alt text](img/image_2.png)

![image alt text](img/image_3.png)

