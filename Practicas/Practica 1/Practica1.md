# Práctica 1

Integrantes: Rubén Calvo Villazán y Marta Arenas Martínez

## Instalación en VirtualBox

Para crear la máquina, primero se le dice que sistema operativo tiene (Linux). En mi caso, he dejado los tamaños de memoria y disco que venían por defecto. 

Para instalar Ubuntu Server, una vez creada la máquina, hay que meterse en la configuración, y en  el almacenamiento, seleccionar lo siguiente: 

![](./images/meter-maquina-virtual.png)

Para cambiar las redes, nos vamos a la opción Red de la configuración, y añadimos una **red interna**, para que las máquinas puedan comunicarse entre sí, de la siguiente manera:

![](./images/aniadir-red-interna.png)

En mi caso, además de añadir la red interna, he añadido un tercer adaptador solo-anfitrión para que las máquinas puedan comunicarse con la máquina anfitriona.

Una vez añadidas las redes, podemos iniciar la máquina.

Como se dice en el pdf de la práctica, hay que instalar la máquina con LAMP (apache, mysql y php). Muestro unas capturas para que se vea que están funcionando:

![](./images/apache-funcionando.png)

![](./images/mysql-funcionando.png)

![](./images/php-funcionando.png)

Para que las máquinas puedieran verse entre sí, he tenido que poner una ip fija en cada máquina, editanto el archivo **/etc/network/interfaces**

![](./images/configuracion-red-interna.png)

La última línea del archivo es porque tuve problemas al conectar la máquina a internet, y era porque por defecto se conectaba a la red interna. Lo que hace la última línea es que la que se conecte por defecto sea la NAT, y así poder tener acceso a internet.

A ambas máquinas hay que ponerles IPs distintas.

A continuación se muestra una captura con las máquinas comunicándose entre sí:

![](./images/conexion-entre-maquinas.png)

## Instalación en VMWare

 **Creamos las dos máquinas virtuales usando VMWare**

1. Tras instalar VMWare, le damos a crear nueva máquina y seleccionamos la ISO del sistema operativo Ubuntu Server.

![](images/1.png)

2. Posteriormente creamos el usuario del sistema junto con la contraseña:

![](images/2.png)

3. Asignamos el nombre a la máquina virtual. En nuestro caso se va a llamar **UbuntuS64-bit** y **2-UbuntuS64-bit**

![](images/3.png)

4. Establecemos el espacio en disco destinado para la máquina.

![](images/4.png)

5. Confirmamos la configuración final de la máquina. Observamos que el adaptador de red se encuentra en modo NAT, de forma que recibe conexión a través del Host.

![](images/5.png)

6. Se procedería de igual manera para crear la segunda máquina virtual con Ubuntu Server:

![](images/6.png)


**Pruebas de conexión**

Realizamos la instalación del software necesario en cada máquina virtual.
Para ello ejecutamos en la terminal:

```shell
apt-get install apache2 mysql-server mysql-client openssh-server curl

```


Comprobamos la dirección IP de cada máquina. Para ello ejecutamos 

```shell
ifconfig

```

![](images/9.png)

Obtenemos la dirección **172.16.156.129**

![](images/10.png)

Obtenemos la dirección **172.16.156.128**

Si hacemos SSH de una máquina a otra:

![](images/12.png)

![](images/13.png)


Y si activamos el servidor **apache** y hacemos **curl** de una máquina a otra:

![](images/14.png)

Obtenemos el fichero html de bienvenida de apache.

![](images/15.png)
