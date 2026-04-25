# Träning inför prov 2a: villkor

Här får du träna på samma moment som kommer på Prov 2a. Temat är **mat och restaurang**.

---

### Uppgift 1: Vegetarisk eller inte?

**Uppgift:** Fråga användaren vilken rätt de vill ha. Om svaret är `"vegetarisk"` ska programmet skriva `"Bra val, nyttigt och gott!"`. Annars ska det skriva `"En klassiker!"`.

**Exempel på körning 1:**
```text
Vilken rätt vill du ha? vegetarisk
Bra val, nyttigt och gott!
```

**Exempel på körning 2:**
```text
Vilken rätt vill du ha? pizza
En klassiker!
```

**Facit:**
```python
ratt = input("Vilken rätt vill du ha? ")
if ratt == "vegetarisk":
    print("Bra val, nyttigt och gott!")
else:
    print("En klassiker!")
```

---

### Uppgift 2: Dyrt eller billigt?

**Uppgift:** Fråga användaren hur mycket rätten kostar. Om priset är 100 kr eller mer ska programmet skriva `"Lyxig middag!"`. Annars ska det skriva `"Prisvärt!"`.

**Exempel på körning 1:**
```text
Pris (kr): 150
Lyxig middag!
```

**Exempel på körning 2:**
```text
Pris (kr): 75
Prisvärt!
```

**Facit:**
```python
pris = int(input("Pris (kr): "))
if pris >= 100:
    print("Lyxig middag!")
else:
    print("Prisvärt!")
```

---

### Uppgift 3: Vilket kök?

**Uppgift:** Fråga användaren vilken typ av mat de vill ha. Om det är `"italiensk"` skriv `"Pasta och pizza väntar!"`. Om det är `"asiatisk"` skriv `"Sushi och nudlar!"`. Annars skriv `"Vi fixar något gott!"`.

**Exempel på körning 1:**
```text
Typ av mat: italiensk
Pasta och pizza väntar!
```

**Exempel på körning 2:**
```text
Typ av mat: asiatisk
Sushi och nudlar!
```

**Exempel på körning 3:**
```text
Typ av mat: mexikansk
Vi fixar något gott!
```

**Facit:**
```python
typ = input("Typ av mat: ")
if typ == "italiensk":
    print("Pasta och pizza väntar!")
elif typ == "asiatisk":
    print("Sushi och nudlar!")
else:
    print("Vi fixar något gott!")
```

---

### Uppgift 4: Prisnivå

**Uppgift:** Fråga användaren hur mycket de vill betala. Skriv ut vilken prisnivå det är:
- Under 50 kr: `"Snabbmat"`
- 50–99 kr: `"Enkelt och bra"`
- 100–199 kr: `"Restaurangnivå"`
- 200 kr eller mer: `"Fine dining"`

**Exempel på körning 1:**
```text
Budget (kr): 35
Snabbmat
```

**Exempel på körning 2:**
```text
Budget (kr): 80
Enkelt och bra
```

**Exempel på körning 3:**
```text
Budget (kr): 140
Restaurangnivå
```

**Exempel på körning 4:**
```text
Budget (kr): 250
Fine dining
```

**Facit:**
```python
budget = int(input("Budget (kr): "))
if budget < 50:
    print("Snabbmat")
elif budget < 100:
    print("Enkelt och bra")
elif budget < 200:
    print("Restaurangnivå")
else:
    print("Fine dining")
```

---

### Uppgift 5: Bordsbokning

**Uppgift:** Fråga användaren om mattyp och antal gäster. Om mattypen är `"sushi"`: kontrollera antal gäster — om 4 eller fler skriv `"Vi bokar ett stort bord för er!"`, annars skriv `"Litet bord vid fönstret!"`. Om mattypen inte är `"sushi"` ska programmet med en **f-sträng** skriva att det ordnas ett bord för den mattypen.

**Exempel på körning 1:**
```text
Mattyp: sushi
Antal gäster: 5
Vi bokar ett stort bord för er!
```

**Exempel på körning 2:**
```text
Mattyp: sushi
Antal gäster: 2
Litet bord vid fönstret!
```

**Exempel på körning 3:**
```text
Mattyp: pizza
Antal gäster: 3
Vi ordnar ett bord för pizza!
```

**Facit:**
```python
mat = input("Mattyp: ")
gaster = int(input("Antal gäster: "))
if mat == "sushi":
    if gaster >= 4:
        print("Vi bokar ett stort bord för er!")
    else:
        print("Litet bord vid fönstret!")
else:
    print(f"Vi ordnar ett bord för {mat}!")
```
