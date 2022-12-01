# Instalar-OpenLdap-ubuntu-20.04
OPENLDAP CLIENTE – SERVIDOR (LINUX)
1. Usando 2 MV de Ubuntu, una como Servidor y otra como cliente

Lo primero que tenemos que hacer es cambiar el nombre de nuestra maquina, para recordar el
nombre del servidor. Para ello nos vamos al modo grafico 

configuración → acerca de “Cambiar el nombre”


![Screenshot_3](https://user-images.githubusercontent.com/119615206/205109624-66b2dfbb-bfda-4581-bc80-e82c141dd1e8.png)

y ahora cambiaremos el archivo host de Ubuntu 

![Screenshot_4](https://user-images.githubusercontent.com/119615206/205109921-075f7d47-5e83-4a5e-b56f-4a19bfa36f4e.png)

ponemos servidorldap.asir.local servidorldap

![Screenshot_5](https://user-images.githubusercontent.com/119615206/205110094-989f4971-9429-4f82-961d-51c2a034207d.png)

el siguiente paso es poner la ip estática a nuestro servidor a traves del modo grafico

![Screenshot_6](https://user-images.githubusercontent.com/119615206/205110291-1e4c383d-d037-4ca8-a5ea-d61e389b043e.png)

el siguiente paso sera instalar los paquetes necesarios para el Openldap.

![Screenshot_7](https://user-images.githubusercontent.com/119615206/205110469-810aab50-9371-425a-86ba-1c0e682cf551.png)

Ahora nos pide que pongamos la contraseña de administración del usuario administrador del
directorio ldap. (el usuario es admin) 

![Screenshot_8](https://user-images.githubusercontent.com/119615206/205110668-7244d9a8-5c06-4778-b4d8-eadeccdef254.png)

y ya esta instalado nuestro directorio ldap y para hacer si la instalación esta bien. Pues con el
comando: sudo slapcat (nos muestra el contenido ldap)

