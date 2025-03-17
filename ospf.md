## [Configuración Router OSPF](README.md)

### 'Bloque Genérico'

- `en`
- `conf term`
- `no ip domain lookup`
- `service password-encryption`
- `hostname Rx` ➡️ Ponemos el nombre de los Routers.
- `enable secret class`
- `banner motd #Frase_a_Introducir#`
- `line con 0`
- `password cisco`
- `login`
- `line aux 0`
- `password cisco`
- `login`
- `line vty 0 4`
- `password cisco`
- `login`

### 'Configuración GigaEthernet'

- `int gx/x` ➡️ Donde tengamos el PC conectado.
- `description link to PCx`
- `ip address IP mask`
- `no shutdown`

### 'Configuración Seriales'

- `int sx/x/x` ➡️ Donde tengamos el cable que enlaza con otro Router.
- `description link to X` ➡️ Dirección al router que estemos configurando.
- `ip address IP mask`
- `clock rate 56000` ➡️ Solo si tenemos el DCE en este serial.
- `no shutdown`
- `exit`

### 'Configuración OSPF'

- `router ospf 1`
- `router-id N-N-N-N` ➡️ Siendo N.N.N.N un número en cada router (1.1.1.1 o 2.2.2.2).
- `passive-interface g0/0`
- `network IP.red inv.mask area 0` ➡️ Un ejemplo: 192.168.0.0 0.0.0.255 area 0.
- `end`
- `wr`

>[!NOTE]
>Si configuramos un OSPF en seriales y RIP en los ethernet, debemos utilizar el comando redistribute rip subnets
---
