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


![Screenshot_10](https://user-images.githubusercontent.com/119615206/205111790-7b2cbc18-652a-4e2a-8883-aadf6ba90796.png)

siguiente paso sera configurar otros parametros del Openldap. Para ello ejecutamos el comando:
sudo dpkg-reconfigure slapd

![Screenshot_11](https://user-images.githubusercontent.com/119615206/205112009-e857dd74-4ca7-47a8-997a-198094188df0.png)

Ahora vamos a completar este ultimo paso.

![Screenshot_12](https://user-images.githubusercontent.com/119615206/205112120-62ff9753-6f52-4280-aef1-13d46d0cb4c5.png)

Nuestro dominio

![Screenshot_13](https://user-images.githubusercontent.com/119615206/205112309-cbec0446-9b75-4bd9-883a-3cc1c127c0d4.png)

![Screenshot_14](https://user-images.githubusercontent.com/119615206/205112467-2b1597f9-9d0b-412b-8beb-d81714b2f3d9.png)

ahora nos pide la contraseña administrador esta contraseña si es la que vale la anterior era para la
preconfiguración inicial 

![Screenshot_15](https://user-images.githubusercontent.com/119615206/205112554-a6d8c3a4-6646-4f4c-9eb4-97caff69d99f.png)


![Screenshot_16](https://user-images.githubusercontent.com/119615206/205112715-ae59b565-0778-41f8-850a-0e44c1698418.png)


aquí le damos que si aunque no va afectar en nada

![Screenshot_17](https://user-images.githubusercontent.com/119615206/205112814-e0ad800c-172a-4936-8148-fbdd71626f76.png)

y ya tendríamos instalado nuestro directorio ldap 

![Screenshot_18](https://user-images.githubusercontent.com/119615206/205112893-08239326-9b3a-4249-b64c-769dd2d6c006.png)

![Screenshot_19](https://user-images.githubusercontent.com/119615206/205113028-27ac7ceb-8786-4482-bbe1-3b71cf88cead.png)

ahora vamos a instalar

![Screenshot_20](https://user-images.githubusercontent.com/119615206/205113104-4a72f005-864c-4bbc-9977-abacdfced9d4.png)

ahora en nuestro navegador ponemos localhost/lam

![Screenshot_21](https://user-images.githubusercontent.com/119615206/205113214-fae1d105-c710-470f-ac87-61a2fab7b0cc.png)

en LAM configuration

![Screenshot_22](https://user-images.githubusercontent.com/119615206/205113309-9a24f6ab-3998-419f-b891-e4c4e327e854.png)

vemos dos opciones , seleccionamos la primera

![Screenshot_23](https://user-images.githubusercontent.com/119615206/205113381-4e893eb9-2c9f-4e06-9823-a715c668b628.png)

cuando entramos nos pide la contraseña maestra que de forma determinada es lam.

![Screenshot_24](https://user-images.githubusercontent.com/119615206/205113512-3e918ca3-7dec-4b6e-852a-5b14a0a23148.png)

Ponemos una contraseña nuevo para estar más seguros

![Screenshot_25](https://user-images.githubusercontent.com/119615206/205113608-d09fe0bc-3343-408b-b4b2-41e934ae1073.png)

volvemos a entrar en LAM configuration

![Screenshot_26](https://user-images.githubusercontent.com/119615206/205113690-9bbd889f-e84c-4b10-af87-3149ed394d2a.png)

y en Edit server profiles

![Screenshot_27](https://user-images.githubusercontent.com/119615206/205113763-c146cf7e-29e8-4368-abb2-9e21de1817cb.png)

ponemos la contraseña

![Screenshot_28](https://user-images.githubusercontent.com/119615206/205113851-efabf902-3deb-4b5c-9bf3-44fc8ea51cb8.png)

y en Tree suffix ponemos dc=asir,dc=local

![Screenshot_29](https://user-images.githubusercontent.com/119615206/205113918-b57a242e-c4aa-4566-8536-989767ccb865.png)

y el idioma

![Screenshot_30](https://user-images.githubusercontent.com/119615206/205113994-4391495b-129d-4bf1-bd3f-f7f252ac0be0.png)

en seguridad poner cn=admin,dc=asir,dc=local

![Screenshot_31](https://user-images.githubusercontent.com/119615206/205114070-4e1bbce3-22cc-4dc3-9eba-f099d4159287.png)

y ponemos los usuarios y los grupos

![Screenshot_32](https://user-images.githubusercontent.com/119615206/205114139-f7cd58ef-0d98-4ee2-9946-74afbe76244d.png)

y añadir hosts

![Screenshot_33](https://user-images.githubusercontent.com/119615206/205114211-77caa6f8-c56b-4dab-adb4-8f53045dfeb6.png)

poner equipos

![Screenshot_34](https://user-images.githubusercontent.com/119615206/205114272-50a715d3-e603-45ce-bda9-5ef1450b405a.png)

anadir unix y account

![Screenshot_35](https://user-images.githubusercontent.com/119615206/205114333-c1c97d4e-8565-48d3-95cb-5299405a3f46.png)

entramos a hora si como admin y la contraseña que anteriormente cambiamos

![Screenshot_36](https://user-images.githubusercontent.com/119615206/205114426-6394c8cd-4392-46a1-945e-6a1123f619bb.png)

y ya tenemos la configuración

![Screenshot_37](https://user-images.githubusercontent.com/119615206/205114500-997d1a57-1817-4d49-893f-8452c413c820.png)

luego lo creamos

![Screenshot_38](https://user-images.githubusercontent.com/119615206/205114556-a85f6c34-2093-4a7b-abbd-2ac454809186.png)

y creamos los usuarios y grupos

![Screenshot_39](https://user-images.githubusercontent.com/119615206/205114650-bd5b3bc2-8d97-4ff8-ad79-fb9204c2a3ac.png)

grupo → nuevo grupo

![Screenshot_40](https://user-images.githubusercontent.com/119615206/205114728-e8db9472-a75b-49c2-80b7-41be94d313e3.png)

profesores

![Screenshot_41](https://user-images.githubusercontent.com/119615206/205114811-a34f209d-2900-46be-b4d7-6d11e3b88fb3.png)

Alumnos

![Screenshot_42](https://user-images.githubusercontent.com/119615206/205114870-037c85d5-c4f9-459e-aa81-742aed553b55.png)

y ya los vemos

![Screenshot_43](https://user-images.githubusercontent.com/119615206/205114970-2d32dd22-1183-4e99-9877-be36953c24d7.png)

y ahora creamos los usuarios

![Screenshot_44](https://user-images.githubusercontent.com/119615206/205115128-b1b4780c-30d0-46a3-8032-4f737b075738.png)

profesor01 y alumno01

![Screenshot_45](https://user-images.githubusercontent.com/119615206/205115194-714d6bb7-5295-4927-92e9-b75eea988c8c.png)

establecemos una contraseña

![Screenshot_46](https://user-images.githubusercontent.com/119615206/205115259-14e5aa37-d6bf-4ed0-b238-db00b5e0b207.png)

y ponemos la contraseña

![Screenshot_47](https://user-images.githubusercontent.com/119615206/205115313-14a32903-3fbe-4754-9e57-6e9b4e270f53.png)

y ya se creo el usuario

![Screenshot_48](https://user-images.githubusercontent.com/119615206/205115378-b90c88e3-bf7b-490f-9fd8-35256ec6eca3.png)

![Screenshot_49](https://user-images.githubusercontent.com/119615206/205115519-b263bdec-414c-4e2d-92ee-24c6b2a7b777.png)

b. Instala y configura el cliente Ldap en una máquina de Ubuntu

Lo primero que tenemos que hacer es verificar de el servidor y el cliente tiene conexión, mediante
un ping

![Screenshot_50](https://user-images.githubusercontent.com/119615206/205115666-ba70dd09-0cb8-4f10-960d-62eaebca855f.png)

lo siguiente es instalar tres paquetes 

![Screenshot_51](https://user-images.githubusercontent.com/119615206/205115755-6361697e-5939-485b-aca3-ba152dd73abe.png)

ahora vamos a configurar el cliente

![Screenshot_52](https://user-images.githubusercontent.com/119615206/205115850-1627f6f3-add9-4c37-a444-d55343f21550.png)

lo siguiente es el dominio 

![Screenshot_53](https://user-images.githubusercontent.com/119615206/205115920-cfc5bbc5-24a0-47ac-9dac-3668d5b2ee22.png)

lo siguiente que nos pide es la versión del ldap 

![Screenshot_54](https://user-images.githubusercontent.com/119615206/205115993-6e1f442f-7bd5-4392-9584-583d184aa4eb.png)

esta pregunta la dejamos por defecto.

![Screenshot_55](https://user-images.githubusercontent.com/119615206/205116041-1404487c-52b6-4295-97aa-d034da46ee94.png)

![Screenshot_56](https://user-images.githubusercontent.com/119615206/205116079-7a836093-28c7-4d69-8f47-09521d06bfb8.png)

Y lo ultimo que nos pide es cual es el administrador del ldap

![Screenshot_57](https://user-images.githubusercontent.com/119615206/205116132-1b58f430-61d2-4dee-b97e-450ac013dd3e.png)

y lo ultimo la contraseña

![Screenshot_58](https://user-images.githubusercontent.com/119615206/205116205-ba5d36a1-195c-4735-9117-a3718daa93a0.png)

y una ves finalizado, solo queda por configurar 3 archivos:

1º Archivo
editamos el nsswitch.conf

![Screenshot_59](https://user-images.githubusercontent.com/119615206/205116295-db7c51ba-3c01-460a-ab50-0fa548e4e4b4.png)

ahora con sudo gedit nsswitch.conf lo editamos

![Screenshot_60](https://user-images.githubusercontent.com/119615206/205116374-3f8a5e54-1087-42b6-9672-746d00dbf435.png)

![Screenshot_61](https://user-images.githubusercontent.com/119615206/205116440-3ca3cfd5-afab-4edc-8e60-9c80fac415de.png)

2º Fichero

![Screenshot_62](https://user-images.githubusercontent.com/119615206/205116497-965bd62a-1527-4aa3-8dcf-dac1199c60aa.png)

quitar este apartado

![Screenshot_63](https://user-images.githubusercontent.com/119615206/205116609-531249d8-2e40-4790-a435-a8724da3db77.png)

![Screenshot_64](https://user-images.githubusercontent.com/119615206/205116680-95370a02-2381-4392-8134-706e526a5ebd.png)

3º y ultimo fichero

![Screenshot_65](https://user-images.githubusercontent.com/119615206/205116747-7a62dd01-650c-4ee3-9e3c-6ce5cbe9c1d3.png)

![Screenshot_66](https://user-images.githubusercontent.com/119615206/205116817-3ed1c930-5b0c-4d1e-8057-eee1d592c7e9.png)

y ahora solo nos queda saber si nuestra ldap es correcta.

![Screenshot_67](https://user-images.githubusercontent.com/119615206/205116905-07c00077-358d-480e-b6af-3a76b26990aa.png)

Ahora reiniciamos

![Screenshot_68](https://user-images.githubusercontent.com/119615206/205116952-5f7cb507-e4f3-49af-8bf3-f972ea6150ad.png)

una ves reiniciado vamos a intentar logearnos mediante terminal

mediante ctrl+alt+f2

![Screenshot_69](https://user-images.githubusercontent.com/119615206/205117048-168b6e37-29b5-4e4b-9772-659f619a72ad.png)

probamos con profesor01 que es el usuario creado anteriormente

![Screenshot_70](https://user-images.githubusercontent.com/119615206/205117129-17f7a7db-a418-442d-b523-e4666357e352.png)

y como se puede ver ya estamos dentro con el usuario donde también se a creado un directorio para
ese usuario.

![Screenshot_71](https://user-images.githubusercontent.com/119615206/205117201-7c19099b-1b5d-4d05-863e-781e27632d65.png)

Ahora instalamos el ultimo paquete

![Screenshot_72](https://user-images.githubusercontent.com/119615206/205117249-a5b9d077-5211-423a-ba17-8ed3904603d1.png)

![Screenshot_73](https://user-images.githubusercontent.com/119615206/205117289-0defddbc-7b7d-455b-9353-2436de085227.png)

![Screenshot_73](https://user-images.githubusercontent.com/119615206/205117366-87804bb9-a287-4831-8958-7fe0457288be.png)

una ves instalado, toca otra vez reiniciar el cliente y comprobar de que funcione.

Y ahora probamos el usuario

![Screenshot_74](https://user-images.githubusercontent.com/119615206/205117483-c9339a80-6e7a-4f2b-8222-fafa3a7032c8.png)

y ya podemos usar cualquier usuario de servidor ldap

![Screenshot_75](https://user-images.githubusercontent.com/119615206/205117545-6a76240f-4e70-4913-a6b9-b17634a1b534.png)

WINDOWS pGine

2. Descarga el programa pgina de http://pgina.org/. Este software permite usar la máquina
Windows, referenciada a una base de datos LDAP como OpenLdap.

Para poder usar una máquina Windows como cliente del LDAP, tendremos que instalar un software
intermedio, llamado pGina.

Cuando lo estemos instalado es posible que se instalen algunas dependencias MS Visual C++

![Screenshot_76](https://user-images.githubusercontent.com/119615206/205117740-250e52ca-b7a8-49ca-91de-7d9d4b89c0f2.png)

![Screenshot_77](https://user-images.githubusercontent.com/119615206/205117781-0d3d15b4-69bf-45f8-9191-715acac425ae.png)


![Screenshot_78](https://user-images.githubusercontent.com/119615206/205117844-1a650e84-af5c-46d3-aa7e-b19c9995d8ae.png)

muchas fotos despues ... 

ahora para configurar el cliente windows lo primero es ir a la pestaña plugin selection activamos las
3 casillas del ldap y hacemos clic en configure

![Screenshot_79](https://user-images.githubusercontent.com/119615206/205117974-ada427f5-9c10-412b-8bb6-ba3b27da92fc.png)

![Screenshot_80](https://user-images.githubusercontent.com/119615206/205118033-cd6dcb1b-3cf3-41a8-8f60-0a5b90d98ff1.png)

En la pestaña plugin order priorizaremos para que la búsqueda para las autenticaciones sea primero
en la LDAP

![Screenshot_81](https://user-images.githubusercontent.com/119615206/205118124-690fa8de-06f9-4240-858d-b4508b162be2.png)

En la pestaña simulation probaremos a introducir unos datos para probar que la búsqueda en la
LDAP es correcta

![Screenshot_82](https://user-images.githubusercontent.com/119615206/205118190-c902d5b6-72e9-47a6-9335-6cbe087a602e.png)

![Screenshot_83](https://user-images.githubusercontent.com/119615206/205118262-12059e92-0201-4423-9f7e-f36092c49552.png)

y ya tenemos usuario del LDAP en windows

![Screenshot_84](https://user-images.githubusercontent.com/119615206/205118337-140533ac-5069-4321-9f84-ff97107188be.png)
