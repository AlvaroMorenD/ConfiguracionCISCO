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
