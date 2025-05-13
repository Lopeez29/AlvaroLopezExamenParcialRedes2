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

Por otro lado, el enrutamiento dinámico permite que los routers ajusten automáticamente las rutas según el estado actual de la red. Esto se logra a través de protocolos de enrutamiento dinámico, como RIP o OSPF, que intercambian información con otros routers para conocer la red y seleccionar las mejores rutas disponibles. Este tipo de enrutamiento ofrece una gran adaptabilidad y eficiencia, especialmente en redes grandes o en constante cambio. Por ejemplo, el protocolo RIP, determina la mejor ruta en función del número de saltos. En cambio, OSPF utiliza un mapa completo de la red para calcular la ruta más corta y eficiente.

La diferencia entre ambos tipos de protocolos radica en su rendimiento y complejidad. Los de vector de distancia son más fáciles de implementar, pero menos eficientes y más propensos a errores en redes grandes. Por otro lado, los de estado de enlace ofrecen un mejor rendimiento al calcular rutas óptimas más rápidamente, aunque requieren más recursos y una configuración más compleja. En resumen, mientras que el enrutamiento estático es adecuado para escenarios simples y controlados, el dinámico es esencial en redes complejas y cambiantes, donde la resiliencia y la actualización automática son fundamentales.


Ejercicio 3.

Pregunta: Explica el funcionamiento básico del sistema DNS y su importancia en la comunicación en redes. ¿Cómo realiza la red rebelde (o cualquier red TCP/IP) la resolución de nombres de dominio a direcciones IP? Incluye en tu explicación qué es un servidor DNS y un registro (por ejemplo, un registro A), ilustrando con un ejemplo simple (por ejemplo: traducir holonet.rebelion.org a una dirección IP)​

### Respuesta:

El DNS es crucial para las redes que usan TCP/IP, ya que ayuda a traducir nombres como Holonetrebelionorg en direcciones IP necesarias para la comunicación del dispositivo. Este método es similar a una lista de teléfonos para Internet: en lugar de recordar números, las personas usan nombres simples, y el DNS busca hacia arriba y devuelve la dirección IP correcta

El trabajo del servidor DNS es obtener una consulta, que verifique si la IP vinculada al nombre solicitado está en su memoria y, si no, pase la solicitud a otros servidores DNS hasta que obtenga una respuesta. Este sistema utiliza una estructura similar a un árbol con una raíz principal que guía la búsqueda a los servidores para cada nivel de dominio. Un tipo de registro frecuente es el tipo A, que relaciona un nombre de dominio con una dirección IPv4.

Por ejemplo, si un navegador intenta acceder a holonet.rebelion.org, su sistema operativo consulta primero el servidor DNS local. Si no tiene la respuesta, este consulta a su proveedor de Internet, que a su vez contacta con otros servidores DNS hasta encontrar el registro A que devuelve la dirección IP correspondiente.

Si el servidor DNS no está disponible, el sistema no puede traducir los nombres simbólicos, lo que imposibilita el acceso a servicios como páginas web, correo electrónico o bases de datos en red. En el contexto de la red rebelde, esto significaría quedar incomunicados, ya que no podrían resolver nombres como echo.base o endor.transmisiones para establecer conexión con sus aliados.
