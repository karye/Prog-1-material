# Prov 2b: villkor

I det här provet testas din förmåga att styra programflödet med `if`, `elif` och `else`. Temat är **väder**.

---

### Uppgift 1: Sol eller inte?

**Uppgift:** Fråga användaren vilket väder det är. Om svaret är `"sol"` ska programmet skriva `"Perfekt väder!"`. Annars ska det skriva `"Ta med ett paraply."`.

**Exempel på körning 1:**
```text
Vilket väder är det? sol
Perfekt väder!
```

**Exempel på körning 2:**
```text
Vilket väder är det? regn
Ta med ett paraply.
```

**Facit:**
```python
vader = input("Vilket väder är det? ")
if vader == "sol":
    print("Perfekt väder!")
else:
    print("Ta med ett paraply.")
```

---

### Uppgift 2: Varmt eller kallt?

**Uppgift:** Fråga användaren efter temperaturen i grader. Om temperaturen är 20 eller mer ska programmet skriva `"Varmt ute!"`. Annars ska det skriva `"Lite kyligt."`.

**Exempel på körning 1:**
```text
Temperatur (grader): 24
Varmt ute!
```

**Exempel på körning 2:**
```text
Temperatur (grader): 12
Lite kyligt.
```

**Facit:**
```python
temp = int(input("Temperatur (grader): "))
if temp >= 20:
    print("Varmt ute!")
else:
    print("Lite kyligt.")
```

---

### Uppgift 3: Vad ska man ha på sig?

**Uppgift:** Fråga användaren vilket väder det är. Om det är `"sol"` skriv `"Ta på dig solglasögon."`. Om det är `"regn"` skriv `"Ta på dig regnkläder."`. Annars skriv `"Klä dig i lager."`.

**Exempel på körning 1:**
```text
Väder: sol
Ta på dig solglasögon.
```

**Exempel på körning 2:**
```text
Väder: regn
Ta på dig regnkläder.
```

**Exempel på körning 3:**
```text
Väder: snö
Klä dig i lager.
```

**Facit:**
```python
vader = input("Väder: ")
if vader == "sol":
    print("Ta på dig solglasögon.")
elif vader == "regn":
    print("Ta på dig regnkläder.")
else:
    print("Klä dig i lager.")
```

---

### Uppgift 4: Temperaturzon

**Uppgift:** Fråga användaren efter temperaturen i grader. Skriv ut vilken zon det är:
- Under 0: `"Minusgrader, frys varning!"`
- 0–9: `"Kallt"`
- 10–19: `"Svalt"`
- 20 eller mer: `"Varmt"`

**Exempel på körning 1:**
```text
Temperatur: -3
Minusgrader, frys varning!
```

**Exempel på körning 2:**
```text
Temperatur: 5
Kallt
```

**Exempel på körning 3:**
```text
Temperatur: 14
Svalt
```

**Exempel på körning 4:**
```text
Temperatur: 27
Varmt
```

**Facit:**
```python
temp = int(input("Temperatur: "))
if temp < 0:
    print("Minusgrader, frys varning!")
elif temp < 10:
    print("Kallt")
elif temp < 20:
    print("Svalt")
else:
    print("Varmt")
```

---

### Uppgift 5: Väderrapport

**Uppgift:** Fråga användaren om stad och väder. Om staden är `"Stockholm"`: kontrollera vädret — om det är `"sol"` skriv `"Ovanligt fint i Stockholm idag!"`, annars skriv `"Typiskt Stockholm-väder."`. Om staden inte är `"Stockholm"` ska programmet med en **f-sträng** skriva ut en enkel hälsning från den staden.

**Exempel på körning 1:**
```text
Stad: Stockholm
Väder: sol
Ovanligt fint i Stockholm idag!
```

**Exempel på körning 2:**
```text
Stad: Stockholm
Väder: regn
Typiskt Stockholm-väder.
```

**Exempel på körning 3:**
```text
Stad: Malmö
Väder: sol
Hej från Malmö!
```

**Facit:**
```python
stad = input("Stad: ")
vader = input("Väder: ")
if stad == "Stockholm":
    if vader == "sol":
        print("Ovanligt fint i Stockholm idag!")
    else:
        print("Typiskt Stockholm-väder.")
else:
    print(f"Hej från {stad}!")
```
