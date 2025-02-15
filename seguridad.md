## [Configuración Seguridad](README.md)

Para configurar la Seguridad en los puertos de ambos Switches, tendremos que:

1. `int range f0/x-x` ➡️ Seleccionamos los puertos que hemos usado como `mode access`.
2. `switchport port-security`
3. `switchport port-security maximum N` ➡️ Siendo N el numero de macs que permitimos el cambio.
4. `switchport port-security mac-address sticky`
5. `switchport port-security violation shutdown` ➡️ Utilizamos shutdown por ser el más potente

> [!WARNING] 
> NUNCA ponemos seguridad en los puertos que hemos declarado como mode trunk

> [!NOTE]
> Para entrar desde el PC Admin, usamos el comando ssh -l usuario IP_Switch

Siguiente -> [Configurar EtherChannel](etherchannel.md)
