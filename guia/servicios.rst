Exportar e Importar Servicios.
=======


En nuestro caso se está migrando de Oracle Service Bus, de la versión 11g a 12c, por lo que debemos exportar los servicios del Bus de 11g e importarlos en 12c. Estas migraciones deben ser consultadas con el área de desarrollo de sotfware, ya que al cambiar el java, hay cambios de librerias que pueden afectar el funcionamiento de la aplicación en el nuevo entorno.

- Ingresamos a la consola administrativa del bus de 11g: 


.. image:: ../imagenes/servicios/14-03-201916-10-19.png


- Seleccionamos la pestaña Administración del Sistema:  


.. image:: ../imagenes/servicios/14-03-201916-10-49.png


- Le damos a la opción Exportar Recursos:


.. image:: ../imagenes/servicios/14-03-201916-12-06.png


- Seleccionamos el proyecto y luego la opción Exportar:


.. image:: ../imagenes/servicios/14-03-201916-12-34.png


- Luego elegimos si queremos proteger los datos con una contraseña o no, y seleccionamos Terminar Exportación:


.. image:: ../imagenes/servicios/14-03-201916-13-02.png


- Luego el sistema operativo nos mostrará un mensaje que la descarga a sido completada:


.. image:: ../imagenes/servicios/14-03-201916-14-00.png


- Seguidamente ingresamos a la consola del bus de 12c:


.. image:: ../imagenes/servicios/14-03-201916-16-04.png


- Seleccionamos el botón crear:


.. image:: ../imagenes/servicios/14-03-201916-21-56.png


- Luego le damos al ícono de la flecha hacia abajo:


.. image:: ../imagenes/servicios/14-03-201916-23-09.png


- Seleccionamos el archivo de la ubicación local que la tengamos:


.. image:: ../imagenes/servicios/14-03-201916-23-31.png


.. image:: ../imagenes/servicios/14-03-201916-24-05.png


- Dejamos la configuración avanzada por defecto y le damos a la opción Importar:


.. image:: ../imagenes/servicios/14-03-201916-24-38.png


- Te mostrará los detalles de la importación y la severidad en caso de presentarse algún problema. En nuestro caso nos arrojó aproximadamente la mitad de los recursos con mensajes de diagnostico:


.. image:: ../imagenes/servicios/14-03-201916-27-06.png


- Finalmente al desplegar la carpeta del proyecto, se puede observar todo su contenido:


.. image:: ../imagenes/servicios/14-03-201916-27-56.png


Cabe destacar, que en esta migración los servicios quedaron funcionando de manera satisfactoria en el nuevo Oracle Service Bus 12c, en um ambiente de producción.
