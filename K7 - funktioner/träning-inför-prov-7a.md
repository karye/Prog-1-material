# Träning inför prov 7a: funktioner

Här får du träna på samma moment som kommer på Prov 7a. Temat är **café och fika**.

**Regler:**
* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

---

### Uppgift 1: Öppna caféet

**Uppgift:** Skapa en funktion som heter `oppna()`. När funktionen körs ska den skriva ut texten `"Caféet är öppet!"`. Funktionen ska inte ha några argument. Anropa funktionen en gång.

**Exempel på körning:**
```text
Caféet är öppet!
```

**Facit:**
```python
def oppna():
    print("Caféet är öppet!")

oppna()
```

---

### Uppgift 2: Servera fika

**Uppgift:** Skapa en funktion som heter `servera()`. Funktionen ska skriva ut texten `"Här kommer fikat!"`. Anropa funktionen **tre gånger i rad**.

**Exempel på körning:**
```text
Här kommer fikat!
Här kommer fikat!
Här kommer fikat!
```

**Facit:**
```python
def servera():
    print("Här kommer fikat!")

servera()
servera()
servera()
```

---

### Uppgift 3: Fikarast i tre steg

**Uppgift:** Skapa tre olika funktioner för en fikarast:

1. `hamta_kaffe()` som skriver ut `"Hämtar kaffe..."`
2. `ta_bulle()` som skriver ut `"Tar en kanelbulle..."`
3. `satt_sig()` som skriver ut `"Sätter sig ner och njuter!"`

Anropa alla tre i rätt ordning.

**Exempel på körning:**
```text
Hämtar kaffe...
Tar en kanelbulle...
Sätter sig ner och njuter!
```

**Facit:**
```python
def hamta_kaffe():
    print("Hämtar kaffe...")

def ta_bulle():
    print("Tar en kanelbulle...")

def satt_sig():
    print("Sätter sig ner och njuter!")

hamta_kaffe()
ta_bulle()
satt_sig()
```

---

### Uppgift 4: Beställning med namn

**Uppgift:** Skapa en funktion som heter `bestall(dryck)`. Funktionen ska ta emot **ett argument** och skriva ut en beställning. Anropa funktionen med en valfri dryck.

**Exempel på körning:**
```text
Du beställde: cappuccino
```

**Facit:**
```python
def bestall(dryck):
    print("Du beställde:", dryck)

bestall("cappuccino")
```

---

### Uppgift 5: Kvitto

**Uppgift:** Skapa en funktion som heter `kvitto(vara, pris)`. Funktionen ska ta emot **två argument**, multiplicera dem för att räkna ut totalkostnaden (antal × pris) och skriva ut en rad med en **f-sträng**. Anropa funktionen med två valfria värden.

**Exempel på körning:**
```text
3 st kaffe á 35 kr = 105 kr totalt.
```

**Facit:**
```python
def kvitto(antal, pris):
    total = antal * pris
    print(f"{antal} st kaffe á {pris} kr = {total} kr totalt.")

kvitto(3, 35)
```
