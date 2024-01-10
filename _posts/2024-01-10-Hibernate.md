---
title: Hibernate
date: 2024-01-10 12:00:00 +0100
categories: [Desarrollo Aplicaciones Multiplataforma, Acceso Datos]
tags: [acceso a datos, teoría, 2DAM]
img_path: /assets/img/hibernate/
---

# Hibernate
Con la siguiente estructura SQL:

```SQL
CREATE DATABASE canciones;

CREATE TABLE `song` (
  `songId` int(11) NOT NULL,
  `songName` varchar(25) NOT NULL,
  `singer` varchar(25) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
```

1. Añadimos las librerías, deben quedar de la siguiente manera:
![Alt text](<Captura de pantalla 2024-01-10 200549.png>)
![Alt text](<Captura de pantalla 2024-01-10 200537.png>)
![Alt text](<Captura de pantalla 2024-01-10 200802.png>)

1. Añadimos un archivo XML dento de nuestro proyecto, se debe llamar **hibernate.cfg.xml* con el siguiente contenido:
   
```XML
<?xml version = "1.0" encoding = "utf-8"?>
<!DOCTYPE hibernate-configuration PUBLIC
        "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
        "http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">
<hibernate-configuration>
    <session-factory>
        <property name = "hibernate.connection.driver_class">com.mysql.jdbc.Driver</property>
        <!-- Set URL -->
        <property name = "hibernate.connection.url">jdbc:mysql://localhost:3306/canciones</property>
        //<property name = "hibernate.connection.url">jdbc:mysql://**direccion_server**:**puerto**/**nombre_BBDD**</property>
        <!-- Set User Name -->
        <property name = "hibernate.connection.username">2DAM</property>
        //<property name = "hibernate.connection.username">**User_BBDD**</property>
        <!-- Set Password -->
        <property name = "hibernate.connection.password">2DAM2023</property>
        //<property name = "hibernate.connection.password">**Pass_BBDD**</property>
        <!-- Set Driver Name -->
        <property name = "hibernate.show_sql">true</property>
        
    </session-factory>
</hibernate-configuration>
```
```
```

1. Añadimos una clase con el siguiente contenido:
   
```JAVA
// Importing required classes
import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.Id;
import javax.persistence.Table;


@Entity
// Seleccionamos el nombre de la tabla
@Table(name = "song")
 
// POJO class
public class Song {

    // Indicamos el tipo ID y le marcamos el nombre de la columna, en este caso songId. Después le marcamos el tipo de dato, en este caso **int** y el nombre de la variable id.
    @Id @Column(name = "songId") private int id;

    // Indicamos el nombre de la segunda columna **songName**. Después le marcamos el tipo de dato, en este caso **String** y el nombre de la variable songName.
    @Column(name = "songName") private String songName;
 
    // Indicamos el nombre de la tercera columna **singer**. Después le marcamos el tipo de dato, en este caso **String** y el nombre de la variable artist.
    @Column(name = "singer") private String artist;
 
    // Método con el cual devolvemos el ID
    public int getId() { return id; }
 
    // Método con el cual establecemos el ID
    public void setId(int id) { this.id = id; }
 
    // Método con el cual devolvemos el nombre de la canción
    public String getSongName() { return songName; }

    // Método con el cual establecemos el nombre de la canción 
    public void setSongName(String songName)
    {
        this.songName = songName;
    }

    // Método con el cual devolvemos el nombre del artista
    public String getArtist() { return artist; }

    // Método con el cual establecemos el nombre del artista 
    public void setArtist(String artist)
    {
        this.artist = artist;
    }
}
```

1. Los import:
   
```JAVA
import java.util.HashSet;
import java.util.List;
import java.util.Set;
import org.hibernate.Session;
import org.hibernate.SessionFactory;
import org.hibernate.cfg.Configuration;
```

1. Trabajando con las sesiones:

```JAVA
    void crearSession(){    
        Configuration configuration = new Configuration();
        configuration.configure("hibernate.cfg.xml");
        configuration.addAnnotatedClass(Song.class);
        this.sessionFactory = configuration.buildSessionFactory();
        //return sessionFactory;
    }
```

1. CRUD

Create

```JAVA
    void crearCancion(String songName, String artist) {
        try (Session session = this.sessionFactory.openSession()) {
            session.beginTransaction();

            Song nuevo = new Song();
            nuevo.setSongName(songName);
            nuevo.setArtist(artist);

            session.save(nuevo);
            session.getTransaction().commit();
            session.close();
        }
    }
```

Read

```JAVA
    void crearCancion(String songName, String artist) {
        try (Session session = this.sessionFactory.openSession()) {
            session.beginTransaction();

            Song nuevo = new Song();
            nuevo.setSongName(songName);
            nuevo.setArtist(artist);

            session.save(nuevo);
            session.getTransaction().commit();
            session.close();
        }
    }
```

Update

```JAVA
    void actualizarProducto(int id, String songName, String artist) {
        try (Session session = this.sessionFactory.openSession()) {
            session.beginTransaction();

            // Obtener el producto a actualizar
            Song cancion = session.get(Song.class, id);

            // Actualizar los campos
            if (cancion != null) {
                cancion.setSongName(songName);
                cancion.setArtist(artist);
            }

            session.getTransaction().commit();
            session.close();
        }
    }
```

Delete

```JAVA
    void eliminarProducto(int id) {
        try (Session session = this.sessionFactory.openSession()) {
            session.beginTransaction();

            // Obtener el producto a eliminar
            Song cancion = session.get(Song.class, id);

            // Eliminar el producto
            if (cancion != null) {
                session.delete(cancion);
            }
            session.getTransaction().commit();
            session.close();
        }
    }
```

Para finalizar la sesión:

```JAVA
    void cerrar(){
        this.sessionFactory.close();
    }
```

Esto es todo.