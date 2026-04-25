# Träning inför prov 6b: for-loopar och slump

Här får du träna på samma moment som kommer på Prov 6b. Temat är **mat och recept**.

---

### Uppgift 1: Loopa igenom maträtter

**Uppgift:** Skapa en lista med tre maträtter: `["pasta", "sushi", "tacos"]`. Använd en `for`-loop för att gå igenom listan och skriva ut varje rätt med texten `"Maträtt:"` framför.

**Exempel på körning:**
```text
Maträtt: pasta
Maträtt: sushi
Maträtt: tacos
```

**Facit:**
```python
matratter = ["pasta", "sushi", "tacos"]
for ratt in matratter:
    print("Maträtt:", ratt)
```

---

### Uppgift 2: Räkna portioner

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut siffrorna 1 till 4. Skriv texten `"Portion"` framför varje siffra.

**Exempel på körning:**
```text
Portion 1
Portion 2
Portion 3
Portion 4
```

**Facit:**
```python
for i in range(1, 5):
    print("Portion", i)
```

---

### Uppgift 3: Lagar idag

**Uppgift:** Skapa en lista med tre rätter: `["soppa", "sallad", "gryta"]`. Använd en `for`-loop och skriv ut en mening för varje rätt.

**Exempel på körning:**
```text
Idag lagar vi soppa
Idag lagar vi sallad
Idag lagar vi gryta
```

**Facit:**
```python
ratter = ["soppa", "sallad", "gryta"]
for ratt in ratter:
    print("Idag lagar vi", ratt)
```

---

### Uppgift 4: Kostnad per portion

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut portionerna 1 till 5. Varje portion kostar 50 kr mer än den förra (portion 1 kostar 50 kr, portion 2 kostar 100 kr och så vidare).

**Exempel på körning:**
```text
Portion 1 kostar 50 kr
Portion 2 kostar 100 kr
Portion 3 kostar 150 kr
Portion 4 kostar 200 kr
Portion 5 kostar 250 kr
```

**Facit:**
```python
for i in range(1, 6):
    print("Portion", i, "kostar", i * 50, "kr")
```

---

### Uppgift 5: Slumpmeny

**Uppgift:** Importera modulen `random`. Skapa en lista med fyra maträtter. Använd `random.choice()` för att slumpa fram en rätt. Skriv ut resultatet med en **f-sträng**.

**Exempel på körning (resultatet varierar):**
```text
Idag äter vi pannkakor!
```

**Facit:**
```python
import random
matratter = ["pannkakor", "köttbullar", "lasagne", "pytt i panna"]
val = random.choice(matratter)
print(f"Idag äter vi {val}!")
```
