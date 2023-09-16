### Hi there 👋
###### Calcular el perímetro de un cuadrado

lado=int(input("Ingrese medida de lado del cuadrado: "))

perimetro=lado * 4

print("El perimetro del cuadrado es: ")
print(perimetro)



###### Encontrar el mínimo y máximo de una lista de números

def min_max(numeros):
    menor = numeros [0]
    mayor = numeros [0]

    for n in numeros:
        if n < menor:
            menor = n 

        if n > mayor:
            mayor = n

    return menor, mayor

datos = [9, 5, 11, 87, 99, 6, 3, 0]

print(min_max(datos))

###### Verificar si una cadena de texto contiene solo dígito

cadena = "input("Ingrese una cadena de texto: ")"

if cadena.isdigit():
    print("La cadena contiene solo dígitos.")
else:
    print("La cadena NO contiene solo dígitos.")


###### Calcular el factorial de un número utilizando una función recursiva

def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

n = factorial(1)
print(n)


###### Invertir una lista

lista = [2001,2002,2003,2004,2005,2006]
lista2 = lista[::-1]
print(lista2)

###### Calcular el producto de dos matrices
def calcular_suma_matrices(A, B):
    if len(A) != len(B):
        raise ArithmeticError("Las dos matrices deben tener la misma cantidad de filas")
    
    if len(A[0]) != len(B[0]):
        raise ArithmeticError("Las dos matrices deben tener la misma cantidad de columnas")
    
    suma_matrices = []

    for i in range(len(A)):
        fila = []
        for j in range(len(A[0])):
            fila.append(A[i][j] + B[i][j])

        suma_matrices.append(fila)
    
    return suma_matrices

A = [[1, 2, 3], [4, 5, 6]]
B = [[6, 5, 4], [9, 8, 7]]

resultado = calcular_suma_matrices(A, B)
for fila in resultado:
    print(fila)

###### Verificar si una palabra es un anagrama de otra
def esAnagrama(cad1,cad2):
    return sorted(cad1)==sorted(cad2)

print(esAnagrama("roma","mora"))


###### Encontrar el segundo elemento más grande en una lista

def segundo_mayor(numeros):
    if isinstance(numeros, list):
        if len(numeros) < 2:
            return None
        
        if len(numeros) == 2 and numeros[0] == numeros[1]:
            return None
        
        duplicados = set()
        unicos = []

        for n in numeros:
            if n not in duplicados:
                duplicados.add(n)
                unicos.append(n)

        unicos.sort()

        return unicos[-2]
    
    raise TypeError("El parametro numeros debe ser una lista")

numeros = [1, 4, 45, 5, 7, 23, 6, 11, 17, 27, 90]

print(segundo_mayor(numeros))

###### Generar una lista de números primos en un rango dado

def es_primo(numero):
    if numero <= 1:
        return False
    elif numero <= 3:
        return True
    elif numero % 2 == 0 or numero % 3 == 0:
        return False
    i = 5
    while i * i <= numero:
        if numero % i == 0 or numero % (i + 2) == 0:
            return False
        i += 6
    return True

def lista_primos_en_rango(inicio, fin):
    primos = []
    for numero in range(max(inicio, 2), fin + 1):
        if es_primo(numero):
            primos.append(numero)
    return primos



print("Números primos en el rango de", inicio, "a", fin, "son:")
print(primos_en_rango)

###### Ordenar una lista de números de forma ascendente

lista = [4, 1, 8, 3, 6, 2, 9, 5, 7]

# Ordenar la lista de forma ascendente (modifica la lista original)
lista.sort()

print("Lista ordenada de forma ascendente:", lista)
