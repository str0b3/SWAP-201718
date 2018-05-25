# Ejercicios 1 y 2 Tema 

### Rubén Calvo Villazán

## Ejercicio 1

**Buscar con qué órdenes de terminal o herramientas gráficas podemos configurar bajo Windows y bajo Linux el enrutamiento del tráfico de un servidor para pasar el tráfico desde una subred a otra.**

En **Windows** se realizaría con el asistente de Windows, en *Panel de Control > Propiedades de la red.*
También se podría realizar por línea de comandos con el comando **route**.

En **Linux** el comando es similar al de Windows, si deseamos configurar una nueva gateway escribiríamos: route add default gw ...


## Ejercicio 2
**Buscar con qué órdenes de terminal o herramientas gráficas podemos configurar bajo Windows y bajo Linux el filtrado y bloqueo de paquetes.**

En **Windows**: Se realizaría en el *Panel de Control*, buscar las opciones del *Firewall* y aparece toda la configuración.
En **Linux**: Se realiza con el comando **iptables**