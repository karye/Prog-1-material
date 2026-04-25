# Träning inför prov 4b: listor

Här får du träna på samma moment som kommer på Prov 4b. Temat är **husdjur**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Mina husdjur

**Uppgift:** Skapa en lista med tre husdjur och skriv ut listan.

**Exempel på körning:**
```text
=== Mina husdjur ===
Djur: ['hund', 'katt', 'hamster']
```

**Facit:**
```python
print("=== Mina husdjur ===")
djur = ["hund", "katt", "hamster"]
print("Djur:", djur)
```

---

### Uppgift 2: Vikter

**Uppgift:** Skapa en lista med fyra djurvikter i kg (heltal) och skriv ut listan.

**Exempel på körning:**
```text
=== Djurens vikt ===
Vikter: [25, 4, 1, 8]
```

**Facit:**
```python
print("=== Djurens vikt ===")
vikter = [25, 4, 1, 8]
print("Vikter:", vikter)
```

---

### Uppgift 3: Husdjursinfo

**Uppgift:** Skapa en lista med tre saker om ett husdjur: namn (text), art (text) och ålder i år (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Husdjursinfo ===
Djur: ['Bella', 'hund', 3]
```

**Facit:**
```python
print("=== Husdjursinfo ===")
djur = ["Bella", "hund", 3]
print("Djur:", djur)
```

---

### Uppgift 4: Två djurnamn

**Uppgift:** Fråga användaren om två djurnamn med `input()`. Skapa en lista med de två namnen och skriv ut listan.

**Exempel på körning:**
```text
=== Mina djurnamn ===
Djurnamn 1: Molly
Djurnamn 2: Max
Din lista: ['Molly', 'Max']
```

**Facit:**
```python
print("=== Mina djurnamn ===")
namn1 = input("Djurnamn 1: ")
namn2 = input("Djurnamn 2: ")
namn = [namn1, namn2]
print("Din lista:", namn)
```

---

### Uppgift 5: Djurjournalen

**Uppgift:** Fråga användaren om djurets namn med `input()` och djurets vikt med `int(input())`. Skapa en lista med namn (text) och vikt (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Djurjournalen ===
Djurets namn: Luna
Vikt (kg): 6
Journal: ['Luna', 6]
```

**Facit:**
```python
print("=== Djurjournalen ===")
namn = input("Djurets namn: ")
vikt = int(input("Vikt (kg): "))
journal = [namn, vikt]
print(f"Journal: {journal}")
```
