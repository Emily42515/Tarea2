# Tarea-Port-Scanner-Banner-Grabber

¿QUÉ CREE?

#Con el Port Scanner - Escanea puertos del 1 al 200 en una IP objetivo para detectar cuáles están abiertos
#Con el Banner Grabber - Captura la información del servicio que corre en cada puerto abierto
Indentifiqué los servicios vulnerables y versiones de software en sistemas objetivo

#PROCESO DE ESCANEO

El script itera por cada puerto, intenta conectarse usando sockets TCP, y si tiene éxito, solicita el banner del servicio. 
Realizé esto con un timeout de 2 segundos

#COMPONENTES CLAVES DEL SCRIPT

*Configuración inicial - Utilizé la ip de 
