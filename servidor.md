## [Configuración Switch Servidor](README.md)

### 'Bloque Genérico'

1. `enable`
2. `conf term`
3. `no ip domain lookup`
4. `service password-encryption`
5. `enable secret class`
6. `hostname SWITCH_SERVIDOR`
7. `line console 0`
8. `password cisco`
9. `login`
10. `line vty 0 15`
11. `password cisco`
12. `login`
13. `banner motd #Usuario Autorizado#`
14. `vtp mode server`
15. `vtp domain nombre_dominio`
16. `vtp password passwd_vtp`

### 'Creación VLAN'
(Crearemos en este caso 6 VLAN's)

1. `vlan 99`
2. `name ADMIN`
3. `vlan 10`
4. `name nombre10`
5. `vlan 20`
6. `name vlan20`
7. `vlan 30`
8. `name vlan30`
9. `vlan 40`
10. `name vlan40`
11. `vlan 50` ➡️ Esta será la Nativa
12. `name vlan50`

### 'Configuramos la IP'
1. `int vlan 99`
2. `no ip address`
3. `ip address [ip] [mask]` ➡️ Configuramos la IP y Mask de la vlan ADMIN
4. `no shutdown`
5. `ip default-gateway [ip]` ➡️ Asignamos Gateway predeterminada

### 'Configuracion Interfaces'
(Activamos los f0/x que vayamos a utilizar)

1. `int range f0/1-24` ➡️ Seleccionamos lo que vayan a estar en mode access
2. `switchport mode access`
3. `shutdown` ➡️ Desactivamos todos los f0/x
4. `int f0/x`
5. `switchport access vlan XX` ➡️ Le decimos a que VLAN va este f0/x
6. `no shutdown` ➡️ Activamos el f0/x
7. `int range g0/1-2` ➡️ Seleccionamos los que vayan a estar en mode trunk
8. `switchport mode trunk` ➡️ Asignamos la VLAN Nativa
9. `switchport trunk native vlan XX`
10. `no shutdown`

---
Siguiente -> [SWITCH CLIENTE](cliente.md)
