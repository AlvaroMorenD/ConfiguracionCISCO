## [Configuración del Router](README.md)

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

### 'Configuración PPP-CHAP'

- `int sx/x/x` ➡️ Donde tengamos el cable que enlaza con otro Router.
- `description link to Rx` ➡️ Dirección al router que estemos configurando.
- `ip address IP mask`
- `encapsulation ppp`
- `ppp authentication chap`
- `no shutdown`
- `exit`

### 'Configuración de Usuario y Contraseña'

- `username Rx password 1234` ➡️ Nombramos el router que tengamos enlazado con el que estamos configurando.
> [!WARNING]
> Si tenemos dos routers conectados, tenemos que poner los dos username Rx que tengamos enlazados.

### 'Configuración Rutas'

- `ip route dir.red mask ip_gateway` ➡️ Configuraremos tantas rutas como direcciones de red tengamos.
> [!WARNING]
> La ip_gateway será la más cercana a la dir.red, pero que esté conectado a nuestro router.
---

Siguiente -> [IP's](ips_pcs.md)

