## [Configuración del EtherChannel](README.md)

1. `conf term`
2. `int range f0/x-x (o g0/x-x)` ➡️ Seleccionamos el rango que hayamos elegido para el `mode trunk`
3. `channel-group 1 mode auto`
4. `int port-channel 1`
5. `switchport mode trunk` 
6. `end`
7. `wr`

---
> [!WARNING]
> Esto lo hacemos en ambos Switches, tanto en Servidor como en Cliente

---
Siguiente -> [Configurar Router](router.md)
