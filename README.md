# Lista de numeros primos
![LISTA DE NUMEROS PRIMOS ](https://user-images.githubusercontent.com/124607325/221423790-bd4e997c-6036-4fed-ad27-22695ea9a88b.png)

## Pasos
Se inicia el programa en el nodo "Inicio".

1. Se ingresa un número n en el nodo "Número n".
2. Se inicia una lista vacía  en la cual se pondran los numeros que se vayan econtrando.
3.Se da un rango de los numeros primos que se hallaran en el que i estara en el rando de 2 a n.
4.si el numero i es igual a 2, el algoritmo asume que 2 es un número primo y lo agrega a la lista de números primos.
5.Si i es mayor que 2, el algoritmo inicia la variable "es_primo" en True.
6.Luego, se repite a través de cada número M en el rango de 2 a i-1 en el nodo "Para cada número M en el rango de 2 a i-1, hacer lo siguiente:".
7.Si el número i es divisible por M, el algoritmo establece "es_primo" en False en el nodo "Si i es divisible por M, establecer es_primo en False y salir del bucle".
8.Si no, continúa con el siguiente número M en el nodo "Si no, continuar con el siguiente número M".
9 .Si "es_primo" sigue siendo True después de repetur a través de todos los números M, el algoritmo agrega el número i a la lista de números primos en el nodo "Si es_primo=True, agregar i a la lista de números primos".
10. El algoritmo continúa repitiendose através de los números i hasta que se llega a n.
11. Finalmente, el algoritmo imprime la lista de números primos encontrados en el nodo "Imprimir la lista de números primos encontrados" 
12. Y  termina  "Fin".

## Pseucodigo 
      variables
      n : entero
      i : entero
      M : entero
      
      inicio
    
      Leer n
      Inicializar una lista de números primos
      Para cada número i en el rango de 2 a n, hacer lo siguiente:
      es_primo = True
      Para cada número M en el rango de 2 a i-1, hacer lo siguiente:
      Si i es divisible por M, establecer es_primo en False y salir del bucle
      Si es_primo=True, agregar i a la lista de números primos
      Si i es divisible por M, establecer es_primo en False y salir del bucle
      Imprimir la lista de números primos encontrados
      Fin

# Hallar la raiz cuadrada de un numero n
![pako_eNqNU81ymzAQfhWNTmSGePxP4NBO_Bc7qX1JTik9bIWKNTUSFagTx_bD9AHyAr36xboSwSmNDwUGWPR92t3vY3eUqYTTiKYa8jV5mMSS4HH9eSEFE-oLubz8QEbeRPwUidCEb4g8_s64VoRLkmqTq4IknCT4YOKbhuKi2mDkiOPdHLbEyBNJZDloS6jAHw8VeuzQ-_vjy55MvOtU8](https://user-images.githubusercontent.com/124607325/221444135-ac26f014-c526-4088-b03b-9b28cd3b2a67.png)

1. Se inicia el diagrama con el nodo " inicio "
2. Se  divide el número en grupos de dos cifras, en caso de que el número de cifras sea impar, se agrega un cero al inicio del número.
3. Se  busca el mayor número entero que elevado al cuadrado sea menor o igual al primer grupo de dos cifras, esto se da usando la función sqrt.
4. Se guarda el número encontrado en una lista que representa la raíz cuadrada aproximada del número original y se calcula el residuo.
5. Se repite el proceso para cada uno de los grupos de dos cifras restantes:
a. Se agrega el siguiente grupo de dos cifras al residuo.
b. Se busca el mayor número que aplicado con la raíz cuadrada hasta el momento,  de un cuadrado menor o igual al residuo. Este proceso se realiza mediante un algoritmo el cual busca el valor de x tal que (2*r+x)^2 <= residuo, donde r es el valor de la raíz cuadrada hasta el momento.
c. El número encontrado se agrega a la lista de la raíz cuadrada aproximada y se recalcula el residuo.
d. Se repite el proceso a partir del paso 5a hasta que no queden más grupos de dos cifras.
6. Se retorna la raíz cuadrada aproximada del número origina


## pseucodigo 
     Variables 
     n = Real 
     x = Real
     a = Real
     Inicio 
     funcion aritmetica_baldor(n):
    digits = [int(d) para d in str(n)]
    si len(digits) % 2 != 0:
        digits = [0] + digits
    groups = [int(str(digits[i])+str(digits[i+1])) para i en rango(0, len(digits), 2)]
    
    a = entero(raiz_cuadrada(groups[0]))
    res = groups[0] - a**2
    resultado = [a]

    para i en rango(1, len(groups)):
        res = res*100 + groups[i]
        x = 0
        y = 2*resultado[-1]
        mientras Verdadero:
            si (y+x)**2 <= res:
                x += 1
            sino:
                y -= 1
            si x > y:
                romper
        resultado.append(x-1)
        res = res - (x-1)**2
    
   Escribir la raíz cuadrada aproximada del número original
    devolver entero(concatenar(resultado))
