# Prov 3b: while-loopar

I det här provet testas din förmåga att använda `while`-loopar. Temat är **restaurang**.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: Öppen skylt

**Uppgift:** Skriv ett program som skriver ut rubriken `"Restaurang Koden"` utanför loopen. Starta sedan en `while`-loop som skriver ut `"Vi är öppna!"` om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Restaurang Koden
Vi är öppna!
Vi är öppna!
Vi är öppna!
(... fortsätter ...)
```

**Facit:**
```python
print("Restaurang Koden")
while True:
    print("Vi är öppna!")
```

---

### Uppgift 2: Ta emot beställningar

**Uppgift:** Be användaren skriva en beställning **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut samma beställning om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Vad vill du beställa? Pizza
Köket förbereder: Pizza
Köket förbereder: Pizza
Köket förbereder: Pizza
(... fortsätter ...)
```

**Facit:**
```python
bestallning = input("Vad vill du beställa? ")
while True:
    print("Köket förbereder:", bestallning)
```

---

### Uppgift 3: Hälsa gäster

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett namn och direkt skriver ut en hälsning. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Välkommen!
Gästens namn: Maria
God kväll Maria
Gästens namn: Jonas
God kväll Jonas
Gästens namn: Lin
God kväll Lin
(... fortsätter ...)
```

**Facit:**
```python
print("Välkommen!")
while True:
    namn = input("Gästens namn: ")
    print("God kväll", namn)
```

---

### Uppgift 4: Stäng restaurangen

**Uppgift:** Skriv ett program med en `while`-loop som frågar efter ett gästnamn och skriver `"God kväll"` plus namnet. Om användaren skriver `"stäng"` ska programmet skriva `"Restaurangen stänger nu."` och avsluta loopen med `break`.

**Exempel på körning:**
```text
Gästens namn: Anna
God kväll Anna
Gästens namn: Erik
God kväll Erik
Gästens namn: stäng
Restaurangen stänger nu.
```

**Facit:**
```python
while True:
    namn = input("Gästens namn: ")
    if namn == "stäng":
        print("Restaurangen stänger nu.")
        break
    print("God kväll", namn)
```

---

### Uppgift 5: Restaurangmeny

**Uppgift:** Skriv ett program med en `while`-loop som visar en meny och väntar på ett val. På `1` skriv `"Dagens rätt: Pasta bolognese"`. På `2` skriv `"Dryck: Vatten eller juice"`. På `3` skriv `"Hejdå och välkommen åter!"` och avsluta loopen. För andra val skriv `"Ogiltigt val, försök igen."`.

**Exempel på körning:**
```text
=== Meny ===
1. Visa dagens rätt
2. Visa drycker
3. Avsluta
Val: 1
Dagens rätt: Pasta bolognese

=== Meny ===
1. Visa dagens rätt
2. Visa drycker
3. Avsluta
Val: 3
Hejdå och välkommen åter!
```

**Facit:**
```python
while True:
    print("=== Meny ===")
    print("1. Visa dagens rätt")
    print("2. Visa drycker")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Dagens rätt: Pasta bolognese")
    elif val == "2":
        print("Dryck: Vatten eller juice")
    elif val == "3":
        print("Hejdå och välkommen åter!")
        break
    else:
        print("Ogiltigt val, försök igen.")
```
