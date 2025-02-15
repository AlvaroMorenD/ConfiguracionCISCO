## [Configuración del EtherChannel](README.md)

1. `int range f0/x-x (o g0/x-x)` ➡️ Seleccionamos el rango que hayamos elegido para el `mode trunk`
2. `channel-group 1 mode auto`
3. `int port-channel 1`
4. `switchport mode trunk` 
5. `end`

> [!WARNING]
> Esto lo hacemos en ambos Switches, tanto en Servidor como en Cliente
