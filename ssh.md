## [Configuración SSH](README.md)

Vamos a configurar el acceso a SSH en ambos Switches:
1. `username usuario1 password clave1`
2. `line vty 0 15`
3. `login local`
5. `transport input ssh`
5. `exit`
6. `ip domain-name ejemplo.es`
7. `crypto key generate rsa`
8. Ahora escribimos los modulos: `1024`
9. `exit`
10. `wr`

> [!WARNING]
> Esto tendremos que hacerlo en ambos Switches

Siguiente -> [Configurar Seguridad](seguridad.md)
