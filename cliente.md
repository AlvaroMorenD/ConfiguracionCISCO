## [Switch Servidor](README.md)

### 'Bloque Genérico'

1. `enable`
2. `conf term`
3. `no ip domain lookup`
4. `enable secret class`
5. `hostname SWITCH_CLIENTE`
6. `line console 0`
7. `password cisco`
8. `login`
9. `line vty 0 15`
10. `password cisco`
11. `login`
12. `banner motd #Usuario NO Autorizado#`
13. `vtp mode client`
14. `vtp domain nombre_dominio`
15. `vtp password passwd_vtp`

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

