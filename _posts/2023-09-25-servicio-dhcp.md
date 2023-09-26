---
title: Montaje del servicio DHCP
date: 2023-09-25 12:00:00 +0100
categories: [Sistemas Microinformáticos y Redes, Servicios en red]
tags: [redes locales, teoría, smr]
img_path: /assets/img/DHCP/
image: 
    path: diagrama-topologia-de-red-en-arbol.webp
---

# Introducción
El protocolo DHCP es uno de los más utilizados por los routers, tanto domésticos como también profesionales. De manera predeterminada cualquier cliente cableado o WiFi está configurado para obtener una dirección IP por DHCP. Aunque continuamente se está utilizando el DHCP, ¿sabes para qué sirve?

Por más que este protocolo sea tan utilizado, lo cierto es que seguramente no conozcas para qué sirve exactamente. Además de esto, no todo el mundo conoce cada una de sus funcionalidades y también cómo funciona. Entre otros aspectos, también puedes encontrar qué mensajes se intercambian entre el servidor y los clientes. Por eso mismo, en RedesZone puedes encontrar todo lo que debes saber sobre el protocolo DHCP.

# ¿Qué es y para qué sirve este protocolo?
El protocolo DHCP (Protocolo de configuración dinámica de host) o también conocido como «Dynamic Host Configuration Protocol«, es un protocolo de red que utiliza una arquitectura cliente-servidor. Por tanto, tendremos uno o varios servidores DHCP y también uno o varios clientes, que se deberán comunicar entre ellos correctamente para que el servidor DHCP brinde información a los diferentes clientes conectados.

Este protocolo se encarga de asignar de manera dinámica y automática una dirección IP, ya sea una dirección IP privada desde el router hacia los equipos de la red local, o también una IP pública por parte de un operador que utilice este tipo de protocolo para el establecimiento de la conexión.

Cuando tenemos un servidor DHCP en funcionamiento, todas las direcciones IP que ha proporcionado a diferentes clientes se guardan en un listado donde se relaciona la IP que se le ha proporcionado (dirección lógica) y la dirección MAC (dirección física de la tarjeta de red). Gracias a este listado, el servidor DHCP se asegura de no proporcionar a dos equipos diferentes la misma dirección IP, lo que ocasiona un caos en la red local.

A medida que el servidor va asignando direcciones IP, también tiene en cuenta cuándo pasa un determinado tiempo y caducan, quedando libres para que otro cliente pueda obtener esta misma dirección IP. El servidor DHCP sabrá en todo momento quién ha estado en posesión de una dirección IP, cuánto tiempo ha estado, y cuándo se ha asignado a otro cliente.

El protocolo DHCP incluye varias formas de asignación de direcciones IP, dependiendo de la configuración que realicemos y el escenario, podremos usar una forma de asignación u otra:

- Manual o estática: el servidor DHCP nos permitirá configurar un listado de parejas IP-MAC con el objetivo de que siempre se le proporcione a un cliente una determinada dirección IP, y que esta dirección no cambie nunca.
- Automática: el servidor DHCP se encarga de proporcionar una dirección IP al cliente que realiza la solicitud, y estará disponible para este cliente hasta que la libere. Existen routers que internamente están configurados para proporcionar direcciones IP privadas de forma secuencial, sin embargo, hay firmwares que están diseñados para proporcionar una dirección IP específica dentro del rango y que no es secuencial, en base a un algoritmo interno y la dirección MAC que se haya conectado.
- Dinámica: este método permite reutilización dinámica de las direcciones IP.
Aunque el protocolo DHCP es muy conocido por proporcionar la dirección IP, máscara de subred y la puerta de enlace, tres parámetros básicos y fundamentales, también es capaz de proporcionar otra información de cara a los clientes, como los siguientes parámetros que son configurables y opcionales:

- Servidor DNS primario y secundario.
- Nombre DNS.
- MTU para la interfaz.
- Servidor y dominio NIS.
- Servidores NTP.
- Servidor de nombre WINS para Windows.
- Otras opciones avanzadas.

Un aspecto muy importante es que, si un sistema Windows no es capaz de obtener una dirección IP a través del cliente DHCP en una red, se inicia un proceso llamado APIPA (Automatic Private Internet Protocol Addressing). Este proceso APIPA que usan los sistemas operativos cuando no se puede obtener una dirección IP por DHCP, este protocolo se encarga de asignar una dirección IP privada de clase B en el rango 169.254.0.0/16 con su correspondiente máscara de subred 255.255.0.0.

Este bloque de direccionamiento se conoce como «link–local» para redes IPv4. Aunque los sistemas operativos se autoconfigure esta dirección IP privada, cada 5 minutos volverán a consultar si hay un servidor DHCP en la red para que les proporcione una dirección IP privada de clase A, B o C habitual. Cuando no funciona el servidor DHCP o no lo tenemos configurado, podéis comprobar la dirección IP que se configura automáticamente si consultamos la IP privada que tenemos en nuestro equipo.

Una vez que ya conocemos qué es el protocolo DHCP y sus principales características, vamos a ver su funcionamiento y qué mensajes se intercambian.

# Instalación del servicio en Ubuntu Server 22.04 LTS

## Cosas necesarias previas a la instalación
- Configuración de MV en red nat
- MV Xubuntu en la misma red nat (Configuración interna DHCP)
- Red 192.168.100.0/24

Con permisos de root ejecutamos el comando:

```console
sudo apt-get install isc-dhcp-server
```

Comprobamos que el servicio está activo en su respectivo puerto:

```console
netstat -putona
```

Tras completar la instalación del servidor vamos a definir la interfaz de red sobre la que funcionará el servidor DHCP. Para este laboratorio de ejemplo será *enp0s3*, por lo que declaramos esta interfaz de IPv4 en */etc/default/isc-dhcp-server*

```console
INTERFACESV4="enp0s3"
INTERFACESV6=""
```

Lo siguiente es configurar nuestro DHCP, para ello vamos a */etc/dhcp* y editamos el fichero *dhcpd.conf*

Podemos comprobar la sintaxis con:

```console
dhcpd -t -cf /etc/dhcp/dhcpd.conf
```
De ser errónea nos mostrara el punto donde se encontró el error, este sería el output que se recibe si no hay fallos de sintaxis:

Tras esta configuración solo queda reiniciar el servidor y comprobar que se encuentra en buen estado:

```console
service isc-dhcp-server restart
service isc-dhcp.server status
```

## Comprobación
En una máquina cliente Xubuntu vamos a las propiedades de red IPv4 y marcamos la opción para que asigne los parámetros de red automáticamente, tras eso podemos hacer un *ip a* para verificar que nos ha dado una IP del rango que hemos definido en la configuración del DHCP.

```console
ip a
```

## Extras