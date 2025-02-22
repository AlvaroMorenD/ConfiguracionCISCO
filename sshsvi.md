## [Configuración SSH](README.md)

Vamos a configurar el acceso a SSH en ambos Switches:
1. `conf term`
2. `username usuario1 password clave1`
3. `line vty 0 15`
4. `login local`
5. `transport input ssh`
6. `exit`
7. `ip domain-name ejemplo.es`
8. `crypto key generate rsa`
9. Ahora escribimos los modulos: `1024`
10. `exit`
11. `wr`

---
> [!WARNING]
> Esto tendremos que hacerlo en todos Switches

---
> [!NOTE]
> Para entrar desde el PC Admin, usamos el comando ssh -l usuario_declarado IP_Switch

---
Siguiente -> [Configurar Seguridad](seguridadsvi.md)
