---
layout: post
title:  "introducción a python"
date:   2018-02-01 18:52:48 -0500
categories: jekyll update
---

**¿Que es Python?**

Es un lenguaje de programacion Orientado a Objetos, Programacion Imperativa, programacion funcional.

- Con una sintaxis sencilla de entender y aprender.
- Ampliamente utilizado en Ciencia e Ingenierias
- Multiples bibliotecas

Tipos Numerico

Disponemos de los tipos numericos y operaciones habituales.

```python
#Si no colocamos el print se ejecutara todo el codigo, pero al momento de vizualisar resultados solo se muestra la ultima linea.
5 + 1 - 4 * 3
4/2
4//3
```
    1

```python
#Colocando print() muestra el resultado de cada linea.
print(5 + 1 - 4 * 3)
print(4/2)
print(4//2)
```
    -6
    2.0
    2

Las divisiones por cero lanzan un error

```python
1/0
```
    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    <ipython-input-7-9e1622b385b6> in <module>()
    ----> 1 1/0


    ZeroDivisionError: division by zero

Numero Complejos

```python
(2+3j)
```
    (2+3j)

Valor Absoluto de numeros

```python
abs(-10)
```
    10

```python
(2+3j)*(1-5j)
```
    (17-7j)

Potencia

```python
2**2
```
    4

Convertir a entero

```python
int(3.1416)
```
    3

```python
round(3.1416)
```

    3

No puedo convertir complejos a numeros flotantes, python no reconoce la parte entera e imaginaria.

```python
float(3+1j)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-90-fb3327f662a4> in <module>()
    ----> 1 float(3+1j)


    TypeError: can't convert complex to float


La asignacion de variables funciona igual que en otros lenguajes


```python
a = 2**1
print(a)
```

    2



```python
a, b = 1, 2
print("el valor de a: ", a)
print("el valor de b: ", b)
```

    el valor de a:  1
    el valor de b:  2


Antes de continuar un detalle interesante sobre python es el Zen de Python.
Frases o ideas que los desarrolladores colocaron.


```python
import this
```

    The Zen of Python, by Tim Peters

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!


Operadores de Comparacion


```python
a , b , c = 1, 2, .05
```


```python
print(a > c)
print(a < c)
print(a == c)
print(a != c)
```

    True
    False
    False
    True


Recordemos que los numeros complejos no se pueden ordenar ;)


```python
a + 1j > 3 + 4j
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-103-9f4650de0cad> in <module>()
    ----> 1 a + 1j > 3 + 4j


    TypeError: '>' not supported between instances of 'complex' and 'complex'


Algunos tipos de Variables en Python son:

    -str (characteres)

    -list (Lista)

    -tuple (Secuencia de objetos inmutables)

    -dict (Diccionario)

    -int (Numero entero 1)

    -float (Numero flotante 1.0)

    -complex (Numero complejo 1+1j)

    -bool (Numero Boleano True o False)


```python
#Type;Funcion para saber el tipo de objeto
Numericas = 1.0
print(type(Numericas))

Numericas = 1
print(type(Numericas))

```

    <class 'float'>
    <class 'int'>



```python
#String
String = 'Hola Mundo'
type(String)
```




    str




```python
#Lista
lista = [1,2,3]
print(lista)
type(lista)
```

    [1, 2, 3]





    list




```python
#Tuple
tuple_0 = ('1', '2', 3)
print(tuple_0)
type(tuple_0)
```

    ('1', '2', 3)





    tuple




```python
lista == tuple_0
```




    False




```python
#Diccionarios
Diccionario = {'Nombre': 'Carlos', 'Edad' : 25}
print(Diccionario)
type(Diccionario)
```

    {'Nombre': 'Carlos', 'Edad': 25}





    dict




```python
#Operaciones con caracteres
Nombre = 'Carlos'
Nombre * 5
```




    'CarlosCarlosCarlosCarlosCarlos'



Listas

Python tiene muchos tipos de estructura de datos,una de ellas es la lista.
En algunos lenguajes de programación se las conocen como arreglos o matrices,
se caracterizan porque los elementos están entre corchetes y separados por una coma.

Una lista es una estructura de datos y un tipo de dato en python con características especiales.
Lo especial de las listas en Python es que nos permiten almacenar cualquier tipo de valor como enteros, cadenas y hasta otras funciones.


```python
lista = [1,2,'a','b']
print(lista)
```

    [1, 2, 'a', 'b']


Ver si un elemento se encuentra en una lista


```python
'a' in lista
```




    True




```python
lista = [1,4,'Python',[7,10],4]
```

Para accede a los datos de una lista:


```python
print(lista[0]) #El primer elemento de cualquier objeto es siempre 0.
print(lista[3]) #Es una lista que esta contenida en una lista
print(lista[3][1]) #Seleccion del elemento de la lista que vive en la lista.
#Para no estar esibiendo print para poder imprimir todos los elementos de un lista ocupamos un for
for elementos in lista:
    print(elementos)
print(lista)
```

    1
    [7, 10]
    10
    1
    4
    Python
    [7, 10]
    4
    [1, 4, 'Python', [7, 10], 4]


Metodos de las listas.

Los Metodos son funciones que se pueden realizar sobre los objetos, en este caso los metodos de las listas son los siguientes.


```python
#Metodos de las Listas.
lista.append(['nuevo_elemento',1,2]) #Agrega un elemento (puede ser una lista)
print("append: ", lista)

lista.extend([10,20,30]) #Agrega elemento la diferencia con append al momento de agregar una lista, cada elemento de esta lista se agrega como un elemento mas dentro de la otra lista.
print("extend: ", lista)

lista.remove(['nuevo_elemento',1,2]) #Elimina un elemento de la lista
print("remove: ", lista)

lista.index('Python')#Devuelve el numero del elemento que le pasemos

print("count: ", lista.count(4))  #Cuenta el numero de veces que se repite un elemento

lista.reverse()  #Invierte los elemenots
print("reverse : ", lista)

```

    append:  [1, 4, 'Python', [7, 10], 4, ['nuevo_elemento', 1, 2]]
    extend:  [1, 4, 'Python', [7, 10], 4, ['nuevo_elemento', 1, 2], 10, 20, 30]
    remove:  [1, 4, 'Python', [7, 10], 4, 10, 20, 30]
    count:  2
    reverse :  [30, 20, 10, 4, [7, 10], 'Python', 4, 1]


Funciones incorporadas en python a diferencia de los metodos nos permiten conocer y trabajar mejor los diferentes tipos de estructuras.

Se tiene precargadas un conjunto de funciones.


```python
type(lista) #Devuelve el tipo del objeto
str(lista) #Convierte elementos a cadenas
dir(lista) #Devuelve los metodos para un objeto
abs(-5) #Valor absoluto
complex(1,5) #Numeros complejos
divmod(10,2) #Toma dos numeros y devuelve una pareja de numeros, el primero es el cociente de los argumentos y el segundo su residuo.
eval('1+1') #Convierte el texto y lo evalua como codigo python.
len(lista) #Numero de elementos en un objeto.

#Existen mas funciones.
```




    8



Paquetes

Los paquetes son un conjunto de modulos, los modulos son archivos de codigo .py con variables, funciones y otros objetos.

En Python, cada uno de nuestros archivos .py se denominan módulos. Estos módulos, a la vez, pueden formar parte de paquetes.
Un paquete, es una carpeta que contiene archivos .py. Pero, para que una carpeta pueda ser considerada un paquete, debe contener un archivo de inicio llamado __init__.py. Este archivo, no necesita contener ninguna instrucción. De hecho, puede estar completamente vacío.

└── paquete
    ├── __init__.py
    ├── modulo1.py
    ├── modulo2.py
    └── modulo3.py
Los paquetes, a la vez, también pueden contener otros sub-paquetes:

└── paquete
    ├── __init__.py
    ├── modulo1.py
    └── subpaquete
        ├── __init__.py
        ├── modulo1.py
        └── modulo2.py
Y los módulos, no necesariamente, deben pertenecer a un paquete:

├── modulo1.py
└── paquete
    ├── __init__.py
    ├── modulo1.py
    └── subpaquete
        ├── __init__.py
        ├── modulo1.py
        └── modulo2.py

Numpy es un ejemplo de paquete en Python.

¿Que es Numpy?

Es una paqueteria de python, sirve para facilitar la manipulacion de vectores y matrices.

Motivacion para Usar numpy.

    -Lob bucles son costosos

    -Eliminar bucles, vectorizar operaciones

    -Los bucles se ejecutan en python, las operaciones vectorizadas en C

    -Las operaciones entre arrays de NumPy se realizan elemento a elemento.


```python
#Importacion de la paqueteria numpy
import numpy
```


```python
a = numpy.arange(5) + 4 #Crea un array de 5 numeros y a cada elemeto le suma 4
print(type(a))
print(a)
```

    <class 'numpy.ndarray'>
    [4 5 6 7 8]


Acceder a las funciones dentro de una paqueteria,la funcion norm se encuentra dentro del modulo linalg que se encuentra dentro de la paqueteria numpy. (De esta manera no traemos todas las funciones, teniendo implicaciones en la velocidad del codigo.)

La funcion norm, devuelve una de las ocho normas de matrices diferentes, o una de un número infinito de normas vectoriales.



```python
print(numpy.linalg.norm(a))
```

    13.784048752090222


Una Practica habitual para trabajar con los paquetes es renombrandolos de la ssiguiente manera.


```python
import numpy as np #Traemos numpy y lo llamamos np
```


```python
print(np.linalg.norm(a))
```

    13.784048752090222



```python
np.e
np.pi
np.log(2)
```




    0.6931471805599453



Se puede renombrar tambien todo un modulo dentro de una paqueteria, de la siguiente manera.


```python
from numpy import linalg as LA
```


```python
print(LA.norm(a))
```

    13.784048752090222


Arrays de NumPy

¿Que es un Array?

Una de las estructuras de datos más fundamentales en cualquier idioma es el arrays (matriz).

Python no tiene una estructura de datos de matriz nativa, pero tiene una lista que es mucho más general y se puede usar como un arrays (matriz), multidimensional con bastante facilidad.



```python
a = np.array([1,2,3,4]) #Los elementos son homogeneos
print(a)
```

    [1 2 3 4]



```python
a = np.array([1,2,"3"])  #Convierte todos en un mismo tipo
print(a)
a = np.array([1,2,"3"], dtype=float) #Forzo que todos tengan un tipo de elemento indicado
print(a)
```

    ['1' '2' '3']
    [1. 2. 3.]


Ventajas de trabajar con arrays y paquetes.

Sumaremos dos matrices (b y c) almacenando los resultados en una tercer matriz llamada a

Y veremos el tiempo que toma hacerlo de dos maneras diferentes


```python
#Definicion de las matrices a,b y c

N, M = 100, 100
a = np.empty(10000).reshape(N,M)
b = np.random.rand(10000).reshape(N,M)
c = np.random.rand(10000).reshape(N,M)
```


```python
%%timeit #Mide el tiempo que tarda en ejecutar el codigo
#Suma elemento a elemento
for i in range(N):
    for j in range(M):
        a[i,j] = b[i,j] + c[i,j]
```

    5.33 ms ± 91.2 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)



```python
%%timeit
a = b + c #Esta operacion se realiza elemento a elemento y se encuentra mas optimizado.
```

    5.88 µs ± 305 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)


Indexacion y seleccion en arrays.

Una de las herramientas mas importantes al momento de trabajar con arrays es la indexacion. Consiste en seleecionar elementos aislados o secciones de un array. Vamos a ver la indexacion basica.


```python
a = np.array([
    [1,2,3],
    [2,4,6]])
a
```




    array([[1, 2, 3],
           [2, 4, 6]])




```python
a[0]
```




    array([1, 2, 3])




```python
a[0][0]
```




    1




```python
a[0, 0]
```




    1




```python
a[0:2, 1:3] #No se toma en cuenta el ultimo elemento
```




    array([[2, 3],
           [4, 6]])




```python
a[:, 1:3]
```




    array([[2, 3],
           [4, 6]])




```python
a[0, 0:3:2] #Tomo los elementos que se encuentren en una posicion par.
```




    array([1, 3])




```python
a[0, ::2] #Es la misma forma de solo tomar los elementos de posiciones pares
```




    array([1, 3])
