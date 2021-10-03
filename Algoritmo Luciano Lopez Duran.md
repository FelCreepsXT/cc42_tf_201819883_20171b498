# Algoritmo A*

Durante el transcurso del proyecto me encargare de utilizar el algoritmo A*, ya que nos ayuda a detectar el camino mas corto como tambien a un tiempo estimado. Este algoritmo posee la logica de el coste unitario.

## Funcionalidad

El algoritmo tiene la funcionalidad de agregar en un arreglo todos los caminos posibles que este puede posseer. Luego, agregamos todos los caminos son agregados a una lista abierta. Además, cuando se agrega a la lista cerrada ningun nodo puede volver a recorrer el camino nuevamente. Dentro de esta lista realizamos un reordenamiento de los caminos partiendo del costo del **camino + tiempo**. Posterior a ello, obtenemos el primer valor el cual tiene el menor costo del camino. Al utilizar este camino nosotros debemos volver a realizar la busqueda de caminos asociados nuevamente, pero esta vez actualizando la lista, ya que el primer camino que escogimos paso una lista cerrada. Por ello, se debe volver a agregar los nuevos nodos respectivos a los que el nodo anterior se dirigia. Esta logica se usa durante todo el transcurso hasta encontrar el camino. Cuando un nodo llege al puntos destino no quiere decir que directamente nos devuelva el valor. Este debe seguir la logica que se establecio desde el inicio, ya que si bien puede haber encontrar el camino este debe esperar en la lista hasta que este se encuentre en la posicion 0 del arreglo de importancia.

## Diagrama de Flujo

[![flujo.png](https://i.postimg.cc/QxNj2B2g/flujo.png)](https://postimg.cc/F1qtcKs1)
