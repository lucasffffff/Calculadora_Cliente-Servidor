##Proyecto Cliente-Servidor en Java
Este proyecto demuestra una simple aplicación de cliente-servidor en Java, donde el servidor realiza operaciones matemáticas simples (suma, resta, multiplicación, división) solicitadas por el cliente. A continuación, se describe cómo configurar y ejecutar ambos componentes en máquinas virtuales dentro de una red interna.

###Configuración del Entorno
Para ejecutar este proyecto, necesitarás dos máquinas virtuales (VM) configuradas para comunicarse en una red interna. Asegúrate de que ambas VM estén configuradas para usar el mismo adaptador de red interno en tu software de virtualización (por ejemplo, VirtualBox o VMware).

###Requisitos
Java Development Kit (JDK) instalado en ambas máquinas virtuales.
Acceso a la terminal o línea de comandos en ambas máquinas.
Conocer la dirección IP de la máquina virtual del servidor dentro de la red interna.
###Ejecución del Servidor
En la VM del servidor, navega hasta la carpeta del proyecto que contiene el código del servidor.
Compila el código del servidor ejecutando javac servidor/Servidor.java.
Inicia el servidor con java servidor.Servidor.
El servidor comenzará a escuchar conexiones en el puerto especificado (por defecto, 3555).
###Ejecución del Cliente
En la VM del cliente, asegúrate de tener la dirección IP del servidor.
Navega hasta la carpeta del proyecto que contiene el código del cliente.
Edita el archivo cliente/Cliente.java, reemplazando la dirección IP del servidor (SERVER_ADDRESS) con la dirección IP de la máquina virtual del servidor.
Compila el código del cliente ejecutando javac cliente/Cliente.java.
Inicia el cliente con java cliente.Cliente.
Una ventana emergente solicitará que ingreses la operación matemática a realizar. Introduce tu operación y presiona Enter.
###Flujo de Trabajo
Una vez iniciados, el cliente y el servidor se comunicarán a través de la red interna. El cliente enviará solicitudes de operaciones matemáticas al servidor, que procesará estas operaciones y devolverá los resultados al cliente. Este flujo continuará hasta que el usuario decida cerrar la aplicación cliente.

###Troubleshooting
Asegúrate de que la dirección IP y el puerto en el código del cliente coincidan con la dirección IP de la VM del servidor y el puerto en el que está escuchando.
Verifica que las VM estén configuradas en la misma red interna y que el firewall o cualquier otro software de seguridad no esté bloqueando la comunicación.
Si encuentras problemas de conexión, revisa la configuración de red de tus máquinas virtuales y asegúrate de que ambas pueden alcanzarse entre sí.
