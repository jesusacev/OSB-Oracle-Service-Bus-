Creación de Repositorio de Metadata
========

- Requisitos:
1. Tener un java instalado que sea compatible con la versión de rcu a Instalar.
2. Verificar que el entorno de las ventanas X esté operativo.
3. Tener instalado Oracle fusion Middleware y Oracle SOA Suite.


Esta creación de repositorio se debe realizar por cada dominio OSB que se vaya a crear


- Ejecutamos el utilitario rcu, ubicado dentro del directorio de instalación de oracle y seguidamente nos mostrará la pantalla de bienvenida de la instalación:


.. image:: ../imagenes/metadata/Captura1.PNG


- Indicamos que deseamos crear un repositorio:


.. image:: ../imagenes/metadata/Captura2.PNG


- Ingresamos los parámetros de conexión a la base de datos. La conexión se debe realizar con un usuario que tenga rol de sysdba, en este caso sys:


.. image:: ../imagenes/metadata/Captura3.PNG


- Si la conexión es satisfactoria nos mostrará esta ventana:


.. image:: ../imagenes/metadata/Captura4.PNG


- Indicamos el nombre del prefijo y los componentes a crear que en nuestro caso son estos:


.. image:: ../imagenes/metadata/Captura5.PNG


- Se chequean los pre-requisitos para la creación de cada componente:


.. image:: ../imagenes/metadata/Captura6.PNG


- Se debe ingresar el password de los schema users:


.. image:: ../imagenes/metadata/Captura7.PNG


- Se personalizan las variables del componente SOA Infraestructure:


.. image:: ../imagenes/metadata/Captura8.PNG


- Se dejan los tablespaces que se crearán por defecto:


.. image:: ../imagenes/metadata/Captura9.PNG


- Seleccionamos ok para que se proceda a crear los tablespaces:


.. image:: ../imagenes/metadata/Captura10.PNG


- Si los tablespaces fueron creados satisfactoriamente, nos mostrará esta ventana de la siguiente manera:


.. image:: ../imagenes/metadata/Captura11.PNG


- Nos mostrará el resumen para la creación de los componentes:


.. image:: ../imagenes/metadata/Captura12.PNG


.. image:: ../imagenes/metadata/Captura13.PNG


- Una vez completada la instalación, todos los componentes deben mostrar estatus "Success":


.. image:: ../imagenes/metadata/Captura14.PNG
