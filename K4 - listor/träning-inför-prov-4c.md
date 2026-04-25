# Träning inför prov 4c: listor

Här får du träna på samma moment som kommer på Prov 4c. Temat är **resor**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Resmål

**Uppgift:** Skapa en lista med tre länder och skriv ut listan.

**Exempel på körning:**
```text
=== Mina resmål ===
Länder: ['Italien', 'Thailand', 'Mexiko']
```

**Facit:**
```python
print("=== Mina resmål ===")
lander = ["Italien", "Thailand", "Mexiko"]
print("Länder:", lander)
```

---

### Uppgift 2: Flygtider

**Uppgift:** Skapa en lista med fyra flygtider i timmar (heltal) och skriv ut listan.

**Exempel på körning:**
```text
=== Flygtider ===
Timmar: [2, 5, 10, 14]
```

**Facit:**
```python
print("=== Flygtider ===")
timmar = [2, 5, 10, 14]
print("Timmar:", timmar)
```

---

### Uppgift 3: Reseinfo

**Uppgift:** Skapa en lista med tre saker om en resa: stad (text), land (text) och antal dagar (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Reseinfo ===
Resa: ['Barcelona', 'Spanien', 7]
```

**Facit:**
```python
print("=== Reseinfo ===")
resa = ["Barcelona", "Spanien", 7]
print("Resa:", resa)
```

---

### Uppgift 4: Två städer

**Uppgift:** Fråga användaren om två städer med `input()`. Skapa en lista med de två städerna och skriv ut listan.

**Exempel på körning:**
```text
=== Mina städer ===
Stad 1: Paris
Stad 2: Rom
Din lista: ['Paris', 'Rom']
```

**Facit:**
```python
print("=== Mina städer ===")
stad1 = input("Stad 1: ")
stad2 = input("Stad 2: ")
stader = [stad1, stad2]
print("Din lista:", stader)
```

---

### Uppgift 5: Resebiljett

**Uppgift:** Fråga användaren om ett resmål med `input()` och antal dagar med `int(input())`. Skapa en lista med resmål (text) och dagar (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Resebiljett ===
Resmål: Lissabon
Antal dagar: 5
Din biljett: ['Lissabon', 5]
```

**Facit:**
```python
print("=== Resebiljett ===")
resmal = input("Resmål: ")
dagar = int(input("Antal dagar: "))
biljett = [resmal, dagar]
print(f"Din biljett: {biljett}")
```
