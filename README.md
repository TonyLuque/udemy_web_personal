# Blog Personal
Proyecto basado en el curso "[Curso Practico de Django](https://www.udemy.com/course/curso-django-2-practico-desarrollo-web-python-3/)" de la plataforma udemy, en el cual se vieron los conceptos básicos de lo que es una app, creación de un modelo para la base de datos y la configuración general del proyecto en el Framework de Django.

El proyecto es un blog personal con cuatro páginas, tres estáticas y una dinámica:

**Inicio**: Descripción rápida de la persona o una portada

**About-me**: Descripción detallada de la persona

**Portfolio**: Se muestran los proyectos realizados en una estructura de titulo, descripción y enlace, estos proyectos son ingresados a través del administrador de Django

**Contacto**: Se muestran los datos de contacto o medios para contactar a la persona

En este repositorio podrás ver dos partes, la primera el Backend que está basado en el curso y el Frontend que es un diseño realizado con la ayuda de [July](https://www.behance.net/julymc).

Herramientas utilizadas:
- Django para el Backend
- SQLite para la base de datos
- Figma para la maquetación web
- HTML, CSS y JS para el Frontend
- Heroku para desplegar

Hay dos ramas en el repositorio, la rama master que tiene el proyecto como se hizo en el curso con un Frontend básico y en la rama deploy se encuentra el proyecto con el diseño propio del Frontend  y los archivos de configuración necesarios para poder hacer el despliegue en Heroku.

***
## ¿Como correr el proyecto?
- Clona el repositorio
- Genera una clave de cifrado con Django y guárdala en la variable de entorno SECRET_KEY
- Crea una variable de entorno llamada DEBUG y asígnale el valor “True” para ejecutar Django en modo desarrollo o asígnale un string vacio “” para que se ejecute en modo producción
- Borra el archivo llamado “db.sqlite3” si existe
- Ejecuta el comando '$ python manage makemigrations ' y luego ' $ python manage mígrate ' para crear la base de datos
- Crear el super usuario para poder acceder al panel del administrador ' $ python manage.py createsuperuser ' , este comando te pedirá nombre, email, contraseña y confirmación de la contraseña
- Ya puedes ejecutar el proyecto con ' $ python manage.py runserver '.
***
## ¿Cómo se hizo?
Primero se desarrollo la estructura del Backend creando una app núcleo en la que vivieran las páginas estáticas y una app por aparte en la que se implementara la lógica de la creación de los proyectos para guardar en la base de datos. En paralelo se implementaba la integración del Frontend (solo la estructura básica) con la estructura de Templates de Django para poder ver el resultado y verificar si todo iba como se esperaba.

Ya terminado el Backend se procedió al diseño del Frontend en la herramienta de Figma, escogiendo colores, espaciados, márgenes, tipografías y todo lo necesario para realizar el Diseño Web.

Terminada la fase de diseño se procedió a la implementación en HTML, CSS y JS usando el patrón de diseño Mobile First, para hacer más fácil la codificación responsiva del diseño.

El despliegue se realizo a través del servicio de Heroku