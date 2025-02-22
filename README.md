# ⚙️ Configuración CISCO
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
