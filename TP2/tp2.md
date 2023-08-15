# Trabajo Práctico N°2

# Docker

## Ejercicio 3

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled.png)

## Ejercicio 4

Cuando se ejecuta el comando **`docker run busybox`**, se intenta crear y ejecutar un contenedor utilizando la imagen de BusyBox. Sin embargo, en este caso, no se obtiene ningún resultado visible porque el contenedor se inicia, realiza una tarea muy breve y luego se detiene automáticamente. Esto sucede debido a la naturaleza efímera de los contenedores.

Cuando se ejecuta **`docker run busybox`**, el contenedor se inicia y ejecuta el programa predeterminado de BusyBox, que en este caso es simplemente un shell interactivo. Sin embargo, como no se está interactuando directamente con el contenedor a través de una terminal, el shell se inicia y se detiene inmediatamente después, lo que hace que parezca que no se obtuvo ningún resultado.

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%201.png)

En esta salida:

- **`CONTAINER ID`** es el ID único del contenedor.
- **`IMAGE`** es la imagen utilizada para crear el contenedor.
- **`COMMAND`** es el comando que se ejecutó dentro del contenedor.
- **`CREATED`** indica cuándo se creó el contenedor.
- **`STATUS`** muestra el estado actual del contenedor. En este caso, "Exited (0)" significa que el contenedor finalizó su ejecución con un código de salida 0, lo que indica que se detuvo exitosamente.
- **`NAMES`** es el nombre asignado automáticamente al contenedor.

## Ejercicio 5

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%202.png)

*El modo interactivo (**`-it`**) en Docker permite interactuar directamente con el contenedor a través de una terminal. Al usar esta combinación de opciones junto con el comando **`docker run`**, se está indicando que se desea acceder al interior del contenedor para ejecutar comandos y ver sus resultados en tiempo real.*

*El comando **`sh`** es el intérprete de comandos de shell en sistemas Unix y Unix-like.*

## Ejercicio 6

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%203.png)

## Ejercicio 7

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%204.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%205.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%206.png)

## Ejercicio 8

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%207.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%208.png)

## Ejercicio 10

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%209.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2010.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2011.png)

## Ejercicio 11

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2012.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2013.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2014.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2015.png)

El comando **`docker exec`** se utiliza para ejecutar comandos dentro de un contenedor en ejecución. En este caso, se está utilizando **`docker exec`** para conectarse al contenedor de PostgreSQL y luego ejecutar el cliente **`psql`** para interactuar con la base de datos PostgreSQL directamente desde la línea de comandos. Estos comandos permiten crear y gestionar una instancia de PostgreSQL en un contenedor Docker, y brindan la capacidad de interactuar con la base de datos tanto desde la línea de comandos como desde una herramienta de IDE.

## Ejercicio 12

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2016.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2017.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2018.png)

![Untitled](Trabajo%20Pra%CC%81ctico%20N%C2%B02%20e5debe9fe4e64165b6452947344a18f9/Untitled%2019.png)