## [Configuración Seguridad](README.md)

Para configurar la Seguridad en los puertos de ambos Switches, tendremos que:

1. `conf term`
2. `int range f0/x-x` ➡️ Seleccionamos los puertos que hemos usado como `mode access`.
3. `switchport port-security`
4. `switchport port-security maximum N` ➡️ Siendo N el numero de macs que permitimos el cambio.
5. `switchport port-security mac-address sticky`
6. `switchport port-security violation shutdown` ➡️ Utilizamos shutdown por ser el más potente

---
> [!WARNING] 
> NUNCA ponemos seguridad en los puertos que hemos declarado como mode trunk

---
> [!TIP]
> Para comprobar la seguridad, cambiamos la mac de un PC dos veces y debería de apagarnos el puerto al tercer cambio 

---
Siguiente -> [Configurar EtherChannel](etherchannel.md)
