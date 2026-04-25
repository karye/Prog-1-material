# Prov 4c: listor

I det här provet testas din förmåga att skapa listor med text och tal samt skriva ut dem. Temat är **mat och recept**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Favoritmaträtter

**Uppgift:** Skapa en lista med tre maträtter och skriv ut listan.

**Exempel på körning:**
```text
=== Mina favoritmaträtter ===
Maträtter: ['pizza', 'tacos', 'sushi']
```

**Facit:**
```python
print("=== Mina favoritmaträtter ===")
matratter = ["pizza", "tacos", "sushi"]
print("Maträtter:", matratter)
```

---

### Uppgift 2: Prislista

**Uppgift:** Skapa en lista med fyra priser (heltal i kronor) och skriv ut listan.

**Exempel på körning:**
```text
=== Prislista ===
Priser: [89, 120, 75, 99]
```

**Facit:**
```python
print("=== Prislista ===")
priser = [89, 120, 75, 99]
print("Priser:", priser)
```

---

### Uppgift 3: Receptinfo

**Uppgift:** Skapa en lista med tre saker om ett recept: namn på rätten (text), antal portioner (tal) och tid i minuter (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Receptinfo ===
Recept: ['Pannkakor', 4, 20]
```

**Facit:**
```python
print("=== Receptinfo ===")
recept = ["Pannkakor", 4, 20]
print("Recept:", recept)
```

---

### Uppgift 4: Två ingredienser

**Uppgift:** Fråga användaren om två ingredienser med `input()`. Skapa en lista med de två ingredienserna och skriv ut listan.

**Exempel på körning:**
```text
=== Mina ingredienser ===
Ingrediens 1: mjöl
Ingrediens 2: ägg
Din lista: ['mjöl', 'ägg']
```

**Facit:**
```python
print("=== Mina ingredienser ===")
ing1 = input("Ingrediens 1: ")
ing2 = input("Ingrediens 2: ")
ingredienser = [ing1, ing2]
print("Din lista:", ingredienser)
```

---

### Uppgift 5: Beställning

**Uppgift:** Fråga användaren om en maträtt med `input()` och antal portioner med `int(input())`. Skapa en lista med maträttens namn (text) och antal portioner (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Beställning ===
Maträtt: Lasagne
Antal portioner: 2
Din beställning: ['Lasagne', 2]
```

**Facit:**
```python
print("=== Beställning ===")
ratt = input("Maträtt: ")
portioner = int(input("Antal portioner: "))
bestallning = [ratt, portioner]
print(f"Din beställning: {bestallning}")
```
