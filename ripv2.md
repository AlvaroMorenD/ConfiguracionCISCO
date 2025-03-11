## [Configuración Router RIPv2](README.md)

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

### 'Configuración Serial con PPP-CHAP y Creación de Usuarios'

- `int sx/x/x` ➡️ Donde tengamos el cable que enlaza con otro Router.
- `description link to X` ➡️ Dirección al router que estemos configurando.
- `ip address IP mask`
- `encapsulation ppp`
- `ppp authentication chap`
- `clock rate 56000` ➡️ Solo si tenemos el DCE en este serial.
- `no shutdown`
- `exit`
- `username X password 1234` ➡️ Donde X será el/los Routers conectados.

### 'Configuración RIPv2'

- `router rip`
- `version 2`
- `network IP.RED` ➡️ Direcciones de Red conectadas directamente al Router
- `passive-interface g0/0`
- `end`
- `wr`

---
Siguiente -> [Router Híbrido](hibrido.md)
