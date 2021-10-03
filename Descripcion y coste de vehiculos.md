# Costos de los vehiculos

Teniendo en cuenta que la logica de los vehiculos es que se ejecute de manera infitina, pero pare cuando se halla encontrado el camino mas cortor. Entonces, al momento de que el camino del primer vehiculo se dirige a un punto, pero luego tiene que volver a un punto que esta mas lejano. Entonces, lo mas conveniente es inicializar otro auto, pero con otro precio.

## Logica para costos para los vehiculos

- El costo para los kilometros seria entre un rango de 2 a 8
- El costo para el tiempo sera entre un rango de 1 a 9

**Acontinuacion se le mostrara una imagen referencia si se inicializa 20 autos**

[Captura1.jpg](https://postimg.cc/hhhnC1ct)

## Termina la ejecucion del programa

El costo total para hallar el recorrido seria hallando lo que recorrio un auto y lo que demoro

- costoTotal = costoKilometro * distancia + costoTiempo * tiempo
