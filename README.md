# Laboratorio ICMPv6 Security con Containerlab

La topología creada tiene por objetivo poveer un entorno controlado para el análisis de seguridad del protocolo **ICMPv6**.
## Descripción de los nodos

| Nodo |OS  |
|--|--|
| Router |Nokia SRL Linux 24.10  
| Switch |Aruba AOS-CX 10.14
|PC1 y PC3|Kali Linux con THC IPv6 Tool e IPv6Toolkit 
|PC2 y PC4|Alpine Linux
## Acceso a los nodos
* Router Nokia vía SSH. `ssh admin@clab-icmpv6-srlrouter` password: `NokiaSrl1!`
* Switch Aruba vía SSH. `ssh admin@clab-icmpv6-arubaaccess` password: `admin`
* PCx vía bash. `docker exec -it clab-icmpv6-PCx /bin/bash`
## Ejemplos ataques
### MiTM/DOS vía Neighbor Spoofing (atk6-parasite6)
>This is an "ARP spoofer" for IPv6, redirecting all local traffic to your own
system (or nirvana if fake-mac does not exist) by answering falsely to
Neighbor Solitication requests.

![Alt text](images/topoatkparasite.png)

* Desde el nodo **srvweb** iniciar el servicio ejecutando el comando `nginx`
* Desde **arubaaccess** verificar la tabla de **IP bindings** ejecutando: `show nd-snooping bindings`
* Desde el nodo **PC1** Kali
  * Habilitar enrutamiento: `sysctl -w net.ipv6.conf.eth1.forwarding=1`
  * Lanzar el ataque ejecutando: `atk6-parasite6 eth1`
* Desde **PC3**
  * Realizar consulta http ejecutando `http http://[2001:db8:d1::50]`
* Desde **arubaaccess** verificar la mitigación del ataque ejecutando: `show nd-snooping statistics` 
