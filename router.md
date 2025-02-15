## [Configuración Router](README.md)

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
12. `int g0/x`
13. `no ip address`
14. `no shutdown`
15. `int g0/x.xx` ➡️ Seleccionamos el g0/x y la VLAN xx dependiendo de las VLAN que hagamos
16. `encapsulation dot1q xx` ➡️ Siendo xx una VLAN creada
17. `ip address [ip] [mask]` ➡️ Ponemos la IP que nos faciliten con su Mask.
18. `no shutdown`
19. `end`
20. `wr`
