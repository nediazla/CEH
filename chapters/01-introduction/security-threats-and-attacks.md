# Security threats and attacks

- Cuanto más valiosa sea la información, mayores serán las amenazas y las posibilidades de un ataque.

## Amenazas de seguridad

📝 **Amenaza** significa cualquier cosa que tenga el potencial de causar daños al sistema.

### Tipos de amenazas

#### Amenazas de red

- **Red** es el conjunto de dispositivos que están conectados a través de canales de comunicación donde se produce el intercambio de datos entre dispositivos.
- El atacante puede irrumpir en el canal y robar la información que se intercambia.
Ejemplos:
	• [ataques de denegación de servicio (DoS)](./../13-web-applications/denial-of-service.md) 
	• [ataques basados ​​en contraseñas](./../06-system-hacking/cracking -passwords-overview.md) 
	• ataques de clave comprometida, ataques de firewall e IDS 
	• envenenamiento de DNS y ARP 
	• ataque de intermediario (MITM) 
	• suplantación de identidad 
	• [secuestro de sesión](./../13-web-applications/ session-hijacking.md) 
	• recopilación de información 
	• sniffing...

#### Amenazas del host

- Ataque que intenta acceder a la información de un sistema
Ejemplos:
	• [ataques de contraseña](./../06-system-hacking/cracking-passwords-overview.md) 
	• acceso no autorizado 
	• creación de perfiles 
	• [ataques de malware](./../07-malware/malware-overview.md ) 
	• [huella](./../02-footprinting/footprinting-overview.md) 
	• [ataques de denegación de servicio (DoS)](./../13-web-applications/denial-of-service.md ) 
	• ejecución de código arbitrario 
	• escalada de privilegios 
	• [ataques de puerta trasera](./../07-malware/malware-overview.md#backdoor) 
	• amenazas de [seguridad física](./physical-security.md)

#### Amenazas de aplicaciones

- Explotación de vulnerabilidades que existen en la propia aplicación.
	 - Causado por, p.e. malas prácticas de codificación
	 - Los programas apresurados tienen errores, Ejemplo: falta de validación de los datos de entrada
- Se puede encontrar mediante ingeniería inversa o prueba y error.
- Los códigos grandes que son difíciles de mantener tienen más vulnerabilidades.
- Principalmente debido a una validación de entrada incorrecta.
Ejemplos:
	• [Inyección SQL](./../14-sql-injection/sql-injection-overview.md) 
	• secuencias de comandos entre sitios 
	• [secuestro de sesión](./../13-web-applications/session-hijacking .md) 
	• suplantación de identidad 
	• validación de entrada inadecuada 
	• configuración incorrecta de seguridad 
	• divulgación de información 
	• [manipulación de campos ocultos](./../13-web-applications/hacking-web-applications.md#hidden-field-manipulation) 
	• gestión de sesión rota 
	• [ataques de criptografía](./../15-cryptography/cryptanalysis.md#cryptography-attacks) 
	• [ataques de desbordamiento de búfer](./../12-web-servers/web-server-threats- and-attacks.md#buffer-overflow-attacks) 
	• [phishing](./../10-social-engineering/social-engineering-types.md#phishing)

## Ataques de seguridad

- O **ataque cibernético**
- Intentar obtener acceso no autorizado a un sistema o red.
- Actualización de una amenaza.

### Motivos

- Ataque = Motivo + Vulnerabilidad + Método (explotar)
- El núcleo general de todos los motivos es el acceso a la información valiosa.
- Motivos comunes:
	 - Interrumpir el flujo de actividades y procesos comerciales.
	 - Robar información valiosa.
	 - Manipulación de datos
	 - Robar dinero e información financiera importante.
	 - Venganza
	 - Rescate

### Tipos de ataques

- Es necesario encontrar la vulnerabilidad en un sistema para sufrir un ataque.
- Nunca se puede demostrar que no es vulnerable, pero sí se puede demostrar que es vulnerable.
 - o Nunca se puede demostrar que un sistema es seguro, pero sí se puede demostrar que es inseguro.

#### Ataques al sistema operativo

❗ Si el sistema operativo se hace cargo, proteger las aplicaciones no importará.
- Las vulnerabilidades incluyen
	 - Errores (ya que es una gran base de código)
	 - Desbordamiento del búfer
	 - Sistemas operativos sin parches
		 - Puede generar clientes potenciales exitosos utilizando vulnerabilidades ya conocidas.
		 🤗 Ejemplo: Microsoft ya había parcheado la [vulnerabilidad EternalBlue](https://en.wikipedia.org/wiki/EternalBlue) que desarrolló la NSA antes de que se filtrara al público. Sin embargo, muchos sistemas aún no estaban parcheados debido a que los usuarios no actualizaban sus sistemas. Por lo tanto, la misma vulnerabilidad en sistemas sin parches fue explotada con éxito primero por [el ransomware WannaCry](https://en.wikipedia.org/wiki/WannaCry_ransomware) que comprometió cientos de miles de computadoras, y luego por el [malware NotPetya](https:/ /en.wikipedia.org/wiki/Petya_(malware)).
- Los ataques incluyen
	 - Explotación de implementaciones de protocolos de red.
	 - [Ataques de autenticación](./../13-web-applications/hacking-web-applications.md#authentication-attacks)
	 - [Descifrar contraseñas](./../06-system-hacking/cracking-passwords-overview.md)
	 - Rompiendo la seguridad del sistema de archivos
  💡 Secure OS es un sistema operativo que se actualiza, monitorea y regula con la mayor frecuencia posible.
- Véase también [captación de banners](./../03-scanning-networks/banner-grabbing.md)

#### Ataques de mala configuración

- El hacker obtiene acceso al sistema que tiene la seguridad mal configurada.
- Puede afectar obras, bases de datos, servidores web, etc.
Ejemplos: 
	• usar cuentas predeterminadas (contraseñas) 
	• olvidar el servidor Apache en línea para permitir solicitudes de proxy que permitan ataques DDoS
💡 Detectado principalmente por escáneres automatizados

#### Ataques a nivel de aplicación

- Similares a los ataques al sistema operativo, pero mucho menos dañinos ya que su alcance es mucho más limitado.
- Causado por la falta de pruebas, ya que los desarrolladores se apresuran en el desarrollo de aplicaciones y se pierden algo.
Ejemplos: 
	• divulgación de información confidencial 
	• ataque de desbordamiento de buffer 
	• inyección SQL v secuencias de comandos entre sitios 
	• denegación de servicio por secuestro de sesión 
	• hombre en el medio 
	• phishing
🤗 Ejemplo: Cliente torrent de transmisión (macOS)
	 - La tienda donde se descargó estaba comprometida.
	 - Sustituyeron el enlace de descarga de torrent por su propia aplicación.
	 - Consulte [La transmisión se piratea para propagar malware](https://blog.malwarebytes.com/threat-analysis/2016/09/transmission-hijacked-again-to-spread-malware/)

#### Ataques de código retráctil

- Ataques a bibliotecas y frameworks de los que depende el software.
- Encontrar vulnerabilidades en bibliotecas permite reutilizar los mismos exploits en más de una sola aplicación.
💡 Utilice bibliotecas: más antiguas, más maduras, mantenidas, actualizadas activamente con un historial comprobado.
- Ejemplos:
	 - Se corrigió un error en la biblioteca, pero la aplicación usa una versión anterior.
	 - La aplicación utiliza bibliotecas en modo de depuración o con configuraciones predeterminadas.

### Vectores de ataque

- Vector de ataque = Medio por el cual los piratas informáticos entregan una carga útil a los sistemas y redes
- [Amenazas de la computación en la nube](./../16-cloud-computing/cloud-security.md#cloud-computing-risks-and-threats), como la violación y pérdida de datos.
- [Amenazas de IoT](./../18-iot-and-ot/iot-security.md#iot-threats) generalmente causadas por dispositivos inseguros y limitaciones de hardware (batería, memoria, CPU, etc.)
- [Ransomware](../07-malware/malware-overview.md#ransomware): restringe el acceso a sus archivos y requiere un pago para poder acceder
- [Amenazas móviles](./../17-mobile-platforms/mobile-attacks.md#mobile-threats)

#### Amenazas persistentes avanzadas (APT)

📝 Actor de amenazas sigiloso con ataques continuos dirigidos a una entidad específica.
- Los grupos APT incluyen:
	 - [APT 10 - Apolo rojo @China](https://en.wikipedia.org/wiki/Double_Dragon_(hacking_organization))
	 - [Grupo de ecuaciones @USA](https://en.wikipedia.org/wiki/Equation_Group)
	 - [APT 29 - Oso acogedor @Rusia](https://en.wikipedia.org/wiki/Cozy_Bear)
	 - y [muchos más](https://en.wikipedia.org/wiki/Advanced_persistent_threat#APT_groups)...
- **Avanzado**
	 - Utiliza malware especial, a menudo diseñado para organizaciones específicas.
		 - Generalmente es una versión modificada del malware común utilizado en botnets.
	 - Técnicas sofisticadas contra objetivos no genéricos.
- **Persistente**
	 - Presencia a largo plazo con mando y control externos.
	 - Extrayendo datos
		 - Generalmente ***bajo y lento*** para evitar la detección
		 - Ejemplo: en lugar de enviar big data, divide los datos en fragmentos y envía cada fragmento cada vez que un usuario está conectado a Internet.
- **Amenaza**
	 - Se dirige a organizaciones e información de alto valor.
	 - Ejemplo: gobiernos y grandes empresas
🤗 Ejemplos
	 - [Hack de Sony Pictures](https://en.wikipedia.org/wiki/Sony_Pictures_hack) donde datos confidenciales de Sony, p.e. Películas inéditas se publicaron como torrents.
	 - [Violación de datos del gobierno federal de los Estados Unidos en 2020](https://en.wikipedia.org/wiki/2020_United_States_federal_government_data_breach) donde más de 18.000 empresas y agencias gubernamentales estadounidenses fueron pirateadas.
- Pasos comunes
	 1. Crear una infracción, Ejemplo: través de phishing
	 2. Explotar las vulnerabilidades internas del sistema
	 3. Control del sistema o de sus segmentos
	 4. Exfiltración de datos (= transferencia de datos no autorizada)

#### Virus y gusanos

- Ambos pueden replicarse en todo el sistema en archivos, documentos.
- Tener capacidades para infectar sistemas y redes en poco tiempo.
- [Virus](./../07-malware/viruses.md): Requiere la acción del usuario para ser activado, Ejemplo: ejecutando un archivo que tiene un virus incrustado.
- [Gusano](./../07-malware/malware-overview.md#worm): puede propagarse de forma independiente sin ninguna acción del usuario, es decir, autorreplicarse.

#### Red de bots

📝 Utilizado por piratas informáticos para controlar las máquinas infectadas, Ejemplos: teléfonos, PC, IoT
- Los piratas informáticos realizan actividades maliciosas desde las máquinas en las que se ejecutan los bots, por ejemplo. Ataques DDoS.
- El principal problema es la falta de software de seguridad o de actualizaciones adecuadas en los dispositivos.
- Véase también [Botnets troyanos](./../07-malware/trojans.md#botnet-trojans) y [Botnets | Denegación de servicio](./../13-web-applications/denial-of-service.md#botnets)

#### Ataques internos

- Realizado por una persona de dentro de la organización que tenga acceso autorizado.
	 - Ejemplos: empleado descontento, empleado pagado por un tercero
- Presenta uno de los ataques con mayor potencial de riesgo y más difíciles de defender.
- Véase también [Ataques internos |Tipos de ingeniería social](./../10-social-engineering/social-engineering-types.md#insider-attacks).

##### Insider threat types

- **Pure insider**
  - Inside employee with normal access rights
- **Elevated pure insider**
  - Insider with elevated access
- **Insider associate**
  - Insider with limited authorized access (e.g. guard, cleaning person)
- **Insider affiliate**
  - Spouse, friend, or client of an employee that uses employee's credentials.
- **Outsider affiliate**
  - Unknown and untrusted person from outside the organization.
  - Uses an open access channel or stolen credentials to gain unauthorized access.

##### Insider attack countermeasures

- Restricting access
- Logging to know who access what at what point of time
- Active monitoring of employees with elevated privileges
- Trying to not have disgruntled employees
- Separation of duties
  - Also known as **segregation of duties**
  - Concept of having more than one person required to complete a task.
  - See also [Separation of duties | Cloud computing](./../16-cloud-computing/cloud-computing.md#separation-of-duties)

#### Phishing

- See [Phishing | Social Engineering Types](./../10-social-engineering/social-engineering-types.md#phishing)

#### Web application threats

- Takes advantage of poorly written code and lack of proper validation of input and output data.
- E.g. buffer overflows, SQL injections, cross-site scripting
💡 There are many online scanning tools to detect those.

## Modern age information warfare

- Use of information and communication technologies for competitive advantages over an opponent
- Weapons include • viruses • worms • trojan horses • logic bombs • trap doors • nano machines and microbes • electronic jamming • penetration exploits and tools.
- E.g.
  - Corporations spy on each other to use each others technology secrets and patents
    🤗 Also known as [Industrial espionage](https://en.wikipedia.org/wiki/Industrial_espionage)
  - Governments spy on other governments by using hackers as proxies to gain information about e.g. defense systems.
  - Intellectual property thefts with reverse engineering to create products without investing in R&D
- Categories include:
  - **Command and control (C2) warfare**
    - Taking down the command center may protect the headquarters but may interfere with their mobility
  - **Intelligence-based warfare**
    - Sensor-based technology to disrupt systems
  - **Electronic warfare**
    - Enhance, degrade, or intercept the flow of information
  - **Psychological warfare**
    - "Capture their minds and their hearts and souls will follow"
    - E.g. propaganda or terror
  - **Hacker warfare**
    - Acquire information about subject A, sell it to subject B.
  - **Economic information warfare**
    - Channeling or blocking information to pursue economic dominance
  - **Cyber warfare**: use of information systems against virtual personas
- Each category can have:
  - **Offensive strategy**
    - Attacks against an opponent
    - E.g. web application attacks, malware attacks, system hacking..
  - **Defensive strategy**
    - Actions taken against attacks.
    - E.g. monitoring, alerts, response, detection, prevention systems
- See also [Information Warfare website](http://www.iwar.org.uk)
