# Reto_11
Código de tres puntos concernientes al reto número 11-srings

2. Según el archivo, procesar:

- Cantidad de vocales.
    Solución:
```pseudocode
manejador_archivo = open('mbox.txt')

contador_vocales = 0
for linea in manejador_archivo:
    if linea.count("A") > 0:
        contador_vocales += 1
    if linea.count("E") > 0:
        contador_vocales += 1
    if linea.count("I") > 0:
        contador_vocales += 1
    if linea.count("O") > 0:
        contador_vocales += 1
    if linea.count("U") > 0:
        contador_vocales += 1
    if linea.count("a") > 0:
        contador_vocales += 1
    if linea.count("e") > 0:
        contador_vocales += 1
    if linea.count("i") > 0:
        contador_vocales += 1
    if linea.count("o") > 0:
        contador_vocales += 1
    if linea.count("u") > 0:
        contador_vocales += 1
print("La cantidad de vocales en el archivo es :", contador_vocales) # La cantidad de vocales en el archivo es : 532943
```

- Cantidad de consonantes
    Solución:

```pseudocode
manejador_archivo = open('mbox.txt')
contador_consonantes = 0
for linea in manejador_archivo:
    if linea.count("B") > 0:
        contador_consonantes += 1
    if linea.count("C") > 0:
        contador_consonantes += 1
    if linea.count("D") > 0:
        contador_consonantes += 1
    if linea.count("F") > 0:
        contador_consonantes += 1
    if linea.count("G") > 0:
        contador_consonantes += 1
    if linea.count("H") > 0:
        contador_consonantes += 1
    if linea.count("J") > 0:
        contador_consonantes += 1
    if linea.count("K") > 0:
        contador_consonantes += 1
    if linea.count("L") > 0:
        contador_consonantes += 1
    if linea.count("M") > 0:
        contador_consonantes += 1
    if linea.count("N") > 0:
        contador_consonantes += 1
    if linea.count("Ñ") > 0:
        contador_consonantes += 1
    if linea.count("P") > 0:
        contador_consonantes += 1
    if linea.count("Q") > 0:
        contador_consonantes += 1
    if linea.count("R") > 0:
        contador_consonantes += 1
    if linea.count("S") > 0:
        contador_consonantes += 1
    if linea.count("T") > 0:
        contador_consonantes += 1
    if linea.count("V") > 0:
        contador_consonantes += 1
    if linea.count("W") > 0:
        contador_consonantes += 1
    if linea.count("X") > 0:
        contador_consonantes += 1
    if linea.count("Y") > 0:
        contador_consonantes += 1
    if linea.count("Z") > 0:
        contador_consonantes += 1
    if linea.count("b") > 0:
        contador_consonantes += 1
    if linea.count("c") > 0:
        contador_consonantes += 1
    if linea.count("d") > 0:
        contador_consonantes += 1
    if linea.count("f") > 0:
        contador_consonantes += 1
    if linea.count("g") > 0:
        contador_consonantes += 1
    if linea.count("h") > 0:
        contador_consonantes += 1
    if linea.count("j") > 0:
        contador_consonantes += 1
    if linea.count("k") > 0:
        contador_consonantes += 1
    if linea.count("l") > 0:
        contador_consonantes += 1
    if linea.count("m") > 0:
        contador_consonantes += 1
    if linea.count("n") > 0:
        contador_consonantes += 1
    if linea.count("ñ") > 0:
        contador_consonantes += 1
    if linea.count("p") > 0:
        contador_consonantes += 1
    if linea.count("q") > 0:
        contador_consonantes += 1
    if linea.count("r") > 0:
        contador_consonantes += 1
    if linea.count("s") > 0:
        contador_consonantes += 1
    if linea.count("t") > 0:
        contador_consonantes += 1
    if linea.count("v") > 0:
        contador_consonantes += 1
    if linea.count("w") > 0:
        contador_consonantes += 1
    if linea.count("x") > 0:
        contador_consonantes += 1
    if linea.count("y") > 0:
        contador_consonantes += 1
    if linea.count("z") > 0:
        contador_consonantes += 1
print("La cantidad de consonantes en mbox.txt es:", contador_consonantes) # La cantidad de consonantes en mbox.txt es: 1392399
```

- Listado de 50 palabras que más se repiten.
    Solución:

```pseudocode
import re
from collections import Counter

def top_50_words(filename):
    try:
        with open(filename, 'r', encoding='utf-8') as file:
            text = file.read()
    except FileNotFoundError:
        return "Error: El archivo no se encontró."
    except Exception as e:
        return f"Error al leer el archivo: {e}"

    words = re.findall(r'\b\w+\b', text.lower()) 

    word_counts = Counter(words)

    top_50 = word_counts.most_common(50)

    return top_50
filename = 'mbox.txt'
top_50 = top_50_words(filename)
x = 0
if isinstance(top_50, list):
    print("Las 50 palabras más comunes son:")
    for word, count in top_50:
        x += 1
        print(str(x) + ": " + str(word) + " -> " + str(count))
        
else:
    print(top_50) 
```
