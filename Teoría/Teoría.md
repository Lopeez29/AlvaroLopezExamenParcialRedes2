Ejercicio 1. 


Pregunta: ¿Cómo dividirías la red 172.16.0.0/24 en subredes para satisfacer las necesidades anteriores, asignando direcciones IP a cada segmento de la base? Indica las subredes obtenidas (con su notación de máscara /xx), la cantidad de hosts útiles en cada una, y especifica qué subred se destinaría al enlace troncal interplanetario.


Comando Central: ~50 hosts (dispositivos)

Defensa Perimetral: ~30 hosts

Centro Médico: ~20 hosts

Hangar y Taller: ~14 hosts


### Respuesta:


Ejercicio 2.


Pregunta: Compara el enrutamiento estático con el enrutamiento dinámico. ¿Cuáles son las ventajas e inconvenientes de cada enfoque en la administración de rutas? En tu respuesta, menciona al menos un protocolo de enrutamiento dinámico (por ejemplo, RIP u OSPF) y comenta por qué los protocolos de vector de distancia difieren de los de estado de enlace en términos de rendimiento y complejidad​


### Respuesta:

El enrutamiento estático consiste en establecer manualmente las rutas que el tráfico debe seguir dentro de una red. Esto le otorga al administrador un control total sobre el comportamiento del router, lo que resulta especialmente útil en redes pequeñas o fijas. Su mayor ventaja es la simplicidad, ya que no requiere protocolos adicionales ni un procesamiento constante. Sin embargo, su principal desventaja es la falta de adaptabilidad: si un nodo falla o hay un cambio en la red, la información no se actualiza automáticamente, lo que puede provocar interrupciones en la comunicación.

Por otro lado, el enrutamiento dinámico permite que los routers ajusten automáticamente las rutas según el estado actual de la red. Esto se logra a través de protocolos de enrutamiento dinámico, como RIP o OSPF, que intercambian información con otros routers para conocer la red y seleccionar las mejores rutas disponibles. Este tipo de enrutamiento ofrece una gran adaptabilidad y eficiencia, especialmente en redes grandes o en constante cambio. por ejemplo, pertenece a la categoría de protocolos de vector de distancia, donde se calcula la mejor ruta basándose en el número de saltos. En cambio, OSPF es un protocolo de estado de enlace, que utiliza un mapa completo de la red para calcular la ruta más corta y eficiente.

La diferencia entre ambos tipos de protocolos radica en su rendimiento y complejidad. Los de vector de distancia son más fáciles de implementar, pero menos eficientes y más propensos a errores en redes grandes. Por otro lado, los de estado de enlace ofrecen un mejor rendimiento al calcular rutas óptimas más rápidamente, aunque requieren más recursos y una configuración más compleja. En resumen, mientras que el enrutamiento estático es adecuado para escenarios simples y controlados, el dinámico es esencial en redes complejas y cambiantes, donde la resiliencia y la actualización automática son fundamentales.


Ejercicio 3.

Pregunta: Explica el funcionamiento básico del sistema DNS y su importancia en la comunicación en redes. ¿Cómo realiza la red rebelde (o cualquier red TCP/IP) la resolución de nombres de dominio a direcciones IP? Incluye en tu explicación qué es un servidor DNS y un registro (por ejemplo, un registro A), ilustrando con un ejemplo simple (por ejemplo: traducir holonet.rebelion.org a una dirección IP)​

### Respuesta:

El Sistema de Nombres de Dominio, conocido como DNS, cumple un papel esencial en redes como Internet o la HoloRed rebelde. Su función es traducir nombres de dominio legibles, como holonet.rebelion.org, en direcciones IP numéricas que los sistemas de red pueden procesar, por ejemplo, 203.0.113.42. Sin esta traducción, los dispositivos no podrían establecer comunicación usando nombres simbólicos.

El proceso de resolución comienza cuando un equipo necesita conocer la IP asociada a un dominio. Este equipo actúa como cliente DNS, enviando una consulta al servidor DNS configurado. Si este servidor no tiene la respuesta guardada en su caché, inicia una búsqueda recursiva preguntando a los servidores raíz, luego a los de nivel superior (como .org), y finalmente al servidor autoritativo del dominio (rebelion.org), que contiene los registros oficiales.

Dentro de estos registros, el tipo A es el más común cuando se busca la dirección IPv4 de un dominio. Por ejemplo, un registro A para holonet.rebelion.org podría devolver la IP 203.0.113.42, junto con un valor TTL que indica cuánto tiempo puede mantenerse esa respuesta en caché.

Si este sistema falla, y los servidores DNS dejan de estar disponibles, no se podrían traducir los nombres a IP. Esto interrumpiría servicios como navegación web, conexión a APIs o comunicaciones por SSH. Aunque físicamente los equipos estén conectados, sin DNS, la Alianza quedaría prácticamente incomunicada salvo que memoricen todas las IPs, lo cual es poco práctico en una red dinámica y distribuida.


Ejercicio 4: 

Pregunta: Compara los protocolos TCP y UDP y sus características en contexto de la transmisión de datos. ¿Por qué TCP se considera un protocolo confiable y orientado a conexión, y qué implica eso en cuanto a rendimiento? ¿Por qué UDP es no confiable y sin conexión, y en qué casos su rapidez resulta ventajosa?​

### Respuesta:

TCP y UDP son protocolos de transporte con funciones distintas en la transmisión de datos. TCP es confiable y orientado a conexión, lo que significa que establece un canal seguro entre emisor y receptor antes de enviar datos. Este protocolo garantiza que los datos lleguen completos, en orden y sin errores, lo que lo hace ideal para navegación web, correo electrónico o envío de planes estratégicos en la red rebelde. A cambio, introduce más latencia y usa más recursos.

En cambio, UDP es no confiable y sin conexión. No establece un canal previo ni verifica la entrega, simplemente envía los datos lo más rápido posible. Eso lo vuelve más eficiente y con menor retardo, lo que es clave en aplicaciones como streaming, juegos o envío de coordenadas de combate en tiempo real, donde importa más la velocidad que la precisión absoluta. Su rapidez es una ventaja táctica cuando cada milisegundo cuenta, aunque se pierda algún dato por el camino.
