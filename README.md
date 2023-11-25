# Reto_12

**_1. Consulte que hacen los siguientes métodos de strings en python_**:

-endswith:
este metodo se utiliza para determinar si una cadena termina en una subcadena especifica o un subfijo especificado. En caso de terminar en dicho subfijo devuelve True, en otro caso devuelve False.

	 Estructura: str/cadenaprincipal.endswith(suffix/subcadena[, start[, end]] )

```pseudocode
texto = "Hola, ¿como va tu dia?"
resultado = texto.endswith("dia?")  # Verifica si termina con "dia?"
print(resultado)  # Esto imprimirá True

resultado = texto.endswith("Hola")  # Verifica si termina con "Hola"
print(resultado)  # Esto imprimirá False
```
-startswith:
este metodo es utilizasod para saber si una cadena empieza con una subcadena especificada o un subfijo especificado. En casos de inciar con dicho subfijo devuelve True, en caso contrario devuelve False.

	 Estructura: str/cadenaprincipal.startswith(suffix/subcadena[, start[, end]] )

```pseudocode
texto = "Hola, ¿como va tu dia?"
resultado = texto.startswith("Hola")  # Verifica si inicia con "Hola"
print(resultado)  # Esto imprimirá True

resultado = texto.startswith("dia?")  # Verifica si inicia con "dia?"
print(resultado)  # Esto imprimirá False
```
 
-isalpha:
este metodo devuelve True si la cadena a evaluar tiene solo letras, en caso contrario retorna False (ejemplos de esto son los espacios en blanco, numeros o caracteres especiales).

	 Estructura: str/cadenaprincipal.isalpha() 

```pseudocode
texto = "Hola"
resultado = texto.isalpha()  # Verifica si el string es solo letras
print(resultado)  # Esto imprimirá True
```

-isalnum:
este metodo sirve para comprobar si una cadena es alfanumerica, es decir esta compuesta por letras y numeros, en caso de cumplir con la condicion devuelve True y si la cadena no cumple o esta vacias retorna False.

	 Estructura: str/cadenaprincipal.isalnum() 

```pseudocode
texto = "Jugador1"
resultado = texto.isalnum()  # Verifica si el string es alfanumerio
print(resultado)  # Esto imprimirá True
```

-isdigit:
este metodo sirve para comprobar si una cadena esta compuesta por solo numeros, en caso de cumplir retorna True, de lo contrario retorna False.

	 Estructura: str/cadenaprincipal.isdigit() 

```pseudocode
texto = "Jugador1"
resultado = texto.isalnum()  # Verifica si el string es alfanumerio
print(resultado)  # Esto imprimirá True
```

-isspace:
este metodo permite verificar si una cadena es vacia o tiene espacios, en caso de cumplir con la condcion devuelve True, de lo contrario retorna False.

	 Estructura: str/cadenaprincipal.isspace()

```pseudocode
texto = " "
resultado = texto.isspace()  # Verifica si el string es vacio
print(resultado)  # Esto imprimirá True
```

-istitle:
este metodo permite evaluar si una cadena esta entregada en formato de titulo, dicho formato consiste en que la primera letra de cada palabra es mayuscula y el resto es minuscula.

	Estructura: str/cadenaprincipal.istitle() 

```pseudocode
texto = "Hola, ¿Como Vas?"
resultado = texto.istitle()  # Verifica si el string es vacio
print(resultado)  # Esto imprimirá True
```

-islower:
este metodo devuelve True cuando todos los caracteres estan en minuscula, de otra manera retorna False

	 Estructura: str/cadenaprincipal.islower() 

```pseudocode
texto = "hola, ¿como vas?"
resultado = texto.islower()  # Verifica si el string esta en minusculas
print(resultado)  # Esto imprimirá True
```

-isupper:
este metodo devuelve True cuando todos los caracteres estan en mayuscula, de otra manera retorna False

	 Estructura: str/cadenaprincipal.isupper()

```pseudocode
texto = "HOLA, ¿COMO VAS?"
resultado = texto.isupper()  # Verifica si el string esta en mayusculas
print(resultado)  # Esto imprimirá True
```

**_2. Procesar el archivo y extraer:_**

-cantidad de vocales:

```pseudocode
def contar_vocales(texto: str): #definicion e una funcion para el conteo de vocales
  n_vocales=0 #conteo
  for letra in texto:
    if letra in "aeiouAEIOU"  #criterio para aumentar el conteo
      n_vocales+=1
    return n_vocales

with open("mbox-short.txt", 'r') as archivo: #apertura del archivo para trabajarlo como una variable
  texto= archivo.read()

cantidad_vocales= contar_vocales(texto) #aplicacion de la funcion a la variable texto

print("la cantidad de vocales es igual a: "+ str(cantidad_vocales))
```
-cantidad de consonantes:

```pseudocode
def contar_consonantes(texto: str):   #definicion de una funcion para el conteo de consonantes
  consonantes=0  #conteo
  for letra in texto:
    if letra.isalpha()  and letra not in  "aeiouAEIOU" #parametro para aumentar el contei
      n_consonantes+=1
    return n_vocales

with open("mbox-short.txt", 'r') as archivo: #apertura del archivo para trabajarlo como una variable
  texto= archivo.read()

cantidad_consonantes= contar_consonantes(texto) #aplicacion de la funcion a la vaiable texto

print("la cantidad de vocales es igual a: "+ str(cantidad_consonantes))
```
-listado de las 50 palabras que mas se repiten:

```pseudocode
def palabras_repetidas(texto: str):   #definicion de una funcion para el conteo de palabras
  texto= texto.lower()   #convierte el texto a minuscula para evalauarlo de manera uniforme

  numero_palabras:{}  #se crea un diccionario con el fin de evidenciar la ocurrencia de las palabras

  for l in texto:  #se reemplazan los espacias y la simbologia no alfabetica
    if not l.isalpha() and != " ":
      texto= texto.replace(l, " ")

  archivo = texto.split()  #se divide el texto en palabras individuales

  for t in archivo:    #se genera un ciclo para contar las ocurrencias de las palabras
    if t not in numero_palabras:  #si la palabra no esta en el diccionario se evalua
      numero_de_palabras[t]=0
    numero_de_palabras[t] +=1 #incrementa con cada ocurrencia

  for l in sorted(numero_de_palabras, reverse=True, key=lambda l: numero_de_palabras[s]):[:51]:
    print("La palabra: {} \tSe repite {} \tveces en el archivo".format(l, numero_de_palabras[l])) #se indica la lectura de las 50 primeras ocurrencias

with open("mbox-short.txt", 'r') as file: #se abre el archivo en tipo lectura para trabajarlo como una variable
  txt = file.read()
  palabras_repetidas(txt) #se llama la funcion para aplicarla a el archivo
```
