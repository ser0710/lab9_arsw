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

![image](https://user-images.githubusercontent.com/90010884/200987095-3b795dd5-eb43-4a6d-bf67-18b421ee29e3.png)
![image](https://user-images.githubusercontent.com/90010884/200987183-db618823-41d1-4519-a15f-1ebd9726b160.png)
![image](https://user-images.githubusercontent.com/90010884/200987207-585da2ab-f399-4b07-925f-b4d6abd12ace.png)
![image](https://user-images.githubusercontent.com/90010884/200987214-851b4b23-31e6-45d7-b834-a2fb43db661e.png)
![image](https://user-images.githubusercontent.com/90010884/200987221-e4e2b1f4-26d8-4719-9e2b-8f83dc8b0328.png)
![image](https://user-images.githubusercontent.com/90010884/200987237-eca2b1d1-70a8-4cbe-b66b-6a022e0135d1.png)
![image](https://user-images.githubusercontent.com/90010884/200987249-459f2f0e-466a-4bc1-80a8-9694594f28bb.png)


1. ¿Cuáles son los tipos de balanceadores de carga en Azure y en qué se diferencian?, ¿Qué es SKU, qué tipos hay y en qué se diferencian?, ¿Por qué el balanceador de carga necesita una IP pública?
Existe el balanceador publico y el privado. El primero proporciona conexiones de salida para maquinas virtuales en una red virtual. Esto mediante traducciones de sus IP privadas a IP publicas. La otra necesita direcciones IP privadas solo en el front, estos se usan para equilibrar el trafico dentro de una red virtual.

Las SKU son una combinacion de maquinas virtuales y una especificacion de de hardware determinada.
Tipos:
* Dadsv5
  * Tipo 1: usa procesador EPYC 7763v de AMD, ofrece 64 nucleos fisicos, 112 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dadsv5
* Dasv5
  * Tipo 1: usa procesador EPYC 7763v de AMD, ofrece 64 nucleos fisicos, 112 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dasv5
* Dasv4
  * Tipo 1: usa procesador EPYC 7452 de 2,35 GHz de AMD, ofrece 64 nucleos fisicos, 96 vCPU y 672 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dasv4
  * Tipo 2: usa procesador EPYC 7763v de AMD, ofrece 64 nucleos fisicos, 112 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dasv4
* DCadsv5
  * Tipo 1: usa procesador EPYC 7763v de AMD 3ra generacion, ofrece 64 nucleos fisicos, 112 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie DCadsv5
* DCasv5 
  * Tipo 1: usa procesador EPYC 7763v de AMD de 3ra generacion, ofrece 64 nucleos fisicos, 112 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie DCasv5
* DCSv3 
  * Tipo 1: usa procesador escalable Intel Xeon 8370C de 3ra generacion, ofrece 48 nucleos fisicos, 48 vCPU y 384 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie DCsv3
* DCdsv3
  * Tipo 1: usa procesador escalable Intel Xeon 8370C de 3ra generacion, ofrece 48 nucleos fisicos, 48 vCPU y 384 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie DCdsv3
* DCsv2
  * Tipo 1: usa procesador Intel Coffee Lake, ofrece 8 nucleos fisicos, 8 vCPU y 64 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie DCsv2
* Ddsv5
  * Tipo 1: usa procesador Intel Ice Lake, ofrece 64 nucleos fisicos, 119 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Ddsv5
* Ddsv4
  * Tipo 1: usa procesador Intel Cascade Lake, ofrece 52 nucleos fisicos, 80 vCPU y 504 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Ddsv4
  * Tipo 2: usa procesador Intel Ice Lake, ofrece 64 nucleos fisicos, 119 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Ddsv5.
* Dsv5
  * Tipo 1: usa procesador Intel Ice Lake, ofrece 64 nucleos fisicos, 119 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dsv5
* Dsv4
  * Tipo 1: usa procesador Intel Cascade Lake, ofrece 52 nucleos fisicos, 80 vCPU y 504 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dsv4
  * Tipo 2: usa procesador Intel Ice Lake, ofrece 64 nucleos fisicos, 119 vCPU y 768 GiB de RAM. Este tipo ejecuta maquinas virtuales de la serie Dsv4

2. ¿Cuál es el propósito del Backend Pool?
Es un componente escencial del equilibrador de carga, este define el grupo de recursos que atenderan el trafico de una regla de equilibrio. la configuracion puede ser por:
* Tarjeta de interfaz de red 
* Direccion IP
3. ¿Cuál es el propósito del Health Probe?
Ayuda a detectar los estados de los endpoints, la configuracion del Health Probe permite determinar cual backend pool sera recibido en la nueva conexion, detectan fallos de la aplicacion, nos ayuda con el control de flujo para administrar la carga. Si este falla el balanceador dejara de enviar conexiones a las respectivas instancias en mal estado
4. ¿Cuál es el propósito de la Load Balancing Rule? ¿Qué tipos de sesión persistente existen, por qué esto es importante y cómo puede afectar la escalabilidad del sistema?.
Permite definir como se distribuye el trafico de todas las instancias dentro del backend pool. Asigna una direccion IP y un front determinado a varias direcciones IP y puerto del Back.
Las sesiones existentes son:
* None: Las solicitudes sucesivas del mismo cliente pueden ser manejadas por cualquier maquina virtual
* Client IP: Las solicitudes sucesivas de la misma IP del cliente seran manejadas por la misma maquina virtual
* Client IP and Protocol: Las soilicitudes de la misma combinacion de protocolo y direccion IP del cliente seran manejadas por la misma maquina virtual
5. ¿Qué es una Virtual Network? ¿Qué es una Subnet? ¿Para qué sirven los address space y address range?
Es el bloque fundamental de una red privada en azure. Permite muchos tipos de recursos como las maquinas virtuales, para poder comunicarse de forma segura entre usuarios, con internet y con redes locales.

La subnet es una red dentro de una red, las subredes hacen que las redes sean mas eficientes. Con esto el trafico de la red puede recorrer una distancia mas corta sin tener que pasar por routers innecesarios

Address Space: Conjunto de direcciones de memoria virtual que puede utilizar. El espacio de direcciones es privado para todos los procesos a menos que se comparta

Address Range: Son los rangos de direcciones de redes privadas

6. ¿Qué son las Availability Zone y por qué seleccionamos 3 diferentes zonas?. ¿Qué significa que una IP sea zone-redundant?
Son data centers separados de forma fisica y logica con su propia fuente de electricidad, conectividad y sistema de enfriamiento. Seleccionamos las 3 puesto que esto nos ayuda a aumentar la disponibilidad y resistencia de las aplicaciones con el respaldo de un SLA con un tiempo de actividad de 99.99% para VM. Tambien habilita la escalabilidad avanzada para las aplicaciones que admiten el escalado activo-activo multisitio. Por ultimo mejora el RTO y RPO
7. ¿Cuál es el propósito del Network Security Group?
Es un firewall a nivel de red con un conjunto de reglas que gestiona permitiendo o denegando el trafico de red, tando de entrada como de salida a los recursos de azure
8. Informe de newman 1 (Punto 2)
9. Presente el Diagrama de Despliegue de la solución.

