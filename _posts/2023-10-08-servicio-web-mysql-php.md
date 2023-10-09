---
title: Montaje del servicio WEB, MySQL y PHP
date: 2023-09-25 12:00:00 +0100
categories: [Sistemas Microinformáticos y Redes, Servicios en red]
tags: [redes locales, teoría, smr]
img_path: /assets/img/web/
image: 
    path: apache.png
---

# Introducción
Un servidor web es un componente fundamental de la infraestructura de Internet que desempeña un papel crucial en la entrega de contenido en línea. En esencia, un servidor web es un software o hardware que almacena, gestiona y distribuye páginas web, archivos, imágenes y otros recursos a través de Internet. Está diseñado para recibir solicitudes de clientes web, como navegadores de Internet, y responder a esas solicitudes enviando los archivos correspondientes para que los usuarios puedan ver y interactuar con ellos en sus dispositivos.

# Instalación del servicio en Ubuntu Server 22.04 LTS

## Cosas necesarias previas a la instalación
- Configuración de MV servidor en red nat
- MV cliente Xubuntu en la misma red nat
- Configuración red nat 192.168.100.0/24

Con permisos de root ejecutamos el comando:

```console
sudo apt-get install apache2
```

Comprobamos que el servicio está activo en su puerto 80:

```console
netstat -putona
```

Otra opción para comprobar que el servicio está activo:

```console
sudo /etc/init.d/apache2 status
```

La ubicación de nuestros archivos es
```
cd /var/www/html/
```

Podemos realizar pruebas en nuestro navegador de Host y poner en la dirección _localhost_

Una página de ejemplo podría ser:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Página Web de Ejemplo</title>
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Página Web de Ejemplo</h1>
        <nav>
            <ul>
                <li><a href="#">Inicio</a></li>
                <li><a href="#">Acerca de</a></li>
                <li><a href="#">Servicios</a></li>
                <li><a href="#">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section>
            <h2>Acerca de Nosotros</h2>
            <p>Somos una empresa ficticia dedicada a brindar soluciones imaginarias.</p>
        </section>

        <section>
            <h2>Nuestros Servicios</h2>
            <ul>
                <li>Servicio 1</li>
                <li>Servicio 2</li>
                <li>Servicio 3</li>
            </ul>
        </section>
    </main>

    <footer>
        <p>Derechos de autor &copy; 2023 Mi Página Web de Ejemplo</p>
    </footer>
</body>
</html>
```

## Logs de Apache2
```
sudo tail -f /var/log/apache2/access.log
```
```
sudo tail -f /var/log/apache2/error.log
```
```
sudo tail -n 100 /var/log/apache2/access.log
```

## Archivos de configuración de Apache2
```
# This is the main Apache server configuration file.
sudo vim /etc/apache2/apache2.conf

# If you just change the port or add more ports here
sudo vim /etc/apache2/port.conf

# Default Apache virtualhost
sudo vim /etc/apache2/site-available/default.conf
```

Y para validar la configuración de Apache2
```
sudo apache2ctl configtest
```

## Extras

Cambia el puerto 80 al 8080
Investiga para que sirve el archivo default.conf