# Träning inför prov 3c: while-loopar

Här får du träna på samma moment som kommer på Prov 3c. Temat är **skola**.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: Lektionen pågår

**Uppgift:** Skriv ett program som skriver ut rubriken `"=== Lektion startar ==="` utanför loopen. Starta sedan en `while`-loop som skriver ut `"Lektionen pågår..."` om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
=== Lektion startar ===
Lektionen pågår...
Lektionen pågår...
Lektionen pågår...
(... fortsätter ...)
```

**Facit:**
```python
print("=== Lektion startar ===")
while True:
    print("Lektionen pågår...")
```

---

### Uppgift 2: Elevens svar

**Uppgift:** Be användaren skriva ett svar **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut att svaret kontrolleras om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Skriv ditt svar: 42
Kontrollerar svar: 42
Kontrollerar svar: 42
(... fortsätter ...)
```

**Facit:**
```python
svar = input("Skriv ditt svar: ")
while True:
    print("Kontrollerar svar:", svar)
```

---

### Uppgift 3: Frågesport

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett elevnamn och skriver ut att eleven är anmäld. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
=== Frågesport ===
Elevens namn: Lena
Lena är anmäld!
Elevens namn: Omar
Omar är anmäld!
(... fortsätter ...)
```

**Facit:**
```python
print("=== Frågesport ===")
while True:
    namn = input("Elevens namn: ")
    print(namn, "är anmäld!")
```

---

### Uppgift 4: Avsluta lektionen

**Uppgift:** Skriv ett program med en `while`-loop som frågar efter ett ämne och skriver ut att ämnet är klart. Om användaren skriver `"avsluta"` ska programmet skriva `"Lektionen är slut. Bra jobbat!"` och avsluta loopen med `break`.

**Exempel på körning:**
```text
Ämne: matte
matte är klart!
Ämne: svenska
svenska är klart!
Ämne: avsluta
Lektionen är slut. Bra jobbat!
```

**Facit:**
```python
while True:
    amne = input("Ämne: ")
    if amne == "avsluta":
        print("Lektionen är slut. Bra jobbat!")
        break
    print(amne, "är klart!")
```

---

### Uppgift 5: Skolmeny

**Uppgift:** Skriv ett program med en `while`-loop som visar en meny och väntar på ett val. På `1` skriv `"Schema: Matte, Svenska, Idrott"`. På `2` skriv `"Läxa: Läs kapitel 3"`. På `3` skriv `"Hej då, ha en bra dag!"` och avsluta loopen. För andra val skriv `"Okänt val."`.

**Exempel på körning:**
```text
=== Skolmeny ===
1. Visa schema
2. Visa läxa
3. Avsluta
Val: 1
Schema: Matte, Svenska, Idrott

=== Skolmeny ===
1. Visa schema
2. Visa läxa
3. Avsluta
Val: 3
Hej då, ha en bra dag!
```

**Facit:**
```python
while True:
    print("=== Skolmeny ===")
    print("1. Visa schema")
    print("2. Visa läxa")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Schema: Matte, Svenska, Idrott")
    elif val == "2":
        print("Läxa: Läs kapitel 3")
    elif val == "3":
        print("Hej då, ha en bra dag!")
        break
    else:
        print("Okänt val.")
```
