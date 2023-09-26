---
title: Clasificación de las redes
date: 2023-09-25 12:00:00 +0100
categories: [Sistemas Microinformáticos y Redes, Redes Locales]
tags: [redes locales, teoría, smr]
img_path: /assets/img/introduccion-redes-locales/
---
# Introducción:

Las infraestructuras de red pueden variar en gran medida en términos de:

- El tamaño del área que abarcan.
- La cantidad de usuarios conectados.
- La cantidad y los tipos de servicios disponibles.
- El área de responsabilidad.

Los dos tipos más comunes de infraestructuras de red son las redes de área local (LAN) y las redes de área amplia (WAN). Una LAN es una infraestructura de red que proporciona acceso a usuarios y dispositivos finales en un área geográfica pequeña. Normalmente, una LAN se utiliza en un departamento dentro de una empresa, un hogar o una red de pequeñas empresas. Una WAN es una infraestructura de red que proporciona acceso a otras redes en un área geográfica amplia, que generalmente es propiedad y está administrada por una corporación más grande o un proveedor de servicios de telecomunicaciones.

# LAN

Una red LAN, o Red de Área Local, es un conjunto de dispositivos de comunicación interconectados dentro de un área geográfica limitada, como un edificio, una escuela, una empresa u otro espacio relativamente pequeño. Estas redes están diseñadas para permitir que los dispositivos, como ordenadores, impresoras, teléfonos y otros dispositivos electrónicos, se comuniquen y compartan recursos de manera eficiente y rápida.

## 1. Propósito de una LAN:

- Compartir recursos: Las LAN permiten compartir recursos como impresoras, archivos, conexiones a internet y dispositivos de almacenamiento entre varios dispositivos conectados a la red. Esto reduce la duplicación de recursos y facilita el acceso a los mismos.

- Comunicación: Las LAN permiten la comunicación instantánea entre dispositivos conectados. Esto es crucial en un entorno empresarial para el intercambio de información y la colaboración entre empleados.

- Acceso a internet: Las LAN suelen proporcionar acceso compartido a internet para todos los dispositivos conectados, lo que permite a los usuarios acceder a recursos en línea y servicios basados en la web.

- Centralización de servicios: Algunas LAN también pueden centralizar servicios como autenticación, seguridad y almacenamiento de datos, lo que facilita la gestión de la red y la aplicación de políticas de seguridad.

## 2. Componentes de una LAN:

- Dispositivos finales: Estos son los dispositivos que se conectan a la red, como ordenadores, portátiles, tablets, teléfonos, impresoras y otros dispositivos electrónicos.

- Dispositivos de red: Estos incluyen routers, switches y puntos de acceso inalámbrico (APs). Los enrutadores conectan la LAN a otras redes, como internet. Los switches se utilizan para conectar los dispositivos finales entre sí en la LAN, mientras que los APs permiten conexiones inalámbricas.

- Medios de transmisión: Los medios de transmisión son los cables o conexiones inalámbricas que permiten la comunicación entre dispositivos. Los cables Ethernet son comunes en las LAN con cable, mientras que las LAN inalámbricas utilizan ondas de radio para la comunicación.

## 3. Topologías de LAN:
Las redes LAN pueden tener diferentes topologías, que se refieren a la forma en que los dispositivos están conectados físicamente. Algunas topologías comunes incluyen:

- Estrella: Todos los dispositivos están conectados a un centro, como un conmutador o un enrutador. Si un dispositivo necesita comunicarse con otro, la información pasa a través del centro.

- Bus: Todos los dispositivos están conectados a un solo cable, llamado bus. La información se envía a través del bus y todos los dispositivos pueden escucharla, pero solo el destinatario adecuado la procesa.

- Anillo: Los dispositivos están conectados en un círculo cerrado, donde la información circula en una dirección constante. Cada dispositivo recibe y retransmite la información.

## 4. Protocolos y estándares:
- Las LAN utilizan protocolos y estándares para garantizar que los dispositivos puedan comunicarse entre sí. Algunos ejemplos de protocolos comunes en una LAN incluyen TCP/IP (para la comunicación en internet), Ethernet (para la transmisión de datos en redes con cable) y Wi-Fi (para redes inalámbricas).

## 5. Seguridad y administración:
- La seguridad es un aspecto crítico en la gestión de una LAN. Se utilizan medidas como cortafuegos, sistemas de detección de intrusiones, autenticación de usuarios y cifrado de datos para proteger la red contra amenazas externas e internas. La administración de la LAN implica la configuración, el monitoreo y el mantenimiento de los dispositivos y recursos para garantizar un funcionamiento óptimo.

En resumen, una red LAN es un componente fundamental en entornos empresariales y domésticos para facilitar la comunicación y el intercambio de recursos entre dispositivos dentro de un área geográfica limitada. Proporciona la base para la conectividad de dispositivos y el acceso a servicios en línea, y su diseño y gestión son esenciales para garantizar un funcionamiento eficiente y seguro.

# MAN

Una red MAN (Metropolitan Area Network, por sus siglas en inglés) es un tipo de red de comunicación que abarca un área geográfica metropolitana o una ciudad. Es una red intermedia entre las redes de área local (LAN) que cubren áreas pequeñas, como edificios o campus, y las redes de área amplia (WAN) que abarcan áreas geográficas extensas, como regiones, países o continentes.

## 1. Propósito y Alcance de una MAN:

- Cobertura Metropolitana: La principal característica de una MAN es que abarca una zona geográfica más grande que una LAN pero más pequeña que una WAN. Esta área suele ser una ciudad o una región metropolitana.

- Conexión de Áreas Urbanas: Las MAN se utilizan para interconectar diferentes ubicaciones dentro de una ciudad o una región metropolitana. Esto permite la comunicación y el intercambio de datos entre sitios que pueden estar a varios kilómetros de distancia.

- Soporte de Aplicaciones Urbanas: Las MAN son útiles para respaldar aplicaciones específicas de áreas metropolitanas, como servicios de videoconferencia, transmisión de datos a alta velocidad, sistemas de vigilancia y acceso a internet de alta velocidad para empresas y usuarios.

## 2. Componentes de una MAN:

- Enrutadores y Dispositivos de Red: Al igual que en las LAN y WAN, los routers desempeñan un papel fundamental en una MAN. Dirigen el tráfico de datos entre diferentes ubicaciones de la red y determinan la mejor ruta para que los datos lleguen a su destino.

- Fibra Óptica y Otros Medios de Transmisión: Dado que las MAN suelen cubrir distancias más largas que las LAN, a menudo utilizan medios de transmisión de alta velocidad, como cables de fibra óptica, para transmitir datos de manera eficiente a través de la ciudad.

- Tecnologías de Acceso: Las MAN pueden utilizar una variedad de tecnologías de acceso, como Ethernet metropolitano, redes de fibra óptica, redes de área amplia inalámbrica y otros métodos para conectar ubicaciones remotas.

## 3. Topologías y Diseño de una MAN:

- Topología de Anillo: En una MAN, una topología de anillo es común, donde las ubicaciones se conectan en un círculo cerrado. Esto proporciona redundancia y tolerancia a fallos, ya que si un enlace falla, los datos pueden seguir circulando en la otra dirección.

- Topología de Estrella: También es posible utilizar una topología de estrella, donde todas las ubicaciones se conectan a un punto central de la red, como un nodo principal o un centro de datos.

## 4. Seguridad y Administración:

- Seguridad: Al igual que en otras redes, la seguridad es un aspecto crítico de las MAN, ya que transmiten datos a través de áreas urbanas densamente pobladas. Se implementan medidas de seguridad, como cortafuegos, sistemas de detección de intrusiones y autenticación, para proteger la red y los datos transmitidos.

- Administración y Supervisión: La administración de una MAN implica la configuración y el monitoreo continuo de dispositivos de red, la gestión del ancho de banda y la implementación de políticas de seguridad en toda la red metropolitana.

## 5. Ejemplos de MAN:

- Metro Ethernet: Es un ejemplo común de una MAN que utiliza tecnología Ethernet para proporcionar servicios de comunicación de alta velocidad en áreas metropolitanas.

- Redes de Telecomunicaciones: Las redes de telefonía móvil y las redes de acceso a internet de alta velocidad en áreas metropolitanas son ejemplos de MAN que ofrecen servicios de comunicación a los usuarios urbanos.

- Redes de Transporte Público: Algunas ciudades utilizan MAN para supervisar y gestionar sistemas de transporte público, como sistemas de trenes o autobuses.

En resumen, una red MAN es un tipo de infraestructura de comunicación que conecta ubicaciones dentro de una ciudad o una región metropolitana, permitiendo la comunicación y el intercambio de datos a distancias metropolitanas. Estas redes son fundamentales para respaldar aplicaciones urbanas y proporcionar servicios de comunicación eficientes en áreas densamente pobladas.

# WAN

Una red WAN, o Red de Área Amplia (Wide Area Network, en inglés), es un tipo de red de comunicación que abarca un área geográfica extensa, generalmente a nivel regional, nacional o incluso internacional. A diferencia de las redes LAN (Redes de Área Local), que se limitan a un espacio geográfico pequeño, las WAN conectan múltiples LAN dispersas geográficamente para permitir la comunicación y el intercambio de datos a larga distancia.

## 1. Propósito y Alcance de una WAN:

- Conexión de ubicaciones remotas: El propósito principal de una WAN es conectar diferentes ubicaciones geográficas, como oficinas, sucursales, campus universitarios o filiales de una empresa, que pueden estar separadas por grandes distancias geográficas.

- Comunicación a larga distancia: Las WAN permiten la comunicación y el intercambio de datos entre ubicaciones distantes, lo que facilita la colaboración, el acceso a recursos compartidos y la transmisión de información crítica entre lugares lejanos.

- Acceso a recursos centralizados: A través de una WAN, las sucursales pueden acceder a recursos centralizados, como bases de datos, servidores de correo electrónico y sistemas de gestión empresarial, ubicados en la sede principal de la organización.

## 2. Componentes de una WAN:

- Routers y Enrutadores: Los routers son dispositivos clave en una WAN. Se utilizan para dirigir el tráfico de datos entre diferentes ubicaciones de la red, determinando la mejor ruta para que los datos lleguen a su destino.

- Circuitos y Líneas de Comunicación: Las WAN suelen utilizar líneas de comunicación de alta velocidad, como líneas telefónicas dedicadas, líneas de fibra óptica, conexiones satelitales o conexiones de Internet de banda ancha para transmitir datos a larga distancia.

- Protocolos WAN: Para garantizar la interoperabilidad entre diferentes dispositivos y tecnologías de red en una WAN, se utilizan protocolos WAN estándar, como el Protocolo de Internet (IP) y el Protocolo de Control de Transmisión (TCP).

## 3. Topologías y Diseño de una WAN:

- Topología de Estrella: En una WAN, una topología de estrella es común, donde todas las ubicaciones remotas se conectan a una ubicación central (a menudo la sede principal de la organización).

- Topología de Malla: En una topología de malla, cada ubicación remota se conecta directamente con todas las demás ubicaciones remotas, lo que proporciona redundancia y una mayor tolerancia a fallos.

- Tecnologías de Acceso: Las WAN pueden utilizar una variedad de tecnologías de acceso, como líneas contratadas, conexiones VPN (Redes Privadas Virtuales) a través de Internet, conexiones satelitales o conexiones de fibra óptica, dependiendo de la disponibilidad y los requisitos de velocidad.

## 4. Seguridad y Administración:

- Seguridad: Debido a que las WAN transmiten datos a larga distancia, la seguridad es fundamental. Se implementan medidas de seguridad, como firewalls, cifrado de datos y autenticación, para proteger la confidencialidad y la integridad de los datos transmitidos.

- Administración y Supervisión: La administración de una WAN implica la configuración y el monitoreo continuo de los dispositivos de red, la resolución de problemas, la gestión del ancho de banda y la implementación de políticas de seguridad en todas las ubicaciones remotas.

## 5. Ejemplos de WAN:

- Internet: La World Wide Web es un ejemplo masivo de una WAN que conecta usuarios y organizaciones de todo el mundo.

- Redes Corporativas: Empresas con múltiples sucursales utilizan WAN para conectar sus oficinas y permitir la transferencia de datos y la comunicación en tiempo real entre ellas.

- Redes de Telefonía: Las redes de telefonía móvil y las redes de telefonía fija utilizan WAN para conectar torres de telefonía y centrales telefónicas en todo un país o región.

En resumen, una red WAN es una infraestructura de comunicación esencial que conecta ubicaciones geográficamente dispersas, facilitando la comunicación y el intercambio de datos a larga distancia. Estas redes son vitales para empresas, organizaciones y la conectividad global en la era digital.

# Otras redes:

- LAN inalámbrica (WLAN): Wireless Local Area Network – son similares a las LAN, solo que interconectan de forma inalámbrica a los usuarios y los extremos en un área geográfica pequeña.
- Red de área de almacenamiento (SAN): Storage Area Network – son infraestructuras de red diseñadas para admitir servidores de archivos y proporcionar almacenamiento, recuperación y replicación de datos.
- Red de área Personal (PAN): PAN – Personal Area Network – es definitivamente el tipo más pequeño de red que puede usar actualmente y el nombre proviene de la red de área personal. Probablemente haya usado esto en la última semana sin siquiera saberlo. Es la red interconectada de dispositivos tecnológicos al alcance de una persona individual, pero generalmente limitada a un alcance de 10 metros como máximo.

# El Internet

Internet es una colección global de redes interconectadas (internetworks o internet para abreviar). En la figura se muestra una forma de ver a la Internet como una colección de LAN y WAN interconectadas.

Algunos de los ejemplos de LAN están conectados entre sí a través de una conexión WAN. Las WAN se conectan entre sí. Las líneas de conexión WAN rojas representan todas las variedades de formas en que conectamos las redes. Las WAN pueden conectarse a través de cables de cobre, cables de fibra óptica y transmisiones inalámbricas (no se muestran).

Asegurar una comunicación efectiva a través de esta infraestructura diversa requiere la aplicación de tecnologías y estándares consistentes y comúnmente reconocidos, así como la cooperación de muchas agencias de administración de redes. Hay organizaciones que se desarrollaron para ayudar a mantener la estructura y la estandarización de los protocolos y procesos de Internet. Estas organizaciones incluyen el Internet Engineering Task Force (IETF), Internet Corporation for Assigned Names and Numbers (ICANN), y el Internet Architecture Board (IAB), además de muchos otros.

# Intranets y Extranets
Hay otros dos términos que son similares al término internet: intranet y extranet.

El término intranet se utiliza para referirse a la conexión privada de LAN y WAN que pertenecen a una organización. Una intranet está diseñada para que solo puedan acceder a ella los miembros y empleados de la organización, u otras personas autorizadas.

Es posible que una organización utilice una extranet para proporcionar acceso seguro a las personas que trabajan para otra organización, pero requieren datos de la empresa. Aquí hay algunos ejemplos de extranets:

- Una empresa que proporciona acceso a proveedores y contratistas externos.
- Un hospital que proporciona un sistema de reservas a los médicos para que puedan hacer citas para sus pacientes.
- Una secretaría de educación local que proporciona información sobre presupuesto y personal a las escuelas del distrito.

La figura ilustra los niveles de acceso que los diferentes grupos tienen a una intranet de la empresa, a una extranet de la empresa y a Internet.

# Redes por tología física
## 1.Red en bus

Una red en bus es aquella topología que se caracteriza por tener un único bus de comunicaciones (denominado bus, troncal o backbone) al cual se conectan los diferentes dispositivos. De esta forma todos los dispositivos comparten el mismo canal.

![Red en bus](../assets/img/topologias/topologia-red-bus.webp)
_Red en bus_

### Ventajas
- Facilidad de implementación y crecimiento.
- Fácil adaptación.
- Simplicidad en la arquitectura.
- Es una red que no ocupa mucho espacio.

### Desventajas
- Hay un límite de equipos dependiendo de la calidad de la señal.
- Puede producirse degradación de la señal.
- Complejidad de reconfiguración y aislamiento de fallos.
- Limitación de las longitudes físicas del canal.
- Un problema en el canal usualmente degrada toda la red.
- El canal requiere ser correctamente cerrado (caminos cerrados).
- Altas pérdidas en la transmisión debido a colisiones entre mensajes.
- Alta demanda
- ocupa mucho espacio.
- Hay mejores opciones de red.

