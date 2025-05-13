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
