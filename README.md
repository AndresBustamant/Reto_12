# Reto_12

**_1. Consulte que hacen los siguientes métodos de strings en python_**:

-endswith:
este metodo se utiliza para determinar si una cadena termina en una subcadena especifica o un subfijo especificado. En caso de terminar en dicho subfijo devuelve True, en otro caso devuelve False.

	<sub> Estructura: str/cadenaprincipal.endswith(suffix/subcadena[, start[, end]] )</sub>

```pseudocode
texto = "Hola, ¿como va tu dia?"
resultado = texto.endswith("dia?")  # Verifica si termina con "dia?"
print(resultado)  # Esto imprimirá True

resultado = texto.endswith("Hola")  # Verifica si termina con "Hola"
print(resultado)  # Esto imprimirá False
```
-startswith:
este metodo es utilizasod para saber si una cadena empieza con una subcadena especificada o un subfijo especificado. En casos de inciar con dicho subfijo devuelve True, en caso contrario devuelve False.

	<sub> Estructura: str/cadenaprincipal.startswith(suffix/subcadena[, start[, end]] )</sub>

```pseudocode
texto = "Hola, ¿como va tu dia?"
resultado = texto.startswith("Hola")  # Verifica si inicia con "Hola"
print(resultado)  # Esto imprimirá True

resultado = texto.startswith("dia?")  # Verifica si inicia con "dia?"
print(resultado)  # Esto imprimirá False
```
 
-isalpha:
este metodo devuelve True si la cadena a evaluar tiene solo letras, en caso contrario retorna False (ejemplos de esto son los espacios en blanco, numeros o caracteres especiales).

	<sub> Estructura: str/cadenaprincipal.isalpha() </sub>

```pseudocode
texto = "Hola"
resultado = texto.isalpha()  # Verifica si el string es solo letras
print(resultado)  # Esto imprimirá True
```

-isalnum:
este metodo sirve para comprobar si una cadena es alfanumerica, es decir esta compuesta por letras y numeros, en caso de cumplir con la condicion devuelve True y si la cadena no cumple o esta vacias retorna False.

	<sub> Estructura: str/cadenaprincipal.isalnum() </sub>

```pseudocode
texto = "Jugador1"
resultado = texto.isalnum()  # Verifica si el string es alfanumerio
print(resultado)  # Esto imprimirá True
```

-isdigit:
este metodo sirve para comprobar si una cadena esta compuesta por solo numeros, en caso de cumplir retorna True, de lo contrario retorna False.

	<sub> Estructura: str/cadenaprincipal.isdigit() </sub>

```pseudocode
texto = "Jugador1"
resultado = texto.isalnum()  # Verifica si el string es alfanumerio
print(resultado)  # Esto imprimirá True
```

-isspace:
este metodo permite verificar si una cadena es vacia o tiene espacios, en caso de cumplir con la condcion devuelve True, de lo contrario retorna False.

<sub> Estructura: str/cadenaprincipal.isspace() </sub>

```pseudocode
texto = " "
resultado = texto.isspace()  # Verifica si el string es vacio
print(resultado)  # Esto imprimirá True
```

-istitle:
este metodo permite evaluar si una cadena esta entregada en formato de titulo, dicho formato consiste en que la primera letra de cada palabra es mayuscula y el resto es minuscula.

<sub> Estructura: str/cadenaprincipal.istitle() </sub>

```pseudocode
texto = "Hola, ¿Como Vas?"
resultado = texto.istitle()  # Verifica si el string es vacio
print(resultado)  # Esto imprimirá True
```

-islower:
este metodo devuelve True cuando todos los caracteres estan en minuscula, de otra manera retorna False

<sub> Estructura: str/cadenaprincipal.islower() </sub>

```pseudocode
texto = "hola, ¿como vas?"
resultado = texto.islower()  # Verifica si el string esta en minusculas
print(resultado)  # Esto imprimirá True
```

-isupper:
este metodo devuelve True cuando todos los caracteres estan en mayuscula, de otra manera retorna False

<sub> Estructura: str/cadenaprincipal.isupper() </sub>

```pseudocode
texto = "HOLA, ¿COMO VAS?"
resultado = texto.isupper()  # Verifica si el string esta en mayusculas
print(resultado)  # Esto imprimirá True
```

**_2. a_**
