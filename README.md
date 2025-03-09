# ⚙️ Configuración CISCO
---

- [Router On a Stick](#Router on a stick)
### [Switches SVI](#Switches SVI)
### [Configuración DHCP](#Configuración DHCP)
### [PPP - PAP](#PPP - PAP)
### [PPP - CHAP](#PPP - CHAP)

---
## 🛜 Router on a Stick

Manual que tenemos que seguir para configurar un Router y dos Switches con VLAN's:

1. Colocamos los PC's, los Switches y el Router. Cableamos los Switches con los PC's.

2. Configuramos el **[Switch servidor](servidor.md)**.

3. Configuramos el **[Switch cliente](cliente.md)**.

4. Asignamos las [IP's](ips.md) a los PC's.

5. Configuramos el **[SSH](ssh.md)** en el Switch servidor.

6. Configuramos la **[Seguridad](seguridad.md)** en ambos Switches.

7. Unimos los dos Switches con los g0/x que hemos configurado como `mode trunk`.

8. Configuramos el **[EtherChannel](etherchannel.md)** en el que caso de que nos lo indiquen.

9. Configuramos el **[Router](router.md)**.

10. Unimos el **Switch Servidor** con el **Router** por el *g0/x* que hemos configurado.

---
## 💿 Switches SVI

Manual que tenemos que seguir para configurar un Switch Multicapa y dos Switches con VLAN's:

1. Colocamos los PC's, los Switches y el Switch Multicapa. Cableamos los Switches con los PC's.

2. Configuramos el **[Switch multicapa](multicapasvi.md)**. Es el que va a enrutar 
  - ‼️ Si lo vamos a configurar como "servidor", lo configuramos primero.
  - ‼️ Si lo vamos a configurar como "cliente", lo configuraremos despues del "servidor"

3. Configuramos el **[Switch servidor](servidorsvi.md)**.

4. Configuramos el **[Switch cliente](clientesvi.md)**.

5. Asignamos las [IP's](ips.md) a los PC's.

6. Conectamos los cables que hemos configurado entre los Switches.

7. Configuramos el **[SSH](sshsvi.md)**.

8. Configuramos la **[Seguridad](seguridadsvi.md)** en todos los Switches.

9. Unimos los dos Switches con los g0/x que hemos configurado como `mode trunk`.

10. Configuramos el **[EtherChannel](etherchannelsvi.md)** en el que caso de que nos lo indiquen.
---

## 🌐 Configuración DHCP

1. Seleccionamos el **[Router](routerdhcp.md)** que ya tenemos configurado.
2. Modificamos las **[IP's](ipdhcp.md)** de los PC's a dinámica
---

## 🔒 PPP - PAP

1. Apagamos los Routers para colocarle el módulo **[HWIC - 2T](hwic2t.md)**.
2. Configuramos todos los **[Routers](routerpap.md)** de la misma manera, excepto al poner el username password.
3. Añadimos las IP's de los **[PC's](ips_pcs.md)** y probamos a hacer ping a todos los PC's.
