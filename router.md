## [Configuración Router](README.md)

### 'Bloque Genérico'

1. `enable`
2. `conf term`
3. `hostname ROUTER`
4. `enable secret class`
5. `banner motd #Usuario NO Autorizado#`
6. `line console 0`
7. `password cisco`
8. `login`
9. `line vty 0 15`
10. `password cisco`
11. `login`

### 'Configuración Interfaces'

1. `int g0/x` ➡️ Siendo la x el puerto que vamos a utilizar para conectar el Router con el Switch_Servidor
2. `no ip address`
3. `no shutdown`
4. `int g0/x.xx` ➡️ Seleccionamos el g0/x y la VLAN xx dependiendo de las VLAN que hagamos
5. `encapsulation dot1q xx` ➡️ Siendo xx una VLAN creada
6. `ip address [ip] [mask]` ➡️ Ponemos la IP que nos faciliten con su Mask.
7. `no shutdown`

---
Siguiente -> [Comprobaciones](comprobaciones.md)
