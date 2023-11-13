---
title: Servicio FTP con usuarios virtuales de AD en Windows Server
date: 2023-11-13 12:00:00 +0100
categories: [Sistemas Microinformáticos y Redes, Servicios en red]
tags: [redes locales, teoría, smr]
img_path: /assets/img/FTP/Windows/
---

# Activar escritorio remoto en Windows Server 2012R2

En este tutorial, te guiaremos a través del proceso de instalación de un servidor FTP en un entorno Windows Server, aprovechando la integración con Active Directory para gestionar usuarios y aplicando medidas de seguridad esenciales.

## Paso 1: Preparación del Entorno

Antes de comenzar, asegúrate de que tu servidor Windows está correctamente configurado y tiene instalado el servicio Active Directory. Esto proporcionará la base para gestionar usuarios de manera centralizada.

## Paso 2: Instalación del Servicio FTP

Abre el "Administrador del Servidor" en tu Windows Server.
Selecciona "Administrar" y luego "Agregar roles y características".
Sigue el asistente de instalación, seleccionando el rol "Servidor FTP" y cualquier característica adicional que necesites.
Completa la instalación y asegúrate de habilitar la opción "Habilitar el soporte para FTP básico" y "Habilitar el soporte para FTP de escritura".

![Alt text](<Captura de pantalla 2023-11-10 194121.png>)
![Alt text](<Captura de pantalla 2023-11-10 194520.png>)
![Alt text](<Captura de pantalla 2023-11-10 194134.png>)
![Alt text](<Captura de pantalla 2023-11-10 194531.png>)

Una vez instalado todo vamos a configurar el AD con las siguientes características:
- Dominio raíz: Axuquer.local
- Establecemos la contraseña
- NetBIOS: AXUQUER

![Alt text](<Captura de pantalla 2023-11-10 195344.png>)
![Alt text](<Captura de pantalla 2023-11-10 195440.png>)
![Alt text](<Captura de pantalla 2023-11-10 195509.png>)
![Alt text](<Captura de pantalla 2023-11-10 195535.png>)
![Alt text](<Captura de pantalla 2023-11-10 195550.png>)
![Alt text](<Captura de pantalla 2023-11-10 195641.png>)

## Paso 3: Configuración del Servidor FTP

Abre el "Administrador de IIS" (Internet Information Services).
Navega hasta el nodo del servidor y selecciona "Sitios FTP".
Haz clic derecho en "Sitio FTP predeterminado" y selecciona "Configurar seguridad de autenticación".
Habilita la autenticación básica y la autenticación anónima si es necesario.

## Paso 4: Integración con Active Directory

En el "Administrador de Servidores", selecciona "Herramientas" y luego "Usuarios y Equipos de Active Directory".
Crea los usuarios que necesitarás para acceder al servidor FTP.
Asegúrate de que estos usuarios tengan permisos adecuados en las carpetas del servidor FTP.
Paso 5: Establecer Seguridad Adicional

Para mejorar la seguridad, considera las siguientes medidas:

Configuración de Firewall: Ajusta las reglas de firewall para permitir el tráfico FTP.
Uso de SSL/TLS: Habilita el cifrado mediante SSL/TLS para proteger la transferencia de datos.
Monitoreo de Registro: Configura el registro del servidor FTP para registrar eventos de seguridad.
Actualizaciones y Parches: Mantén tu servidor actualizado con las últimas actualizaciones de seguridad de Microsoft.
Con estos pasos, habrás instalado un servidor FTP en Windows Server, integrado con Active Directory y reforzado con medidas de seguridad. Recuerda realizar pruebas exhaustivas y ajustar la configuración según las necesidades específicas de tu entorno. ¡Ahora tu servidor FTP está listo para proporcionar un acceso seguro y gestionado a tus archivos!
