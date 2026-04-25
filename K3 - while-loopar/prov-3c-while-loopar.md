# Prov 3c: while-loopar

I det här provet testas din förmåga att använda `while`-loopar. Temat är **spel**.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: Spelet körs

**Uppgift:** Skriv ett program som skriver ut rubriken `"=== Spelet startar ==="` utanför loopen. Starta sedan en `while`-loop som skriver ut `"Spelet körs..."` om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
=== Spelet startar ===
Spelet körs...
Spelet körs...
Spelet körs...
(... fortsätter ...)
```

**Facit:**
```python
print("=== Spelet startar ===")
while True:
    print("Spelet körs...")
```

---

### Uppgift 2: Spelarens drag

**Uppgift:** Be användaren skriva ett drag **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut att draget utförs om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Skriv ett drag: hoppa
Utför drag: hoppa
Utför drag: hoppa
Utför drag: hoppa
(... fortsätter ...)
```

**Facit:**
```python
drag = input("Skriv ett drag: ")
while True:
    print("Utför drag:", drag)
```

---

### Uppgift 3: Välj karaktär

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett karaktärsnamn och skriver ut att karaktären väljs. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
=== Karaktärsval ===
Skriv karaktärens namn: Zelda
Zelda väljs!
Skriv karaktärens namn: Link
Link väljs!
(... fortsätter ...)
```

**Facit:**
```python
print("=== Karaktärsval ===")
while True:
    namn = input("Skriv karaktärens namn: ")
    print(namn, "väljs!")
```

---

### Uppgift 4: Game over

**Uppgift:** Skriv ett program med en `while`-loop som frågar efter ett drag och skriver ut att draget utförs. Om användaren skriver `"avsluta"` ska programmet skriva `"Game over!"` och avsluta loopen med `break`.

**Exempel på körning:**
```text
Drag: spring
Utför: spring
Drag: hoppa
Utför: hoppa
Drag: avsluta
Game over!
```

**Facit:**
```python
while True:
    drag = input("Drag: ")
    if drag == "avsluta":
        print("Game over!")
        break
    print("Utför:", drag)
```

---

### Uppgift 5: Spelstyrning

**Uppgift:** Skriv ett program med en `while`-loop som visar en styrning och väntar på ett val. På `1` skriv `"Spelaren rör sig framåt."`. På `2` skriv `"Spelaren hoppar."`. På `3` skriv `"Spelet avslutas. Tack för att du spelade!"` och avsluta loopen. För andra val skriv `"Okänt kommando."`.

**Exempel på körning:**
```text
=== Styrning ===
1. Gå framåt
2. Hoppa
3. Avsluta
Val: 2
Spelaren hoppar.

=== Styrning ===
1. Gå framåt
2. Hoppa
3. Avsluta
Val: 3
Spelet avslutas. Tack för att du spelade!
```

**Facit:**
```python
while True:
    print("=== Styrning ===")
    print("1. Gå framåt")
    print("2. Hoppa")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Spelaren rör sig framåt.")
    elif val == "2":
        print("Spelaren hoppar.")
    elif val == "3":
        print("Spelet avslutas. Tack för att du spelade!")
        break
    else:
        print("Okänt kommando.")
```
