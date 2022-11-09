## PROCESOS DEL PRIMER PUNTO

![image](https://user-images.githubusercontent.com/90010884/200722968-92c9f5eb-c5c3-4931-86c9-c26748e7e095.png)
![image](https://user-images.githubusercontent.com/90010884/200723004-db4fae88-8916-4d91-b871-539a61a2c5e0.png)
![image](https://user-images.githubusercontent.com/90010884/200723018-57db3869-2a13-4356-8e8f-06125a8f7e71.png)
![image](https://user-images.githubusercontent.com/90010884/200723033-df923261-4594-4d87-9110-7c56c3c086de.png)
![image](https://user-images.githubusercontent.com/90010884/200723049-f1814419-60ff-4ce2-97cb-7296dbfe3bf7.png)
![image](https://user-images.githubusercontent.com/90010884/200723059-03624687-a759-427e-9363-9f0cc32818b6.png)
![image](https://user-images.githubusercontent.com/90010884/200723070-e743f333-9a30-4f5f-ba7b-b5376c0c0891.png)
![image](https://user-images.githubusercontent.com/90010884/200723082-25ebcb39-e3b6-4335-b150-416007185fb2.png)
![image](https://user-images.githubusercontent.com/90010884/200723099-2ff7b4a6-4c14-423a-b43e-f317dd07cf50.png)
![image](https://user-images.githubusercontent.com/90010884/200723113-cab562b6-d353-436d-96b1-57ed0b3b198d.png)
![image](https://user-images.githubusercontent.com/90010884/200723122-b3afb8b9-a63b-4e8c-bedb-dc3cb8a3a4ec.png)
![image](https://user-images.githubusercontent.com/90010884/200723129-91ba57f9-6892-407e-b793-02bf23562725.png)
![image](https://user-images.githubusercontent.com/90010884/200723140-bc2e1060-3ae9-47d7-ae0e-59fdfed5e9cd.png)
![image](https://user-images.githubusercontent.com/90010884/200723150-a97f80fb-6204-4f20-8241-c06b72812afb.png)
![image](https://user-images.githubusercontent.com/90010884/200723157-19f44f96-c5b8-42ad-8eed-0cb5d1fb38bf.png)
![image](https://user-images.githubusercontent.com/90010884/200723164-c2b0e25b-4775-4ee8-9d25-6202ee8971b4.png)
![image](https://user-images.githubusercontent.com/90010884/200723171-e24896fc-5fc3-463f-9e96-569e51e9909a.png)
![image](https://user-images.githubusercontent.com/90010884/200723182-07cb0bc8-db42-4fd8-a6e5-bd1b631272a2.png)
![image](https://user-images.githubusercontent.com/90010884/200723192-4f84b0b2-a3f1-4c75-a90c-e4f62c76bb92.png)
![image](https://user-images.githubusercontent.com/90010884/200723203-21d1ecd0-32e5-4661-b2b6-6f6677a3784f.png)
![image](https://user-images.githubusercontent.com/90010884/200723276-2c811dca-4642-4526-971b-f8d82854fb57.png)
![image](https://user-images.githubusercontent.com/90010884/200723283-51de6072-8456-42bd-9686-2c7b07da66b5.png)
![image](https://user-images.githubusercontent.com/90010884/200723296-046961c3-5e29-4389-8225-74b2e81f96b0.png)
![image](https://user-images.githubusercontent.com/90010884/200723304-f1d685bc-227f-4b44-bcb2-7ff9e545fa25.png)

1. ¿Cuántos y cuáles recursos crea Azure junto con la VM?
Se crean 4 recursos, los cuales son
* Resource Group
* Public and private IP address
* Virtual Machine
2. ¿Brevemente describa para qué sirve cada recurso?
* Resource Group: Es un contenedor que almacena recursos relacionados con una solucion de Azure. Puede incluir todos los recirsos de la solucion o solo los que se desean administrar
* Public and private IP address: las privadas permiten la comunicacion entre los recursos de azure, como interfaces de red de VM, equilibradores de carga o puertas de enlace de aplicaciones. Las publicas permiten a los recursos de internet la comunicacion entrante a los recursos de azure. Permiten que los recursos de Azure se comuniquen con los servicios de Azure orientados al publico e Internet
* Virtual Machine: Se puede ver como otro equipo fisico, como un portatil, un smartphone o un servidor. Tiene CPU, memoria, discos para almacenar los archivos y pueden conectarse a internet si es necesario.
3. ¿Al cerrar la conexión ssh con la VM, por qué se cae la aplicación que ejecutamos con el comando npm FibonacciApp.js? ¿Por qué debemos crear un Inbound port rule antes de acceder al servicio?
Si se cierra la conexion tambien se cortan todos los procesos que se estan ejecutando, se debe configurar para que sea con forever, puesto que por defecto se corre por el puerto 22 y los demas no son aceptados
4. Adjunte tabla de tiempos e interprete por qué la función tarda tando tiempo.
Adjunte imágen del consumo de CPU de la VM e interprete por qué la función consume esa cantidad de CPU.
Adjunte la imagen del resumen de la ejecución de Postman. Interprete:
Tiempos de ejecución de cada petición.
Si hubo fallos documentelos y explique.
Podemos ver las imagenes de cada ejecucion en la parte de superior, se generaron fallos donde se puede pensar que es porque el mensaje nunca se pudo responder o no sabia que responder a la peticion, en ultimo caso por temas de timeout
5. ¿Cuál es la diferencia entre los tamaños B2ms y B1ls (no solo busque especificaciones de infraestructura)?
La B1ls se puede considerar una maquina basica, pues los recursos son muy simples y se demora mas en manejar una peticion, por otro lado la B2ms tiene mas capacidad, tiene mayor facilidad y rapidez para procesar cosas, de igual manera tiene un mejor uso de los recursos y mayor cantidad de entradas
6. ¿Aumentar el tamaño de la VM es una buena solución en este escenario?, ¿Qué pasa con la FibonacciApp cuando cambiamos el tamaño de la VM?
Aumentando el tamaño de la maquina permite disminuir el tiempo que toma en procesar la informacion para encontrar un fibonacci
7. ¿Qué pasa con la infraestructura cuando cambia el tamaño de la VM? ¿Qué efectos negativos implica?
Principalmente se genera un aumento en el costo de los precios, puesto que necesita mas potencia para que las respuestas sean mas cortas.
8. ¿Hubo mejora en el consumo de CPU o en los tiempos de respuesta? Si/No ¿Por qué?
Sí se mejora el consumo de la CPU, ya que la maquina aprovecha mejor los recursos, con mayor eficiencia
9. Aumente la cantidad de ejecuciones paralelas del comando de postman a 4. ¿El comportamiento del sistema es porcentualmente mejor?

## PROCESOS DEL SEGUNDO PUNTO
