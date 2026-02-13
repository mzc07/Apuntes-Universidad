- Variables = _espacio en la memoria a la que se le asigna un valor._
### Tipos de datos
- Enteros
- Float
- Caracteres
- Booleanos


- **Vector (Array)** Indice que describe posicion donde se almacena un elemento. Guarda varios elementos de un mismo tipo. Tiene un numero definido de elementos.
- Los elementos son fijos. Estan guardados en memoria de forma secuencial.
$$N-1$$
- **Matriz** Array de Arrays. Arreglo bidimensional $M \times N$. Mismo tipo  de datos.

## Representacion de Listas
- Para cualquier lista, excepto para la nula, se dice que $a_{i+1}$ es sucesor de $a_i$ donde $(i < N)$ y que $a_{i-1}$ es predecesor de $a_i$ done $(i>1)$.
- No se define ni el predecesor de $a_1$ ni el sucesor de $a_N.$
- La posicion del elemento $a_i$ en una lista es $i$
> **Pointer** Es un valor a nivel de registros del disco duro  que me ndica en donde empieza un valor o una variable.

- La posicion es la inmediata a la del elemento anterior.
- Una lista termina cuando el apuntador apunta a un valor nulo (No hay elemento siguiente al cual apuntar).

La representacion grafica mas extendida  es aquella que utiliza una caja con dos secciones en su interior. En la primera seccion se escribe el elemento y en la segunda el indice.

$$
[a_1] \mapsto [a_2] \mapsto [a_3] \mapsto ... \mapsto [a_n]
$$

### Representacion de listas

```
struct Nodo
{
	int dato;
	Nodo *siguiente;
}
```
- El elemento puede ser de cualquier tipo.
- Guarda la direccion del siguiente nodo o elemento de la lista.
### P.O.O
- Clases
- Objetos
$Clase 1 \rightarrow Atributos \rightarrow Metodos(Funciones)$

#### Carro
- Motor
- #. de llantas
- Puertas
- Color
- Placa
- Cilindraje
- Marca
- **encender()**
- **frenar()**
- **cambio_marcha()**
- **acelerar()**

#### Objeto: Camioneta
##### Atributos
- Motor V6
- 4 llantas
- 5 puertas
- Color fucsia
- Placa: "ABC-123"
- Cilindraje: 12.8
- Toyota
##### Metodos
- **encender()**
- **frenar()**
- **cambio_marcha()**
- **acelerar()

- Herencia: La clase carro puede tener subclases que pueden heredar algunas caracteristicas o funciones.
- Polimorfismo: Cuando una clase u objeto tiene comportamientos anormales sin cambiar su estructura.
- Encapsulamiento



## Tipos de listas
- Listas simplemente enlazadas: Cada nodo contiene un unico enlace que conecta ese nodo.
- Listas doblemente enlazadas: La lista tiene dos apuntadores, uno a su nodo predecesor y el otro a su sucesor. Eficiente en recorrido directo e inverso. Un nodo apunta hacia el elemento inmediatamente anterior y el inmediatamente posterior.
- Lista circular simplemente enlazada: Lista enlazada simplemente en la que el ultimo elemento se enlaza al primer elemento de tal forma que la lista puede ser recorrida de modo circular.
- Lista circular doblemente enlazada: Puede recorrir directa e inversamente y recorrerse de modo circular.


### Lista: A
$$
[A|B^*] \rightarrow [B|C^*] \rightarrow [C|\textbf{NULL}]
$$
1. _Inicio_ 
$$[X|A*]$$
2. _Final_
		Iteramos sobre la lista hasta encontrar un elemento que no apunte a otro y se inserta.
			$[X|\textbf{NULL}]$
		