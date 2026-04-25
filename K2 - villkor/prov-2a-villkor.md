# Prov 2a: villkor

I det här provet testas din förmåga att styra programflödet med `if`, `elif` och `else`. Temat är **djur**.

---

### Uppgift 1: Hund eller inte?

**Uppgift:** Fråga användaren vilket djur de har. Om svaret är `"hund"` ska programmet skriva `"Voff! En hund!"`. Annars ska det skriva `"Inte en hund."`.

**Exempel på körning 1:**
```text
Vilket djur har du? hund
Voff! En hund!
```

**Exempel på körning 2:**
```text
Vilket djur har du? katt
Inte en hund.
```

**Facit:**
```python
djur = input("Vilket djur har du? ")
if djur == "hund":
    print("Voff! En hund!")
else:
    print("Inte en hund.")
```

---

### Uppgift 2: Stor eller liten?

**Uppgift:** Fråga användaren hur mycket djuret väger i kg. Om vikten är 20 eller mer ska programmet skriva `"Stort djur!"`. Annars ska det skriva `"Litet djur!"`.

**Exempel på körning 1:**
```text
Vikt (kg): 30
Stort djur!
```

**Exempel på körning 2:**
```text
Vikt (kg): 5
Litet djur!
```

**Facit:**
```python
vikt = int(input("Vikt (kg): "))
if vikt >= 20:
    print("Stort djur!")
else:
    print("Litet djur!")
```

---

### Uppgift 3: Vilket läte?

**Uppgift:** Fråga användaren vilket djur de har. Om det är `"hund"` skriv `"Voff!"`. Om det är `"katt"` skriv `"Mjau!"`. Annars skriv `"Okänt läte."`.

**Exempel på körning 1:**
```text
Djurart: hund
Voff!
```

**Exempel på körning 2:**
```text
Djurart: katt
Mjau!
```

**Exempel på körning 3:**
```text
Djurart: fisk
Okänt läte.
```

**Facit:**
```python
art = input("Djurart: ")
if art == "hund":
    print("Voff!")
elif art == "katt":
    print("Mjau!")
else:
    print("Okänt läte.")
```

---

### Uppgift 4: Livsfas

**Uppgift:** Fråga användaren hur gammalt djuret är i år. Skriv ut vilken livsfas djuret befinner sig i:
- 0–1 år: `"Bebis"`
- 2–5 år: `"Ung"`
- 6–10 år: `"Vuxen"`
- 11 år eller mer: `"Senior"`

**Exempel på körning 1:**
```text
Ålder (år): 1
Bebis
```

**Exempel på körning 2:**
```text
Ålder (år): 4
Ung
```

**Exempel på körning 3:**
```text
Ålder (år): 8
Vuxen
```

**Exempel på körning 4:**
```text
Ålder (år): 13
Senior
```

**Facit:**
```python
alder = int(input("Ålder (år): "))
if alder <= 1:
    print("Bebis")
elif alder <= 5:
    print("Ung")
elif alder <= 10:
    print("Vuxen")
else:
    print("Senior")
```

---

### Uppgift 5: Djurpass

**Uppgift:** Fråga användaren om djurets art och vikt i kg. Om djuret är `"hund"`: kontrollera vikten — om 20 kg eller mer skriv `"Stor hund, behöver stort utrymme."`, annars skriv `"Liten hund, passar i lägenhet."`. Om djuret inte är `"hund"` ska programmet med en **f-sträng** skriva ut att det behövs mer info om det djuret.

**Exempel på körning 1:**
```text
Djurets art: hund
Vikt (kg): 25
Stor hund, behöver stort utrymme.
```

**Exempel på körning 2:**
```text
Djurets art: hund
Vikt (kg): 8
Liten hund, passar i lägenhet.
```

**Exempel på körning 3:**
```text
Djurets art: kanin
Vikt (kg): 2
Kontakta oss för mer info om kanin.
```

**Facit:**
```python
art = input("Djurets art: ")
vikt = int(input("Vikt (kg): "))
if art == "hund":
    if vikt >= 20:
        print("Stor hund, behöver stort utrymme.")
    else:
        print("Liten hund, passar i lägenhet.")
else:
    print(f"Kontakta oss för mer info om {art}.")
```
