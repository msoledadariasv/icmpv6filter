# Laboratorio ICMPv6 Security con Containerlab
---
La topología creada tiene por objetivo poveer un entorno controlado para el analisis de seguridad del protocolo ICMPv6.
## Descripción de los nodos
* Router Nokia SRL Linux 24.10
* Switch Aruba AOS-CX 10.14
* PC1 y PC3: Kali Linux con THC IPv6 Tool y IPv6Toolkit
* PC2 y PC4: Alpine Linux
## Acceso a los nodos
* Router Nokia vía SSH. admin@clab-icmpv6-srlrouter password: NokiaSrl1!
* Switch Aruba vía SSH. admin@clab-icmpv6-arubaaccess password: admin
* PCx vía bash. docker exec -it clab-icmpv6-PCx /bin/bash
## Vista gráfica
---
![Alt text](images/topoicmpv6.png)

