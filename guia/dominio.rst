Creación de Dominio OSB en Cluster
========

- Requisitos:
1. Tener un java instalado que sea compatible con la versión de rcu a Instalar.
2. Verificar que el entorno de las ventanas X esté operativo.
3. Tener instalado Oracle fusion Middleware y Oracle SOA Suite.
4. Tener instalado un repositorio de metadata.


- Ejecutamos el script config.sh dentro de la ruta de instalación y lo primero que nos mostrará será la pantalla a donde indicaremos que deseamos crear un dominio y la ruta de instalación del dominio:


.. image:: ../imagenes/dominio/Captura1.PNG


- Seleccionamos las plantillas a utilizar requeridas para el dominio OSB:


.. image:: ../imagenes/dominio/Captura2.PNG


.. image:: ../imagenes/dominio/Captura3-1.PNG


.. image:: ../imagenes/dominio/Captura3-2.PNG


- Dejamos las opciones de alta disponibilidad por defecto.


.. image:: ../imagenes/dominio/Captura4.PNG


- Indicamos la ruta de instalación de las aplicaciones:


.. image:: ../imagenes/dominio/Captura5.PNG


- Ingresamos el usuario y contraseña de la consola administrativa:


.. image:: ../imagenes/dominio/Captura6.PNG


- Indicamos el modo en que será creado el dominio, en este caso modo producción:


.. image:: ../imagenes/dominio/Captura7.PNG


- Ingresamos las credenciales para que se conecte al repositorio de metadata (en schema owner siempre se debe colocar "prefijo"_stb). Luego la prueba de conexión debe ser satisfactoria:


.. image:: ../imagenes/dominio/Captura8.PNG


- Nos muestra los componentes a utilizar:


.. image:: ../imagenes/dominio/Captura9.PNG


- Realizará un test jdbc por cada componente:


.. image:: ../imagenes/dominio/Captura10.PNG


- La configuración de Keystore se deja por defecto:


.. image:: ../imagenes/dominio/Captura11.PNG


- En configuración avanzada debemos seleccionar los mostrados en la imagen para la configuración de un cluster. File store se tildará solo si es requerido, que en nuestro caso sí:


.. image:: ../imagenes/dominio/Captura12.PNG


- Ingresamos los parámetros del Admin Server:


.. image:: ../imagenes/dominio/Captura13.PNG


- Se asignan las credenciales del nodo manager, que es el que no permitirá poder administrar los manejados a través de la consola administrativa:


.. image:: ../imagenes/dominio/Captura14.PNG


- Se agregan los servidores manejados con su ip y puerto de escucha. Si estarán en un mismo servidor deben tener los puertos de escucha diferentes para evitar conflictos. Todos los manejados deben pertenecer al mismo "Server Groups", para por ejemplo poder asignarle la memoria java al grupo y todos la tomarán:


.. image:: ../imagenes/dominio/Captura15.PNG


- Se indica el nombre del cluster:


.. image:: ../imagenes/dominio/Captura16.PNG


- Los Server Templates se deja por defecto:


.. image:: ../imagenes/dominio/Captura17.PNG


- Igualmente los Dynamic Servers:


.. image:: ../imagenes/dominio/Captura18.PNG


- Se agregan los servidores manejados al cluster:


.. image:: ../imagenes/dominio/Captura19.PNG


- La configuración "Coherence Clusters" se deja por defecto:


.. image:: ../imagenes/dominio/Captura20.PNG


- Creamos una máquina (machine) por cada servidor fisico o virtual existente en el cluster e indicamos su puerto de escucha:


.. image:: ../imagenes/dominio/Captura21.PNG


- Asigamos los servidores manejados a la maquina que corresponda. El Admin Server no es necesario asignarlo a una máquina ya que no posee servidores manejados. Sin embargo, se asignó ya que en este caso estamos realizando una migración de versión y en la instalación pasada lo realizaron, y se busca que la nueva instalación este lo mas similar posible:


.. image:: ../imagenes/dominio/Captura22.PNG


- No se asignan Destinos Virtuales:


.. image:: ../imagenes/dominio/Captura23.PNG


- No se agregan particiones:


.. image:: ../imagenes/dominio/Captura24.PNG


- En los despliegues de destino se agrega "wsm-pm" al Admin Server:


.. image:: ../imagenes/dominio/Captura25.PNG


- Se dejan los Servicios de destino sin modificaciones:


.. image:: ../imagenes/dominio/Captura26.PNG


- Se configuran los File Stores:


.. image:: ../imagenes/dominio/Captura27.PNG


- Nos muestra el resumen de la instalación:


.. image:: ../imagenes/dominio/Captura28.PNG


- Esperamos que el progreso de la instalación llegue al 100 %:


.. image:: ../imagenes/dominio/Captura29.PNG


- Finalmente nos mostrará un mensaje que el dominio fue creado satisfactoriamente:


.. image:: ../imagenes/dominio/Captura30.png
