Propagación del Dominio a Otras Máquinas
========


Cuando tenemos un dominio con servidores manejados en servidores físicos o virtuales diferentes, se debe propagar el dominio a tantos servidores estén involucrados.


- Primero empaquetamos el dominio con el ejecutable pack en el servidor a donde se creó dicho dominio como se muestra en la imagen:


.. image:: ../imagenes/propagacion/14-03-201912-44-55.png


- Luego desempaquetamos el dominio en las otrás máquinas o servidores con el comando unpack de la siguiente manera:


.. image:: ../imagenes/propagacion/14-03-201912-47-39.png


- Luego ejecutamos el Weblogic Scripting Tool (wlst) en la máquina a donde desempaquetamos el dominio, y nos conectamos al Admin Server con las respectivas credenciales y url de la siguiente manera:


.. image:: ../imagenes/propagacion/14-03-201912-49-38.png


- Procedemos a enrrolar el node manager de la máquina con el Admin Server para que pueda ser gestionado desde la consola administrativa como se muestra en la imagen:


.. image:: ../imagenes/propagacion/14-03-201912-50-08.png


- Luego iniciamos el node manager de esa máquina:


.. image:: ../imagenes/propagacion/14-03-201912-51-06.png


- Si chequeamos el estado del gestor de nodos de esta máquina, debe estar Accesible:


.. image:: ../imagenes/propagacion/14-03-201912-51-56.png


- Esto quiere decir que ya podemos administrar los servidores manejados de esta máquina a través de la consola administrativa (Admin Server):


.. image:: ../imagenes/propagacion/14-03-201912-53-59.png