# Reto_4
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
      Inicio
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
