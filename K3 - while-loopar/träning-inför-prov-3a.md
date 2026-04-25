# Träning inför prov 3a: while-loopar

Här får du träna på samma moment som kommer på Prov 3a. Temat är **djurparken**.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: Djurparken är öppen

**Uppgift:** Skriv ett program som skriver ut rubriken `----- Djurparken -----` utanför loopen. Starta sedan en `while`-loop som skriver ut `Välkommen till djurparken!` om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
----- Djurparken -----
Välkommen till djurparken!
Välkommen till djurparken!
Välkommen till djurparken!
(... fortsätter ...)
```

**Facit:**
```python
print("----- Djurparken -----")
while True:
    print("Välkommen till djurparken!")
```

---

### Uppgift 2: Annonsera ett djur

**Uppgift:** Be användaren skriva ett djurnamn **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut samma djurnamn om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Skriv ett djur: Lejon
Visar djur...
Lejon
Lejon
Lejon
(... fortsätter ...)
```

**Facit:**
```python
djur = input("Skriv ett djur: ")
print("Visar djur...")
while True:
    print(djur)
```

---

### Uppgift 3: Hälsa besökare

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett besökarnamn och skriver ut en hälsning. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Portalen öppen!
Besökarens namn: Maja
Hej Maja
Besökarens namn: Kalle
Hej Kalle
(... fortsätter ...)
```

**Facit:**
```python
print("Portalen öppen!")
while True:
    namn = input("Besökarens namn: ")
    print("Hej", namn)
```

---

### Uppgift 4: Stäng portalen

**Uppgift:** Skriv ett program med en `while`-loop som frågar efter ett besökarnamn och skriver `Hej` plus namnet. Om användaren skriver `q` ska programmet skriva `Portalen stängs` och avsluta loopen med `break`.

**Exempel på körning:**
```text
Besökarlista:
Besökarens namn (q för att sluta): Maja
Hej Maja
Besökarens namn (q för att sluta): Kalle
Hej Kalle
Besökarens namn (q för att sluta): q
Portalen stängs
```

**Facit:**
```python
print("Besökarlista:")
while True:
    namn = input("Besökarens namn (q för att sluta): ")
    if namn == "q":
        print("Portalen stängs")
        break
    print("Hej", namn)
```

---

### Uppgift 5: Djurparksmeny

**Uppgift:** Skriv ett program med en `while`-loop som visar en meny och väntar på ett val. På `1` skriv ut `Dagens matning: Lejon kl 14:00`. På `2` skriv ut `Karta: Lejon - Giraff - Elefant`. På `3` skriv ut `Tack för besöket!` och avsluta loopen. För andra val skriv `Fel val`.

**Exempel på körning:**
```text
Djurparksmeny
=============

1. Visa dagens matning
2. Visa karta
3. Avsluta
Val: 1
Dagens matning: Lejon kl 14:00

1. Visa dagens matning
2. Visa karta
3. Avsluta
Val: 3
Tack för besöket!
```

**Facit:**
```python
print("Djurparksmeny")
print("=============")
while True:
    print()
    print("1. Visa dagens matning")
    print("2. Visa karta")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Dagens matning: Lejon kl 14:00")
    elif val == "2":
        print("Karta: Lejon - Giraff - Elefant")
    elif val == "3":
        print("Tack för besöket!")
        break
    else:
        print("Fel val")
```
