# 📋 Nota:

Mi propósito con este curso de Python es empezar desde lo más básico, para que quienes se inician en el campo puedan adquirir sus primeros conocimientos y avanzar hasta desarrollar sus propios proyectos. Siempre es valioso repasar las bases, y en el proceso, uno termina aprendiendo algo nuevo.

---

# Python

## Características

* Múltiples usos
* Alto nivel
* Tipado dinámico
* Orientado a objetos
* Interpretado

## Historia

Puedes encontrar más sobre la historia de Python en [Wikipedia](https://en.wikipedia.org/wiki/History_of_Python)

## Instalación

Descarga Python desde su [Sitio Web Oficial](https://www.python.org/)

### **Ejecución y compilación de un programa con Python**

Python es un **lenguaje interpretado**, no se compila como C o Java. El código se ejecuta línea por línea usando el **intérprete de Python**.

**Cómo ejecutar un programa:**

1.  Crear un archivo con extensión `.py`, por ejemplo: `mi_programa.py`
2.  Ejecutarlo desde la terminal:

    ```bash
    python mi_programa.py
    ```

---

### **Variables en Python**

Una variable es un espacio donde guardamos un dato para usarlo después.

```python
nombre = "Wilfrido" #
edad = 30
altura = 1.75
````

  * No necesitas declarar el tipo.
  * El tipo se asigna automáticamente según el valor.

-----

### **Manipulación de cadenas de caracteres**

Una cadena (string) es un texto entre comillas. Puedes hacer muchas operaciones:

```python
mensaje = "Hola Mundo"
print(mensaje.upper())      # HOLA MUNDO
print(mensaje.lower())      # hola mundo
print(len(mensaje))         # 10
print(mensaje[0])           # H
print(mensaje[-1])          # o
print(mensaje[0:4])         # Hola
```

También puedes concatenar:

```python
nombre = "Wilfrido" #
saludo = "Hola " + nombre
print(saludo)  # Hola Wilfrido #
```

-----

### **Palabras reservadas**

Son palabras que **no puedes usar como nombres de variables** porque tienen un significado especial en Python.

Ejemplos:

```python
if, else, for, while, def, return, import, class, try, except, True, False
```

⚠️ **No puedes hacer esto:**

```python
def = 5   # ❌ Error
```

-----

### **Operadores aritméticos**

Sirven para hacer operaciones matemáticas:

```python
a = 10
b = 3

print(a + b)  # Suma → 13
print(a - b)  # Resta → 7
print(a * b)  # Multiplicación → 30
print(a / b)  # División (float) → 3.333...
print(a // b) # División entera → 3
print(a % b)  # Módulo (residuo) → 1
print(a ** b) # Potencia → 1000
```

-----

### **Comentarios en Python**

Son líneas que no se ejecutan, sirven para explicar el código.

```python
# Esto es un comentario de una línea

"""
Esto es un comentario
de varias líneas (docstring)
"""
```

-----

### **Tipos de datos**

Python tiene varios tipos de datos:

```python
entero = 10            # int
decimal = 3.14         # float
texto = "Hola"         # str
booleano = True        # bool
lista = [1, 2, 3]      # list
tupla = (1, 2, 3)      # tuple
diccionario = {"a":1}  # dict
```

Puedes ver el tipo con `type()`:

```python
print(type(entero))  # <class 'int'>
```

-----

### **Entrada de datos desde el teclado**

Usamos la función `input()`:

```python
nombre = input("¿Cuál es tu nombre? ")
print("Hola, " + nombre)
```

Todo lo que se ingresa con `input()` es **texto (str)**. Si quieres un número:

```python
edad = int(input("¿Cuántos años tienes? "))
```

-----

### **Sentencias condicionales `if`**

Permiten tomar decisiones:

```python
edad = int(input("¿Qué edad tienes? "))

if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")
```

También puedes usar `elif` (else if):

```python
nota = 85

if nota >= 90:
    print("Excelente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Reprobado")
```

-----

### **Sentencias condicionales `if else`**

Permiten ejecutar una acción si se cumple una condición (`if`), y otra si no se cumple (`else`).

```python
edad = 17

if edad >= 18:
    print("Puedes votar")
else:
    print("Aún no puedes votar")
```

-----

### **Sentencias condicionales `elif`**

Se usa cuando hay **más de dos condiciones** posibles. Es una combinación de `if` y `else`.

```python
nota = 85

if nota >= 90:
    print("Excelente")
elif nota >= 70:
    print("Aprobado")
else:
    print("Reprobado")
```

-----

### **Sentencias anidadas**

Es cuando se coloca un `if` dentro de otro `if`.

```python
edad = 20
nacionalidad = "costarricense"

if edad >= 18:
    if nacionalidad == "costarricense":
        print("Puede votar en Costa Rica")
    else:
        print("No es costarricense")
else:
    print("Es menor de edad")
```

-----

### **Operadores relacionales**

Se usan para comparar valores. Devuelven `True` o `False`.

| Operador | Significado       |
| -------- | ----------------- |
| `==`     | Igual             |
| `!=`     | Distinto          |
| `>`      | Mayor que         |
| `<`      | Menor que         |
| `>=`     | Mayor o igual que |
| `<=`     | Menor o igual que |

```python
print(5 == 5)  # True
print(3 != 4)  # True
print(10 > 8)  # True
```

-----

### **Operadores lógicos**

Permiten combinar varias condiciones:

| Operador | Significado             |
| -------- | ----------------------- |
| `and`    | Y (ambas verdaderas)    |
| `or`     | O (una verdadera)       |
| `not`    | No (niega la condición) |

```python
edad = 25
ciudad = "San José"

if edad >= 18 and ciudad == "San José":
    print("Puede registrarse")

if edad < 18 or ciudad != "San José":
    print("No cumple los requisitos")

if not edad < 18:
    print("Es mayor de edad")
```

-----

### **Operadores de asignación**

Sirven para asignar o actualizar valores en una variable.

```python
x = 5       # Asignación
x += 2      # Suma acumulativa → x = x + 2
x -= 1      # Resta acumulativa
x *= 3      # Multiplicación acumulativa
x /= 2      # División acumulativa
```

-----

### **Parámetros `end` y `sep`**

Se usan en la función `print()` para **modificar el final de línea** (`end`) o el **separador** entre elementos (`sep`).

```python
# end evita el salto de línea
print("Hola", end=" ")
print("Mundo")  # Resultado: Hola Mundo

# sep cambia el separador entre palabras
print("Python", "es", "genial", sep="-")  # Resultado: Python-es-genial
```

-----

### **Bucle o ciclo `while`**

Ejecuta un bloque de código **mientras** una condición sea verdadera.

```python
contador = 1

while contador <= 5:
    print("Número:", contador)
    contador += 1
```

⚠️ **Cuidado:** si la condición nunca cambia a `False`, el bucle será infinito.

-----

### **Sentencias `continue` y `break`**

  * `continue`: salta a la siguiente iteración.
  * `break`: termina el ciclo.

<!-- end list -->

```python
# Ejemplo de continue
for i in range(1, 6):
    if i == 3:
        continue
    print(i)  # Imprime: 1, 2, 4, 5

# Ejemplo de break
for i in range(1, 6):
    if i == 4:
        break
    print(i)  # Imprime: 1, 2, 3
```

-----

### **Función `len()`**

Devuelve la **longitud (cantidad de elementos)** de una cadena, lista, tupla, etc.

```python
texto = "Python"
print(len(texto))  # 6

lista = [1, 2, 3, 4]
print(len(lista))  # 4
```

-----

### **Concatenación con `format()`**

Permite insertar variables en una cadena usando llaves `{}`.

```python
nombre = "Wilfrido" #
edad = 30

mensaje = "Hola, mi nombre es {} y tengo {} años".format(nombre, edad)
print(mensaje)
```

También se puede usar por posición o nombre:

```python
mensaje = "Hola, {0}. Tienes {1} años.".format(nombre, edad)
mensaje = "Hola, {n}. Tienes {e} años.".format(n=nombre, e=edad)
```

-----

### **Concatenación con `f-strings`**

Forma más moderna y legible (Python 3.6+).

```python
nombre = "Wilfrido" #
edad = 30

mensaje = f"Hola, mi nombre es {nombre} y tengo {edad} años"
print(mensaje)
```

-----

### **Método `strip()`**

Elimina espacios en blanco **al inicio y final** de una cadena.

```python
texto = "  Hola mundo  "
print(texto.strip())  # "Hola mundo"
```

-----

### **Métodos `rstrip()` y `lstrip()`**

  * `rstrip()`: elimina espacios solo al final.
  * `lstrip()`: elimina espacios solo al inicio.

<!-- end list -->

```python
texto = "  Hola mundo  "
print(texto.rstrip())  # "  Hola mundo"
print(texto.lstrip())  # "Hola mundo  "
```

-----

### **Métodos `istitle()` y `title()`**

  * `istitle()`: verifica si cada palabra inicia con mayúscula.
  * `title()`: convierte una cadena para que cada palabra inicie con mayúscula.

<!-- end list -->

```python
frase = "Hola Mundo"
print(frase.istitle())  # True

frase2 = "hola mundo"
print(frase2.title())   # "Hola Mundo"
```

-----

### **Métodos `islower()`, `lower()`, `isupper()`, `upper()`**

  * `lower()`: convierte a minúsculas.
  * `islower()`: verifica si todo está en minúscula.
  * `upper()`: convierte a mayúsculas.
  * `isupper()`: verifica si todo está en mayúscula.

<!-- end list -->

```python
texto = "Hola"

print(texto.lower())     # "hola"
print(texto.islower())   # False
print(texto.upper())     # "HOLA"
print(texto.isupper())   # False
```

-----

### **Método `swapcase()`**

Invierte mayúsculas por minúsculas y viceversa.

```python
texto = "Hola Mundo"
print(texto.swapcase())  # "hOLA mUNDO"
```

-----

### **Método `capitalize()`**

Convierte solo la **primera letra** del texto en mayúscula.

```python
texto = "hola mundo"
print(texto.capitalize())  # "Hola mundo"
```

-----

### **Métodos `center()`, `ljust()`, `rjust()`**

Permiten **alinear texto** agregando espacios (o caracteres personalizados).

```python
texto = "Python"

print(texto.center(10))     # "  Python  "
print(texto.center(10, "*"))# "**Python**"

print(texto.ljust(10))      # "Python    "
print(texto.rjust(10))      # "    Python"
```

-----

### **Método `count()`**

Cuenta cuántas veces aparece un **carácter o palabra** dentro de la cadena.

```python
frase = "Hola mundo mundo"
print(frase.count("mundo"))  # 2
print(frase.count("o"))      # 3
```

-----

### **Método `startswith()` y `endswith()`**

Verifican si una cadena **comienza** o **termina** con un texto específico. Devuelven `True` o `False`.

```python
texto = "Hola mundo"

print(texto.startswith("Hola"))  # True
print(texto.endswith("mundo"))   # True
```

-----

### **Substrings**

Un **substring** es una **parte** de una cadena, que se puede obtener usando **slicing** (rebanado).

```python
texto = "Python es genial"

print(texto[0:6])    # "Python"
print(texto[7:9])    # "es"
print(texto[-6:])    # "genial"
```

-----

### **Ciclo o bucle `for`**

Se usa para **iterar** (recorrer) elementos de una lista, cadena u otra colección.

```python
for letra in "Python":
    print(letra)

frutas = ["manzana", "pera", "uva"]
for fruta in frutas:
    print(fruta)
```

-----

### **Clase `range()`**

Genera una secuencia de números, útil en bucles `for`.

```python
for i in range(5):
    print(i)  # Imprime del 0 al 4

for i in range(1, 6):
    print(i)  # Imprime del 1 al 5

for i in range(0, 10, 2):
    print(i)  # Imprime 0, 2, 4, 6, 8
```

-----

### **Listas**

Una lista es una colección **ordenada y modificable** de elementos.

```python
numeros = [1, 2, 3, 4]
nombres = ["Ana", "Luis", "Carlos"]
mixta = [1, "texto", 3.14]
```

-----

### **Acceder a los elementos de una lista**

Los elementos se acceden por su índice, empezando en `0`.

```python
frutas = ["manzana", "pera", "uva"]

print(frutas[0])   # "manzana"
print(frutas[-1])  # "uva" (último elemento)
```

-----

### **Modificar elementos de una lista**

Puedes cambiar el valor de un elemento asignando uno nuevo a su índice.

```python
frutas = ["manzana", "pera", "uva"]
frutas[1] = "mango"
print(frutas)  # ["manzana", "mango", "uva"]
```

-----

### **Agregar elementos a una lista – `append()`**

Agrega un **elemento al final** de la lista.

```python
numeros = [1, 2, 3]
numeros.append(4)
print(numeros)  # [1, 2, 3, 4]
```

-----

### **Insertar elementos a una lista – `insert()`**

Agrega un elemento en **una posición específica**.

```python
nombres = ["Ana", "Luis", "Carlos"]
nombres.insert(1, "Pedro")
print(nombres)  # ["Ana", "Pedro", "Luis", "Carlos"]
```

-----

### **Eliminar elementos de una lista – `pop()`**

Elimina un elemento según su posición. Si no se especifica el índice, elimina el **último**.

```python
colores = ["rojo", "verde", "azul"]
colores.pop(1)       # Elimina "verde"
print(colores)       # ["rojo", "azul"]

colores.pop()        # Elimina "azul"
print(colores)       # ["rojo"]
```

-----

### **Eliminar elementos de una lista – `remove()`**

Elimina un **elemento específico** (por valor, no por índice). Si el valor no existe, da error.

```python
frutas = ["manzana", "pera", "uva"]
frutas.remove("pera")
print(frutas)  # ["manzana", "uva"]
```

-----

### **Eliminar una lista – `del()`**

Elimina **una variable o lista completa**.

```python
numeros = [1, 2, 3]
del numeros
# Ahora `numeros` ya no existe.
```

También se puede usar para eliminar un solo elemento:

```python
frutas = ["manzana", "pera", "uva"]
del frutas[1]
print(frutas)  # ["manzana", "uva"]
```

-----

### **Invertir una lista – `reverse()`**

Invierte el orden de los elementos en la misma lista.

```python
letras = ["a", "b", "c"]
letras.reverse()
print(letras)  # ["c", "b", "a"]
```

-----

### **Ordenar elementos – `sort()`**

Ordena los elementos de menor a mayor (o alfabéticamente).

```python
numeros = [3, 1, 4, 2]
numeros.sort()
print(numeros)  # [1, 2, 3, 4]

nombres = ["Luis", "Ana", "Pedro"]
nombres.sort()
print(nombres)  # ["Ana", "Luis", "Pedro"]
```

Para ordenar al revés:

```python
nombres.sort(reverse=True)
```

-----

### **Buscar elementos en una lista – `index()`**

Devuelve el **índice del primer elemento** que coincida con el valor.

```python
colores = ["rojo", "verde", "azul"]
print(colores.index("verde"))  # 1
```

-----

### **Concatenar listas – `extend()`**

Une los elementos de una lista con otra.

```python
lista1 = [1, 2]
lista2 = [3, 4]

lista1.extend(lista2)
print(lista1)  # [1, 2, 3, 4]
```

También se puede usar con el operador `+`, pero crea una **nueva lista**:

```python
nueva_lista = lista1 + lista2
```

-----

### **Sumar elementos de una lista – `sum()`**

Suma todos los elementos numéricos.

```python
numeros = [10, 20, 30]
print(sum(numeros))  # 60
```

-----

### **Construir objetos a lista**

Puedes **convertir otros objetos** (como cadenas, tuplas o rangos) en listas con `list()`.

```python
cadena = "hola"
lista_letras = list(cadena)
print(lista_letras)  # ['h', 'o', 'l', 'a']

rango = range(5)
lista_rango = list(rango)
print(lista_rango)  # [0, 1, 2, 3, 4]
```

-----

### **Listas anidadas**

Son listas dentro de otras listas. Puedes acceder a los elementos con múltiples índices.

```python
datos = [
    ["Ana", 25],
    ["Luis", 30],
    ["Carlos", 22]
]

print(datos[1])      # ["Luis", 30]
print(datos[1][0])   # "Luis"
print(datos[2][1])   # 22
```

-----

### **Matrices con listas anidadas**

Se representan como listas dentro de listas, cada lista interna es una fila.

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matriz[0][0])  # 1 (primera fila, primera columna)
print(matriz[2][1])  # 8 (tercera fila, segunda columna)
```

Puedes recorrer la matriz con bucles anidados:

```python
for fila in matriz:
    for elemento in fila:
        print(elemento, end=" ")
    print()  # Salto de línea por cada fila
```

-----

### **Matrices con el ciclo `for`**

Puedes recorrer una **matriz (lista de listas)** con un **bucle `for` anidado**, fila por fila y luego elemento por elemento:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for fila in matriz:
    for elemento in fila:
        print(elemento, end=" ")
    print()  # Para hacer salto de línea al final de cada fila
```

-----

### **Suma de matrices**

Para sumar dos matrices del mismo tamaño, se suman **elemento por elemento**.

```python
A = [
    [1, 2],
    [3, 4]
]

B = [
    [5, 6],
    [7, 8]
]

resultado = []

for i in range(len(A)):
    fila = []
    for j in range(len(A[0])):
        suma = A[i][j] + B[i][j]
        fila.append(suma)
    resultado.append(fila)

print(resultado)  # [[6, 8], [10, 12]]
```

-----

### **Diccionarios**

Un **diccionario** en Python almacena datos en **pares clave-valor**.

```python
persona = {
    "nombre": "Ana",
    "edad": 28,
    "ciudad": "San Jose"
}
```

-----

### **Acceder a elementos de un diccionario**

Puedes acceder a un valor usando la **clave**:

```python
print(persona["nombre"])  # Ana
print(persona.get("edad"))  # 28
```

`get()` es más seguro porque no lanza error si la clave no existe.

-----

### **Método `items()`**

Devuelve una **lista de tuplas** con todos los pares clave-valor.

```python
for clave, valor in persona.items():
    print(clave, "→", valor)
```

-----

### **Método `keys()`**

Devuelve solo las **claves** del diccionario:

```python
print(persona.keys())  # dict_keys(['nombre', 'edad', 'ciudad'])
```

-----

### **Método `values()`**

Devuelve solo los **valores** del diccionario:

```python
print(persona.values())  # dict_values(['Ana', 28, 'Cartago'])
```

-----

### **Método `clear()`**

Borra **todos los elementos** del diccionario:

```python
persona.clear()
print(persona)  # {}
```

-----

### **Modificar y agregar elementos a un diccionario**

Puedes **modificar** un valor asignando otro nuevo a la clave, o agregar un nuevo par clave-valor:

```python
persona = {"nombre": "Ana", "edad": 28}

persona["edad"] = 30       # Modificar
persona["profesión"] = "Ingeniera"  # Agregar

print(persona)
# {'nombre': 'Ana', 'edad': 30, 'profesión': 'Ingeniera'}
```

-----

### **Método `copy()`**

Crea una **copia independiente** del diccionario.

```python
original = {"a": 1, "b": 2}
copia = original.copy()

copia["a"] = 99

print(original)  # {'a': 1, 'b': 2}
print(copia)     # {'a': 99, 'b': 2}
```

-----

### **Método `fromkeys()`**

Crea un diccionario con **claves definidas** y un **mismo valor predeterminado**.

```python
claves = ["nombre", "edad", "ciudad"]
nuevo_dic = dict.fromkeys(claves, "No definido")

print(nuevo_dic)
# {'nombre': 'No definido', 'edad': 'No definido', 'ciudad': 'No definido'}
```

-----

### **Método `get()`**

Accede al valor de una clave de forma **segura** (no lanza error si la clave no existe).

```python
persona = {"nombre": "Ana", "edad": 28}

print(persona.get("edad"))        # 28
print(persona.get("profesión"))   # None
print(persona.get("profesión", "No disponible"))  # "No disponible"
```

-----

### **Método `popitem()`**

Elimina y devuelve el **último par clave-valor** del diccionario.

```python
datos = {"a": 1, "b": 2, "c": 3}
ultimo = datos.popitem()

print(ultimo)  # ('c', 3)
print(datos)   # {'a': 1, 'b': 2}
```

-----

### **Método `pop()` con diccionario**

Elimina un **elemento específico** por clave.

```python
persona = {"nombre": "Ana", "edad": 28}
persona.pop("edad")

print(persona)  # {'nombre': 'Ana'}
```

También puedes pasar un valor por defecto si no existe la clave:

```python
persona.pop("ciudad", "No existe")  # No error
```

-----

### **Método `setdefault()`**

  * Si la **clave existe**, devuelve su valor.
  * Si **no existe**, la crea con un valor por defecto.

<!-- end list -->

```python
persona = {"nombre": "Ana"}
persona.setdefault("edad", 30)

print(persona)  # {'nombre': 'Ana', 'edad': 30}
```

-----

### **Método `update()`**

Actualiza un diccionario con otro diccionario o con pares clave-valor.

```python
persona = {"nombre": "Ana", "edad": 28}
persona.update({"edad": 30, "ciudad": "San Jose"})

print(persona)
# {'nombre': 'Ana', 'edad': 30, 'ciudad': 'San Jose'}
```

-----

### **Tuplas**

Una **tupla** es como una lista, pero **inmutable** (no se puede modificar después de creada).

```python
colores = ("rojo", "verde", "azul")
```

-----

### **Acceder a los elementos de una tupla**

Se accede igual que con listas, usando índices.

```python
print(colores[0])  # "rojo"
print(colores[-1]) # "azul"
```

-----

### **Operador de segmentación en tuplas**

Puedes usar **slicing** (rebanado) igual que en cadenas o listas.

```python
numeros = (0, 1, 2, 3, 4, 5)

print(numeros[1:4])   # (1, 2, 3)
print(numeros[:3])    # (0, 1, 2)
print(numeros[::2])   # (0, 2, 4)
```

-----

### **Desempaquetado de tuplas**

Permite **asignar directamente** los valores de una tupla a variables.

```python
persona = ("Ana", 28, "San Jose")
nombre, edad, ciudad = persona

print(nombre)  # Ana
print(edad)    # 28
print(ciudad)  # San Jose
```

-----

### **Inmutabilidad de una tupla**

Una **tupla es inmutable**, lo que significa que **no se puede cambiar, agregar ni eliminar** sus elementos después de creada.

```python
mi_tupla = (1, 2, 3)
# mi_tupla[0] = 10  ❌ Esto causará un error: TypeError
```

Sin embargo, sí puedes:

  * Leer sus elementos
  * Hacer slicing
  * Convertirla a lista para modificarla, y luego volverla a tupla

-----

### **Función `tuple()`**

Convierte **otro tipo de datos** (lista, cadena, rango, etc.) en una **tupla**.

```python
lista = [1, 2, 3]
tupla = tuple(lista)
print(tupla)  # (1, 2, 3)

cadena = "hola"
print(tuple(cadena))  # ('h', 'o', 'l', 'a')
```

-----

### **Concatenación de tuplas**

Puedes unir dos o más tuplas usando el operador `+`.

```python
a = (1, 2)
b = (3, 4)
c = a + b
print(c)  # (1, 2, 3, 4)
```

-----

### **La función `zip()`**

Une elementos de varias listas (o tuplas) en **pares**, formando una tupla por cada posición.

```python
nombres = ("Ana", "Luis", "Pedro")
edades = (25, 30, 35)

combinado = zip(nombres, edades)
print(list(combinado))
# [('Ana', 25), ('Luis', 30), ('Pedro', 35)]
```

-----

### **Conjuntos y la función `set()`**

Un **conjunto** es una colección **desordenada y sin elementos repetidos**.

```python
mi_set = set([1, 2, 2, 3])
print(mi_set)  # {1, 2, 3}

# También se puede crear así:
otro_set = {4, 5, 6}
```

-----

### **Método `issubset()`**

Devuelve `True` si **todos los elementos** de un conjunto están en otro.

```python
a = {1, 2}
b = {1, 2, 3, 4}

print(a.issubset(b))  # True
```

-----

### **Método `issuperset()`**

Es lo opuesto: devuelve `True` si el conjunto actual **contiene completamente** al otro.

```python
b = {1, 2, 3, 4}
a = {1, 2}

print(b.issuperset(a))  # True
```

-----

### **Método `union()`**

Devuelve un nuevo conjunto con **todos los elementos**, **sin duplicados**.

```python
a = {1, 2}
b = {2, 3, 4}

print(a.union(b))  # {1, 2, 3, 4}
```

-----

### **Método `intersection()`**

Devuelve un conjunto con los **elementos comunes**.

```python
a = {1, 2, 3}
b = {2, 3, 4}

print(a.intersection(b))  # {2, 3}
```

-----

### **Método `difference()`**

Devuelve los elementos que **están en el primer conjunto pero no en el segundo**.

```python
a = {1, 2, 3}
b = {2, 3, 4}

print(a.difference(b))  # {1}
print(b.difference(a))  # {4}
```

-----

### **Método `add()`**

Agrega un **elemento único** al conjunto.

```python
mi_set = {1, 2, 3}
mi_set.add(4)
print(mi_set)  # {1, 2, 3, 4}
```

-----

### **Método `update()`**

Agrega **varios elementos** (de una lista, tupla u otro set) al conjunto.

```python
mi_set = {1, 2}
mi_set.update([3, 4], {5, 6})
print(mi_set)  # {1, 2, 3, 4, 5, 6}
```

-----

### **Métodos `remove()` y `discard()`**

  * `remove(x)` elimina el elemento `x`, pero **lanza error** si no existe.
  * `discard(x)` elimina `x`, pero **no lanza error** si no está.

<!-- end list -->

```python
mi_set = {1, 2, 3}
mi_set.remove(2)   # OK
# mi_set.remove(5) # ❌ Error

mi_set.discard(5)  # ✅ No error aunque 5 no esté
```

-----

### **Función `enumerate()`**

Permite **recorrer una lista o tupla** obteniendo el **índice y el valor** al mismo tiempo.

```python
frutas = ["manzana", "pera", "uva"]

for indice, fruta in enumerate(frutas):
    print(indice, fruta)

# 0 manzana
# 1 pera
# 2 uva
```

-----

### **Módulo `random`**

Permite generar **números aleatorios** y seleccionar elementos de manera aleatoria.

Importación:

```python
import random
```

Funciones comunes:

```python
print(random.randint(1, 10))     # Número aleatorio entre 1 y 10
print(random.random())           # Número aleatorio entre 0.0 y 1.0
print(random.choice(["a", "b", "c"]))  # Elige aleatoriamente un elemento
```

-----

### **Manejo de excepciones (`try` / `except`)**

Se usa para **evitar que el programa se detenga** por errores en tiempo de ejecución.

```python
try:
    numero = int(input("Ingresa un número: "))
    resultado = 10 / numero
    print("Resultado:", resultado)

except ValueError:
    print("Error: Debes ingresar un número entero.")

except ZeroDivisionError:
    print("Error: No se puede dividir entre cero.")

finally:
    print("Fin del programa.")
```

  * `try`: bloque donde puede ocurrir un error.
  * `except`: bloque que maneja el error.
  * `finally`: bloque que siempre se ejecuta (opcional, útil para limpiar recursos).

<!-- end list -->

```
```
