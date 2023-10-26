---
title: Montaje del servicio IIS, SQL Server y ASP
date: 2023-10-25 12:00:00 +0100
categories: [Sistemas Microinformáticos y Redes, Servicios en red]
tags: [redes locales, teoría, smr]
img_path: /assets/img/windowsWeb/   
---

![Instalación de ISS](1.png)
_Instalación de IIS_
![Instalación de ISS](2.png)
_Instalación de IIS_
![Instalación de ISS](3.png)
_Instalación de IIS_
![Instalación de ISS](4.png)
_Instalación de IIS_
![Instalación de ISS](5.png)
_Instalación de IIS_
![Instalación de ISS](6.png)
_Instalación de IIS_
![Instalación de ISS](7.png)
_Instalación de IIS_
![Instalación de ISS](8.png)
_Instalación de IIS_
![Instalación de ISS](9.png)
_Instalación de IIS_
![Instalación de ISS](10.png)
_Instalación de IIS_
![Instalación de ISS](11.png)
_Instalación de IIS_
![Instalación de ISS](12.png)
_Instalación de IIS_

## Creación de tabla en SQL Server

```
USE NombreDeTuBaseDeDatos; -- Reemplaza "NombreDeTuBaseDeDatos" con el nombre de tu base de datos

CREATE TABLE TuTabla (
    ID INT PRIMARY KEY,
    Nombre VARCHAR(50),
    Apellido VARCHAR(50),
    Edad INT
);
```


## Página web conexión a SQL Server

```
<%
' Definir la cadena de conexión a la base de datos
Dim connStr
connStr = "Provider=SQLOLEDB;Data Source=nombre_servidor;Initial Catalog=nombre_bd;User ID=usuario;Password=contraseña;"

' Crear una conexión a la base de datos
Dim conn
Set conn = Server.CreateObject("ADODB.Connection")
conn.Open connStr

' Definir una consulta SQL
Dim strSQL
strSQL = "SELECT * FROM MiTabla"

' Crear un objeto de registro (recordset) y ejecutar la consulta
Dim rs
Set rs = Server.CreateObject("ADODB.Recordset")
rs.Open strSQL, conn

' Recorrer los resultados y mostrarlos
Do Until rs.EOF
    Response.Write(rs("NombreCampo") & "<br />")
    rs.MoveNext
Loop

' Cerrar el recordset y la conexión a la base de datos
rs.Close
Set rs = Nothing
conn.Close
Set conn = Nothing
%>
```