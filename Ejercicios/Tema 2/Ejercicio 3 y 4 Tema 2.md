
# Ejercicios 3 y 4 Tema 2

### Rubén Calvo Villazán

## Ejercicio 3
**¿Cómo analizar el nivel de carga de cada uno de los subsistemas en el servidor?**

Encontramos varios comandos en las distribuciones Linux para este fin:

* **top:** Vista previa de todos los procesos ejecutándose en el sistema (con sus variantes **htop** y **atop**)
* **apachetop:** Como **top** pero dedicado al servidor Apache
* **traceroute:** Para comprobar la latencia entre dispositivos de la red
* **netstat:** Buscar problemas en una red
* **ss:** Como netstat pero más rápido y completo
* **nmap:** Se usa para escanear una red y buscar dispositivos, puertos abiertos, etc.
* **tcpdump:** Imprime el tráfico en la red pudiendo filtrar los paquetes por expresiones en la línea de comandos.
* **df:** Abreviatura de Disk Free, muestra estadísticas del disco.
* **vmstat:** Muestra estadísticas sobre la memoria de la máquina.
* **mpstat:** Muestra la carga de la CPU.
* **ps:** Listado de procesos en ejecución junto con su PID.

Para más herramientas: https://blog.serverdensity.com/80-linux-monitoring-tools-know/

## Ejercicio 4
**Buscar ejemplos de balanceadores software y hardware (productos comerciales).**

* Balanceadores de carga software encontramos **Nginx** (Balanceador de carga de peticiones http https://nginx.org/)
o **Pound** (http://www.apsis.ch/pound) para distribuir peticiones http entre servidores especialmente los que no tienen la seguridad SSL 
implementada 

* En los balanceadores hardware tenemos **Barracuda**, de instalación rápida y con alto rendimiento (https://www.barracuda.com/solutions/physical). Además encontramos las soluciones posibles de la empresa **Kemptechnologies** (https://kemptechnologies.com/)

**Buscar productos comerciales para servidores de aplicaciones.**
* Oracle Application Server (http://www.oracle.com/technetwork/es/middleware/ias/overview/index.html)
* Apache (https://www.apache.org/)
* Windows Server (https://www.microsoft.com/es-es/cloud-platform/windows-server)

**Buscar productos comerciales para servidores de almacenamiento.**
Entre los servidores de almacenamiento comerciales tenemos:

* Microsoft Azure: (https://azure.microsoft.com/es-es/)
* Amazon Web Services: (https://aws.amazon.com/es/)
* Rackspace: (https://www.rackspace.com/es)
* Google Cloud: (https://cloud.google.com/?hl=es)



