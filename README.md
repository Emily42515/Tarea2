# Tarea-Port-Scanner-Banner-Grabber

¿QUÉ CREE?

#Con el Port Scanner - Escanea puertos del 1 al 200 en una IP objetivo para detectar cuáles están abiertos
#Con el Banner Grabber - Captura la información del servicio que corre en cada puerto abierto
Indentifiqué los servicios vulnerables y versiones de software en sistemas objetivo

#PROCESO DE ESCANEO

El script itera por cada puerto, intenta conectarse usando sockets TCP, y si tiene éxito, solicita el banner del servicio. 
Realizé esto con un timeout de 2 segundos

#COMPONENTES CLAVES DEL SCRIPT

*Configuración inicial - Utilizé la ip de '189.142.124.12' con un rando de puertos del 1-200
*Realizar la Socket Connection - Cree socket TCP con AF_INET y SOCK_STREAM para cada puerto
*Detección de puerto - Con el comando "connect_ex()", retorna a 0 si el puerto está abierto
*Captura de banner - Con el comando "recv(1024)" obtiene hasta 1KB de datos del servicio

#EJEMPLO DE SALIDA

Escaneando 127.0.0.1 de puerto 1 a 100...
--------------------------------------------------
Puerto 22: ABIERTO
Banner: SSH-2.0-OpenSSH_8.2p1
Puerto 80: ABIERTO
Banner: HTTP/1.1 200 OK
Puerto 443: ABIERTO
Banner: No disponible
--------------------------------------------------
Escaneo completado

En mi caso, al ejecutar el script con python solo apareció:




