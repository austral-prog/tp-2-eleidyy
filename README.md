[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/sqDY-fvG)
# Trabajo Práctico 2

## Ejercicio 1 - Ada

Los nombres suelen venir en distintas formas y uno siempre tiene que estar preparado para lo peor. En este caso, necesitamos ordenar y organizar un poco estos nombres. Para este task, tenes que lograr dado un nombre y un apellido, poder mostrar el nombre completo en distintos formatos. En este caso lo que necesitamos es lo siguiente: 

Dado las siguientes dos variables:

```python
first_name = "AdA"
last_name  = "LoVeLAce"
```

Lograr conseguir este mismo output: 
```python 
ada lovelace 
Ada Lovelace 
ADA LOVELACE  
	ada lovelace
```
first_name="AdA"
last_name="LoVeLAce"
name=f"{first_name} {last_name}"
name_lower=name.lower()
print(name.lower())
print(name.upper())             
print(name.title())
print(f"\t{name.lower()}")
print(f"\t{name_lower}")

## Ejercicio 2 - Earth

El planeta tierra es muy grande y actualmente es el hogar de 7700 millones de personas. Las personas viven en distintos paises y necesitamos distinguir las ubicaciones una de otra.

En este ejercicio, necesitamos saber qué país esta primero en el diccionario. Dado los paises Bangladesh y Barbados, comparar los paises teniendo en cuenta quien esta primero en el diccionario.

La respuesta debería tener el siguiente formato (Donde X es Bangladesh e Y es Barbados):

```python
The result of X comes first in the dictionary than Y is True/False.
The result of Y comes first in the dictionary than X is True/False.
```
X = "Bangladesh"
Y = "Barbados"

def comes_first(X, Y):
    if X < Y:
        return f"The result of {X} comes first in the dictionary than {Y} is True."
    else:
        return f"The result of {X} comes first in the dictionary than {Y} is False."
    
result = comes_first(X, Y)
print(result)

## Ejercicio 3 - Change

Escribir un programa que dado dos números reales que representan el gasto efectuado por una persona y la cantidad pagada, imprima en pantalla el informe de la cantidad de pesos y centavos a devolver.

Hay que respetar el formato del informe (incluido la prolijidad con los espacios y saltos de linea). Un ejemplo de un informe es:

```python
Ingresar gasto:
23.75
Dinero recibido
100

Vuelto

Pesos:
76
Centavos:
25
```
def informe_devolucion(gasto, dinero_recibido):
    # Calcular el vuelto
    vuelto = dinero_recibido - gasto

    # Separar la parte entera de la parte decimal
    pesos = int(vuelto)
    centavos = round((vuelto - pesos) * 100, 0)

    # Imprimir el informe de devolución
    print("Informe de devolución:")
    print("=======================")
    print("Cantidad a devolver:")
    print(f"{pesos} pesos y {centavos} centavos")

# Ejemplo de uso
gasto = float(input("Ingresar gasto: "))
dinero_recibido = float(input("Dinero recibido: "))

informe_devolucion(gasto, dinero_recibido)

