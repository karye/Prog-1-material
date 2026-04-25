# Träning inför prov 3b: while-loopar

Här får du träna på samma moment som kommer på Prov 3b. Temat är **affär och butik**.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: Butiken är öppen

**Uppgift:** Skriv ett program som skriver ut rubriken `"Välkommen till KodButiken!"` utanför loopen. Starta sedan en `while`-loop som skriver ut `"Butiken är öppen!"` om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Välkommen till KodButiken!
Butiken är öppen!
Butiken är öppen!
Butiken är öppen!
(... fortsätter ...)
```

**Facit:**
```python
print("Välkommen till KodButiken!")
while True:
    print("Butiken är öppen!")
```

---

### Uppgift 2: Skanna varor

**Uppgift:** Be användaren skriva in en vara **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut att varan skannas om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Vilken vara ska skannas? Mjölk
Skannar: Mjölk
Skannar: Mjölk
Skannar: Mjölk
(... fortsätter ...)
```

**Facit:**
```python
vara = input("Vilken vara ska skannas? ")
while True:
    print("Skannar:", vara)
```

---

### Uppgift 3: Välkommen kund

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett kundnamn och skriver ut en hälsning. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Öppnar kassan...
Kundens namn: Pia
Välkommen Pia
Kundens namn: Thomas
Välkommen Thomas
(... fortsätter ...)
```

**Facit:**
```python
print("Öppnar kassan...")
while True:
    namn = input("Kundens namn: ")
    print("Välkommen", namn)
```

---

### Uppgift 4: Stäng kassan

**Uppgift:** Skriv ett program med en `while`-loop som frågar efter ett kundnamn och skriver `"Välkommen"` plus namnet. Om användaren skriver `"stäng"` ska programmet skriva `"Kassan är stängd."` och avsluta loopen med `break`.

**Exempel på körning:**
```text
Kundens namn: Ida
Välkommen Ida
Kundens namn: Max
Välkommen Max
Kundens namn: stäng
Kassan är stängd.
```

**Facit:**
```python
while True:
    namn = input("Kundens namn: ")
    if namn == "stäng":
        print("Kassan är stängd.")
        break
    print("Välkommen", namn)
```

---

### Uppgift 5: Butiksmeny

**Uppgift:** Skriv ett program med en `while`-loop som visar en meny och väntar på ett val. På `1` skriv `"Erbjudande: 3 för 2 på alla varor"`. På `2` skriv `"Öppettider: 9-20 alla dagar"`. På `3` skriv `"Tack för ditt besök!"` och avsluta loopen. För andra val skriv `"Ogiltigt val."`.

**Exempel på körning:**
```text
=== Butiksmeny ===
1. Visa erbjudanden
2. Visa öppettider
3. Avsluta
Val: 2
Öppettider: 9-20 alla dagar

=== Butiksmeny ===
1. Visa erbjudanden
2. Visa öppettider
3. Avsluta
Val: 3
Tack för ditt besök!
```

**Facit:**
```python
while True:
    print("=== Butiksmeny ===")
    print("1. Visa erbjudanden")
    print("2. Visa öppettider")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Erbjudande: 3 för 2 på alla varor")
    elif val == "2":
        print("Öppettider: 9-20 alla dagar")
    elif val == "3":
        print("Tack för ditt besök!")
        break
    else:
        print("Ogiltigt val.")
```
