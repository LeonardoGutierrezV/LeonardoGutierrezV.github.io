---
layout: single
title: Archivos CPL
excerpt: "Listado y explicación rápida sobre que son y para que sirven archivos **.CPL** de windows."
date: 2021-11-04
classes: guía
header:
  teaser: /assets/images/archivos-cpl/logo.png
  teaser_home_page: true
  icon: /assets/images/win_icon.png
categories:
  - Windows
  - Configuración
tags:
  - Windows
  - Configuración
  - Documentación
---

## Archivos CPL

Un archivo CPL (Control Palen Launcher), no es otra cosa que un archivo que apunta a un elemento del panel de control. Estos archivos nos dan un acceso directo y simple a administración y configuración del sistema operativo Windows.


Para poder ejecutar un elemento del panel de control lo podemos hacer de las siguientes maneras.

Si quisieramos abrir el Administrador de Dispositivos de Windows.

![](/assets/images/genericos/AdmDisp.png)

Podríamos hacerlo de las siguientes maneras.

### Desde el explorador de archivos de windows.

En el caso de que tengamos una ventana del explorador de archivos abierta, podríamos teclear en la barra de dirección de esta ventana una instrucción que llama el elemento del panel de control que deseamos ejecutar.

![](/assets/images/genericos/fexplorer.png)

Instrucción:**control /name Microsoft.DeviceManager**

### Desde la ventana Ejecutar.

En este caso debemos mantener presionada la tecla Windows y presionar la tecla R **(Win+R)** y se mostrara la ventana ejecutar.

![](/assets/images/genericos/wejecutar.png)

Es en esta ventana que tendríamos que escribir la instrucción para mostrar el elemento del panel de control.

Instrucción:**control /name Microsoft.DeviceManager**

## Desde la ventana Ejecutar, utilizando el nombre del archivo CPL.

Tal como se mostro en el apartado anterior debemos mostrar la ventana ejecutar mediante la combinación de teclas (Win+R). Con la diferencia que escribiremos directamente el nombre del archivo. Solo que en este caso escribiremos directamente el nombre del archivo CPL.

Archivo: **hdwwiz.cpl**

Obteniendo el mismo resultado.

## Archivos CPL de uso común

 | Archivo | Elemento del panel de control. | 
 |--- |--- |
 | appwiz.cpl | Programas y características. | 
 | bthprops.cpl | Panel de control Bluetooth. | 
 | desk.cpl | Ajustes de pantalla. | 
 | firewall.cpl | Firewall de Windows. | 
 | hdwwiz.cpl | Administrador de dispositivos. | 
 | inetcpl.cpl | Propiedades de internet. | 
 | intl.cpl | Configuración regional y de idioma. | 
 | joy.cpl | Dispositivos de juego. | 
 | main.cpl | Mouse. | 
 | mmsys.cpl | Sonido. | 
 | ncpa.cpl | Conexiones de red. | 
 | powercfg.cpl | Opciones de energía de Windows. | 
 | sysdm.cpl | Propiedades del Sistema. | 
 | timedate.cpl | Fecha y hora de sistema. | 
 | wscui.cpl | Seguridad y Mantenimiento. | 

Es de utilidad conocer el nombre de los archivos CPL y el apartado del panel de control que lanzan, para poder simplificar y agilizar la gestión, administración y configuración del Sistema Operativo Windows sin la necesidad de depender del teclado o por comodidad y simplicidad.