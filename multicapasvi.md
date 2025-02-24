## [Configuración Switch Multicapa](README.md)

### 'Bloque Genérico'

1. `enable`
2. `conf term`
3. `no ip domain lookup`
4. `service password-encryption`
5. `enable secret class`
6. `hostname SWITCH_MULTICAPA`
7. `line console 0`
8. `password cisco`
9. `login`
10. `line vty 0 15`
11. `password cisco`
12. `login`
13. `banner motd #Usuario Autorizado#`
14. `vtp mode server` o `vtp mode client` ➡️ Depende de como hayamos configurado la red.
15. `vtp domain nombre_dominio`
16. `vtp password passwd_vtp`

### 'Creación VLAN'
---
> [!CAUTION]
> Solo si se crean las VLAN's como SWITCH SERVIDOR
---
1. `vlan 99`
2. `name ADMIN`
3. `vlan XX`
4. `name nombreXX`
5. `vlan YY`
6. `name vlanYY`
7. `vlan 50` ➡️ Esta será la Nativa
8. `name vlan50`

### 'Configuracion Interfaces'
(Activamos los f0/x que vayamos a utilizar)

1. `ip routing` ➡️ Con esto indicamos que vamos a enrutar
2. `int range f0/x-xx` ➡️ Seleccionamos lo que vayan a estar en mode access
3. `switchport mode access`
4. `shutdown` ➡️ Desactivamos todos los f0/x
5. `int f0/x`
6. `switchport access vlan XX` ➡️ Le decimos a que VLAN va este f0/x
7. `no shutdown` ➡️ Activamos el f0/x
8. `int range g0/x-x` ➡️ Seleccionamos los que vayan a estar en mode trunk
9. `switchport trunk native vlan XX` ➡️ Asignamos la VLAN Nativa
10. `no shutdown`
---
> [!WARNING]
> En los troncales no usamos switchport mode trunk
---


### 'Configuramos la IP'

1. `int vlan 99`
2. `ip address [ip_gateway] [mask]` ➡️ Configuramos la IP y Mask de la vlan ADMIN
3. `int vlan XX`
4. `ip address [ip_gateway] [mask]` ➡️ Configuramos la IP y Mask de la vlan XX
---
Siguiente -> [SWITCH SERVIDOR](servidorsvi.md) ➡️ En el caso que hayamos configurado el Switch Multicapa como "cliente"\
Siguiente -> [SWITCH CLIENTE](clientesvi.md) ➡️ En el caso que hayamos configurado el Switch Multicapa como "servidor"

