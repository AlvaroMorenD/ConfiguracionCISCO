## [Configuración Router](README.md)

### 'DHCP'

1. `enable`
2. `conf term`
3. `ip dhcp pool LANx` ➡️ Siendo x las vlans que hemos creado en el Switch Servidor. Haremos una pool por cada VLAN, excepto de la VLAN_Nativa.
4. `network [IP_RED] [Mask]` ➡️ Escribiremos la dirección de red de esa vlan y la máscara.
5. `default-router [IP_Gateway]` ➡️ Ponemos la puerta de enlace de esa vlan.
6. `dns-server 0.0.0.0` ➡️ En nuestro caso colocamos 0.0.0.0
7. `exit`
8. `ip dhcp excluded-address [IP]` ➡️ Excluiremos todas las IP's que queremos que sean estáticas, como las direcciones de puerta de enlace, los servidores, etc.
9. `end`
10. `wr`

---
Siguiente -> [IP's](ipdhcp.md)
