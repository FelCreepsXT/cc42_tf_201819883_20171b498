
## Descripcion
 En un primer lugar la funcion pide como parametros a los  de los csv ya definidos, luego los almacena en listas creadas, para luego entrar en creacion de otras dos listas,
 las cuales seran de visitados, para saber si un nodo de los puntos de entrega ya fue visto, y de prosimos movimientos que mostrara los proximos lugares a donde podra ir 
 el camion (esta restringido en 5), si en caso todas las opciones de movimiento son invalidas debido a no encontrar nuevos puntos o encontrarlos ocupados, regresara al
 al punto anterior , siendo el peor de los casos que regrese al almacen haciendo el retroceso en otro camino ya definido
## Algoritmo

Funcion VRP(PI Por Referencia, PF Por Referencia)
	Dimension Almacenes[0]
	Dimension Entregas[0]
	Almacenes <- PI
	Entregas <- PF
	n <- longitud(Almacenes[])
	Dimension Visitados[0]
	Dimension Rango_mov[2]
	Repetir
		Para i<-0 Hasta n Con Paso 1 Hacer
			Rango_mov[1] <- Almacenes[i]+5
			Rango_mov[2] <- Almacenes[i]-5
			Para j<-0 Hasta 1 Con Paso 1 Hacer
				Almacenes[i]<-Almacenes[i] + Rango_mov[j]
				Para Q<-0 Hasta Longitud(Visitados[]) Con Paso 1 Hacer
					
				Fin Para
			Fin Para
		Fin Para
	Hasta Que Entregas[] = Visitados[]
	
FinFuncion
