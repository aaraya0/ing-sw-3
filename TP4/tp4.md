# Trabajo Práctico N°4

## Ejercicio 1

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%201.png)

## Ejercicio 2

Estos son los contenedores creados al ejecutar docker-compose.yml

1. front-end
2. edge-router
3. catalogue
4. catalogue-db
5. carts
6. carts-db
7. orders
8. orders-db
9. shipping
10. queue-master
11. rabbitmq
12. payment
13. user
14. user-db
15. user-sim

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%202.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%203.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%204.png)

**Endpoints:** 

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%205.png)

---

*¿Por qué cree usted que se está utilizando repositorios separados para el código y/o la configuración del sistema? Explique puntos a favor y en contra.*

**Ventajas:**

1. **Separación de Preocupaciones:** Tener repositorios separados permite una clara separación entre el código de la aplicación y la configuración del sistema. Esto facilita la gestión y el mantenimiento de ambos aspectos de la aplicación de forma independiente.
2. **Gestión de Versiones:** Los cambios en el código y en la configuración del sistema a menudo tienen ciclos de vida diferentes. Tener repositorios separados permite gestionar las versiones de manera más específica y adecuada para cada componente.
3. **Colaboración más Fácil:** Diferentes equipos pueden trabajar en el código y la configuración de forma simultánea sin interferir entre sí. Esto mejora la colaboración y permite a los equipos especializarse en sus respectivas áreas.
4. **Automatización y Despliegue Continuo:** Al separar la configuración del sistema, se puede automatizar el proceso de implementación y configuración. Esto facilita la adopción de prácticas de despliegue continuo y orquestación de infraestructura.
5. **Mayor Flexibilidad en Despliegue:** Al tener la configuración separada, es más fácil ajustar y cambiar la infraestructura subyacente o los recursos sin necesariamente cambiar el código de la aplicación. Esto facilita la adaptación a cambios en la demanda o requisitos.

**Desventajas:**

1. **Complejidad Adicional:** Gestionar múltiples repositorios puede aumentar la complejidad, especialmente para equipos pequeños o proyectos menos sofisticados.
2. **Sincronización:** Es importante mantener sincronizados los cambios en el código y en la configuración para asegurarse de que funcionen bien juntos. Esto puede requerir un esfuerzo adicional.
3. **Dificultad en el Descubrimiento:** Para los nuevos miembros del equipo, puede ser complicado descubrir dónde se encuentra la configuración relevante, lo que podría llevar a retrasos y confusiones.
4. **Posible Desalineación:** Si los cambios en la configuración y el código no se coordinan adecuadamente, podría surgir una desalineación entre ambos, lo que podría causar problemas de compatibilidad.
5. **Mayor Complejidad en la Implementación Local:** Durante el desarrollo local o las pruebas, gestionar y mantener ambos repositorios puede requerir esfuerzo adicional y puede ser un proceso más complejo.

---

*¿Cuál contenedor hace las veces de API Gateway?*

El contenedor que hace de API Gateway es edge-router. El repositorio que corresponde a este contenedor tiene un archivo traefik.toml. Traefik es un *Edge Router*; esto significa que es la **puerta a la plataforma**. Se encarga de *interceptar* cada petición que se realiza y enrutarla al servicio correcto. Traefik sabe la lógica y las reglas que determinan qué servicio es el encargado de gestionar cada petición.

---

*¿Cuál de todos los servicios está procesando la operación?*

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%206.png)

El servicio de **user** realiza la operación y se comunica con el **front-end.**

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%207.png)

*¿Cuál de todos los servicios está procesando la operación?*

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%208.png)

El servicio de **catalogue** realiza la operación y se comunica con el **front-end.**

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%209.png)

*¿Cuál de todos los servicios está procesando la operación?*

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%2010.png)

El servicio de **catalogue** realiza la operación y se comunica con el **front-end.**

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%2011.png)

---

*¿Como perisisten los datos los servicios?*

**Volúmenes de Docker:** Los volúmenes son una forma de persistir datos en Docker. Los volúmenes son directorios o archivos que están fuera del sistema de archivos del contenedor y se montan en el contenedor. Esto permite que los datos persistan incluso cuando el contenedor se detiene o se elimina. Los volúmenes pueden ser administrados por Docker y pueden compartirse entre varios contenedores.

Los servicios que deben almacenar datos, en este caso, user-db y catalogue-db, tienen creados volúmenes de Docker para la persistencia de datos.

Dockerfile de user-db: 

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%2012.png)

**VOLUME /data/db-users:**

Declara /data/db-users como un volumen. *Los volúmenes en Docker son puntos de montaje que pueden persistir datos incluso después de que el contenedor se detenga o se elimine.*

---

*¿Cuál es el componente encargado del procesamiento de la cola de mensajes?*

El componente encargado del procesamiento de la cola de mensajes es el servicio llamado **`queue-master`**

---

*¿Qué tipo de interfaz utilizan estos microservicios para comunicarse?*

Estos microservicios utilizan principalmente comunicación basada en **HTTP/HTTPS** para interactuar entre sí. Esto se logra a través de interfaces API expuestas por los servicios que permiten a otros microservicios realizar solicitudes HTTP a rutas específicas para obtener o enviar datos.

Por ejemplo:

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B04%2044b3218197eb431ea5ed13bd0dde5ec9/Untitled%2013.png)