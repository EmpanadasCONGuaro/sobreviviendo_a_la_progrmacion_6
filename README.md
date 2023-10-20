# sobreviviendo_a_la_progrmacion_6



# 1.Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.


```pseudocode
for x in range (1,101):
  elcuadrado = x**2
  print(elcuadrado)

```


# 2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.


```pseudocode
for x in range(1,1000,2):
    
    print(x) 
print("hasta aqui van los impaeres")

for y in range(2,1001,2):
    print(y)

print("hasta aqui van los pares")   
```


# 3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado


```pseudocode
x:int=int(input("ingrese un numero:"))
for x in range(x,1,-1):
    if x%2==0:
        print(x)
for x in range(x,1,-1):
    if x%2!=0:
        print(x)

```


# 4. Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial


```pseudocode
import math
x:int=int(input("ingrese un numero:"))
factorial = 1

for x in range(1,x+1,1):
    factorial = math.factorial(x)
    print(f"El factorial de {x} es {factorial}")
```


# 5. Calcular el valor de 2 elevado a la potencia n usando ciclos for.


```pseudocode
x:int= int(input("Ingrese el numero de la potencia:"))
Lapotencia = 2

for x in range(x-1):
  Lapotencia *= 2

print(f"El resultado es {Lapotencia}")
```


# 6. Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for. Disclaimer: Trate de no utilizar el operador de potencia (**).


```pseudocode
x:int=int(input("ingrese el valor de x:"))
n:int=int(input("ingrese el valor de n:"))
potencia=1

for n in range(n):
    potencia *= x
print(potencia)
```

# 7. Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.


```pseudocode
for x in range(1,10):
    print(f"la tabla de multiplicar {x}")
    
    for y in range(1,11):
      TablaDeMultiplicar= x*y
      print(f"{x} x {y} = {TablaDeMultiplicar}")  
    
```


# 8. Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.



![image](https://github.com/EmpanadasCONGuaro/sobreviviendo_a_la_progrmacion_6/assets/142174506/e636172a-2f9f-452f-8bac-1435e58c82f5)



```pseudocode
from math import exp, factorial

def aproximacion(x: float, y: int) -> float:
    suma: float = 0
    for i in range(0,y+1):
        aproximacion1= (x**i)/factorial(i)

        suma += aproximacion1
    return suma

if __name__ == "__main__": 
    y : int = 10
    x : float = float(input("Ingrese un número real: "))
    aproximacion1 : float = aproximacion(x,y)
    ValorReal : float = exp(x)
    print(f"Aproximación:{aproximacion1}")
    print(f"Valor real:{ValorReal}")

    error:float=(abs(ValorReal - aproximacion1)) / ValorReal * 100 

    print(f"El porcentaje de error es de:{error}%") 

```


# 9. Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.


![image](https://github.com/EmpanadasCONGuaro/sobreviviendo_a_la_progrmacion_6/assets/142174506/edb8b639-2476-48a3-ada2-12bbe8f5f1f2)


```pseudocode
from math import sin, factorial
def aproximaciondelseno(x: float, y: int) -> float:
    suma: float = 0
    for i in range(0,y+1):
        aproximaciondelseno1= (((-1)**i)*((x**((2*i)+1))/factorial(2*i+1)))
        suma += aproximaciondelseno1
    return suma

if __name__ == "__main__": 
    y : int = 1
    x : float = float(input("Ingrese un número real: "))
    aproximacion1 : float = aproximaciondelseno (x,y)
    ValorReal : float = sin(x)
    print(f"Aproximación:{aproximacion1}")
    print(f"Valor real:{ValorReal}")
    error:float=(abs(ValorReal - aproximacion1)) / ValorReal * 100 
    print(f"El porcentaje de error es de:{error}%") 

```


# 10. Diseñar una función que permita calcular una aproximación de la función arcotangente alrededor de 0 para cualquier valor x en el rango [-1, 1], utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función arctan y mostrar la diferencia entre el valor real y la aproximación.



![image](https://github.com/EmpanadasCONGuaro/sobreviviendo_a_la_progrmacion_6/assets/142174506/565c143a-8744-47ec-bfad-5df5646d5475)


```pseudocode
import math
from math import atan, factorial
def aproximaciondelarctangente(x: float, y:float) -> float: 
    suma: float = 0
    for i in range(0,2):
        y = (((-1)**i)*((x**((2*i)+1))/factorial((2*i)+1)))
        suma += y
    return suma

if __name__ == "__main__": 
    
    x : float = float(input("Ingrese un número real: "))
    n: int = 1
    aproximacion1 : float = aproximaciondelarctangente (x,n)
    ValorReal : float = atan(x)
    print(f"Aproximación:{aproximacion1}")
    print(f"Valor real:{ValorReal}")

    error:float=(abs(ValorReal - aproximacion1)) / ValorReal * 100 

    print(f"El porcentaje de error es de:{error}%") 

```



 - NOTA: como en la matemática no es posible elevar un numero negativo a otro negativo, no me fue posible hacer de un rango [-1,1]. (supuse que era por eso)
 - lo hice de rango [0,1] y si funciono, pero este punto me genera dudas al igual que todos :)
 - NOTA 2:  Al parecer me corrio el codigo, PERO, (siempre hay un Pero) no se si los resultdos sean correctos, asi que despues de varias horas, me rindo. Espero que este bien

   

