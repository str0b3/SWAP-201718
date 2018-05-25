# Ejercicios Tema 6

### Rubén Calvo Villazán

## Ejercicio 1 y 2
Realizado en prácticas con **iptables**

## Ejercicio 3
**Buscar información acerca de los tipos de ataques más comunes en servidores web (p.ej. secuestros de sesión). Detallar en qué consisten, y cómo se pueden evitar.**

* **Injección de código:** Puede ser SQL, JavaScript, etc. Su fin es el de revelar información sobre el servicio o ejecutar código arbirario. Se evita con una correcta configuración y programación del servicio web

* **DDoS:**  Este ataque trata de bloquear el acceso a un sitio web saturando sus recursos a base de peticiones, de forma que el contenido sea inaccesible. Se puede evitar con servidores de respaldo o contratando empresas que se encarguen de soportar la carga, como *CloudFlare*.

* **Secuestros de sesión:** Robo de credenciales por fuerza bruta, robo de cookies del navegador, ingeniería social, etc.
