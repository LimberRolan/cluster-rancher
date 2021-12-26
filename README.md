# Reconocimiento de Billetes por medio de I.A.
## Resumen
<p align="justify">
En el presente proyecto se realizó el diseño y fabricación de un 
cluster de raspberry PIs, el El Cluster  se puede utilizar para ejecutar aplicaciones distribuidas en un clúster real con el fin trabajar, aprender y experimentar con Docker y Docker Clustering aprender sobre redes, equilibrio de carga y alta disponibilidad
    ... ¡y mucho más!
</p>

# Hypriot Cluster 
Un conjunto de roles para configurar e inicializar un clúster de Kubernetes en un grupo de Raspberry Pis que ejecutan HypriotOS. Aquí hay dos componentes principales. En primer lugar, estamos iniciando los nodos utilizando un script de inicio  y preparándolos para el servicio. Este paso puede implicar cambiar las direcciones IP de los nodos y fallará después de ejecutar . Para evitarlo, utilice las direcciones IP asignadas por DHCP o SSH y configúrelas como static_host_ip. La segunda parte implica el uso de kubernetes para iniciar un nuevo clúster y luego unirse a los nodos trabajadores.


<br>
| <a href="https://agetic.gob.bo">AGETIC</a>
| <a href="https://www.youtube.com/c/AgeticBolivia">YouTube</a>
| <a href="https://twitter.com/AgeticBolivia">Twitter</a>
|  
<br>


## Requisitos

* Requisitos para el desarrollo de software:
    * Sistemas Operarivos:
        * hypriotOS.
        * linux debian
    * formaterSSDcard
    * advanced-ip-scanner
    * balenaEtcher
    * putty

* Requisitos para el desarrollo de hardware:

    * Raspberry Pi 4 version B+ 8 Gb de memoria RAM.
    * pc linux OS.
    * MicroSD 32 Gb.
    * Cable micro HDMI - micro HDMI (Unicamente al momento de la programación)
    * Pantalla. (Unicamente al momento de la programación)
    * Cable de red rj45.
    * Cable de alimentaciòn 5v 3A
    * Caja switch con puertos rj45.
    * Tornillos y tuercas.
    * Separadores
    * Acrilico.
    * Tira de Leds.

    # Configuracion
IPs
```
ip: IP ( 172.25.0.1/24)

```
Descargar OS y aplicaciones
```
descarga las siguientes aplicaciones y sistema operativo de los siguientes links que son necesarios para implementar nuestro cluster de raspberry PIs
1.- https://blog.hypriot.com/downloads/
2.- https://putty.softonic.com/
3.- https://www.advanced-ip-scanner.com/
4.- https://alternativeto.net/software/etcher/about/

FORMATEAR SSD CARD
```
ante todo para iniciar todo el proceso devemos formatear nuestras ssd 

```
```
GRABAR OS Hypriot 
```
nececitamos instalar el sistema operativo en la targeta ssd, para esto utilizaremos BalenaEtcher utilizando un lector  de ssd

```
DETECTAR ips y establecer un host estatico

```
ahora devemos ingresar las ssd card a las raspberry PIs y realizar toda la conexion electronica necesaria para su funcionamiento. 

```

hosts master y slavos o nodos
```
# Existente Raspberry Pi SSH IPs  (192.168.0.1/24)
[inicializacion-nodos]
192.168.0.6 host_name=master-nodo static_host_ip=172.25.0.6/24 
192.168.0.7 host_name=slavo-nodo-01 static_host_ip=172.25.0.7/24


# Master nodo IPs
[master]
172.25.0.6

# slavo nodo IPs
[workers]
172.25.0.7
```

![alt text](imgs/pi-cluster "cluster de raspberry PIs!!!!!")



