# Práctica 2

## Crear un tar con ficheros locales en un equipo remoto

![](capturas/9.png)

## Sincronizar directorios con rsync

1. Ejecutamos el comando:

```shell
sudo chown -R usuario:usuario /var/www/

```
Para cambiar el propietario del directorio /var/www/ de **root** a **usuario**.

![](capturas/1.png)

2. Tras realizar la instalación de rsync en ambas máquinas, ejecutamos el comando:

```shell
rsync -avz -e ssh 172.16.156.128:/var/www/ /var/www/

```

En el server 2 para vincularlo con el server 1.

![](capturas/2.png)

3. Si en el server 1 creamos un fichero en /var/www/

![](capturas/3.png)

Al ejecutar el comando anterior en el server 2, vemos que aparece el fichero creado en el directorio:

![](capturas/4.png)


## SSH sin contraseña

1. Ejecutamos el comando 

```shell
ssh-keygen -b 4096 -t rsa
```
y seguimos las indicaciones para crear un par de claves **pública** y **privada**.

2. Exportamos la clave pública de una máquina a la otra para añadirla a los dispositivos de confianza.

```shell
ssh-copy-id usuario@172.16.156.128
```

Si no queremos especificar la IP de la máquina cada vez que nos queramos conectar por ssh, podemos establecerle un **alias** editando el fichero **/etc/hosts**

![](capturas/6.png)

![](capturas/7.png)

De forma que para conectarse, bastaría con hacer:

```shell
ssh server1
```

```shell
ssh server2
```

## Programar la tarea rsync

Si queremos que la tarea rsync se ejecute una vez cada hora, deberemos indicarle un minuto cualquiera (por ejemplo el minuto 0), de todas las horas, todos los días, cualquier día de la semana, etc.

![](capturas/7.png)



