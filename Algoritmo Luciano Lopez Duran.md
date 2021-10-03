# Algoritmo A*

Algoritmo A* es un algoritmo que tambien es conocido como el algoritmo de busqueda de primero el mejor. Su objetivo es encontrar el camino mas corto. Su funcion es la siguiente:

*f(n) = g(n) + h(n)*

g(n) representa la funcion del costo acumulado
h(n) representa la funcion del costo de la heuristica

Como dentro del proyecto debemos elaborar el camino menos costos con un menor tiempo de demora. Entonce, se tomara que h(n) como la **suposicion** de los caminos para poder determinar la heuristica y asi poder encontrar un recorrido menor. Esto se hara con los puntos finales de los lugares de entrega menos las posiciones inciales y asi asignar una h(n) a cada nodo. Por otra parte, g(n) tomara el valor del tiempo para poder priorizar el envio. Por ello, se decidio utilizar para el proyecto el algoritmo A*, ya que nos ayuda a detectar el camino mas corto como tambien a un tiempo estimado. Este algoritmo posee la logica de el coste unitario.

Este algoritmo tiene una complejidad de **O(n^2)**

## Funcionalidad

El algoritmo tiene la funcionalidad de agregar en un arreglo todos los caminos posibles que este puede posseer. Luego, agregamos todos los caminos son agregados a una lista abierta. Además, cuando se agrega a la lista cerrada ningun nodo puede volver a recorrer el camino nuevamente. Dentro de esta lista realizamos un reordenamiento de los caminos partiendo del costo del **camino + tiempo**. Posterior a ello, obtenemos el primer valor el cual tiene el menor costo del camino. Al utilizar este camino nosotros debemos volver a realizar la busqueda de caminos asociados nuevamente, pero esta vez actualizando la lista, ya que el primer camino que escogimos paso una lista cerrada. Por ello, se debe volver a agregar los nuevos nodos respectivos a los que el nodo anterior se dirigia. Esta logica se usa durante todo el transcurso hasta encontrar el camino. Cuando un nodo llege al puntos destino no quiere decir que directamente nos devuelva el valor. Este debe seguir la logica que se establecio desde el inicio, ya que si bien puede haber encontrar el camino este debe esperar en la lista hasta que este se encuentre en la posicion 0 del arreglo de importancia.


**

## Diagrama de Flujo

[![flujo.png](https://i.postimg.cc/QxNj2B2g/flujo.png)](https://postimg.cc/F1qtcKs1)


## Pseudocodigo con un solo recorrido Coste Uniforme

**¿Utilidad?** 

Su utilidad sera a futuro cuando se implemente con la heuristica y asi tener un algoritmo mas eficiente.

**Dato usado de ejemplo era:** 
G = [
    [[1,1],[2,1],[3,5]],
    [[0,1],[2,1],[3,1]],
    [[0,1],[1,1],[3,2]],
    [[0,5],[1,1],[2,2]]
]

### En primer lugar, debemos establecer nuestros datos iniciales
    n = size(G)
    visited = [False]*n
    parent = [None]*n
    stack = []
    stack.append([init, 0])
        
### En segundo lugar, debemos establecer un bluque y tomamos el primer elemento del array
           
    while stack:
        pos = stack[0][0]
        
        if pos == final:
            return        
            
### En tercer lugar, añadir los nodos cercanos al inicial y marcamos como visitado el nodo padre

        for i in range(len(G[pos])):
            if visited[G[pos][i][0]] == False:
                temp = G[pos][i][:]
                temp[1]= temp[1] + stack[0][1]
                stack.append(temp)
        visited[pos] = True
        
        stack.pop(0)
        
### Finalmente, ordenamos el arreglo y volvemos al buclque hasta que la posInicial = posFinal
        orderD(stack)

