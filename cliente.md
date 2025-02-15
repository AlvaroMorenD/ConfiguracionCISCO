## [Configuración Switch Cliente](README.md)

### 'Bloque Genérico'

1. `enable`
2. `conf term`
3. `no ip domain lookup`
4. `service password-encryption`
5. `enable secret class`
6. `hostname SWITCH_CLIENTE`
7. `line console 0`
8. `password cisco`
9. `login`
10. `line vty 0 15`
11. `password cisco`
12. `login`
13. `banner motd #Usuario NO Autorizado#`
14. `vtp mode client`
15. `vtp domain nombre_dominio`
16. `vtp password passwd_vtp`

### 'Configuracion Interfaces'
(Activamos los f0/x que vayamos a utilizar)

1. `int range f0/1-24` ➡️ Seleccionamos los que van en mode access
2. `switchport mode access`
3. `shutdown` ➡️ Desactivamos todos los f0/x
4. `int f0/x` ➡️ Seleccionamos los f0/x que tengan asignados PCS's 
5. `switchport access vlan XX` ➡️ Le decimos a que VLAN va este f0/x
6. `no shutdown`
7. `int range g0/1-2` ➡️ Seleccionamos los que vayan a estar en mode trunk
8. `switchport mode trunk` ➡️ Asignamos la VLAN Nativa
9. `switchport trunk native vlan XX`
10. `no shutdown`

### 'Configuramos la IP'
1. `int vlan 99`
2. `ip address [ip] [mask]` ➡️ Configuramos la IP y Mask de la vlan ADMIN
3. `no shutdown`
4. `ip default-gateway [ip]` ➡️ Asignamos Gateway predeterminada

Siguiente -> [Configurar IP's](ips.md)
