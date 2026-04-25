# Träning inför prov 7b: funktioner

Här får du träna på samma moment som kommer på Prov 7b. Temat är **rymd**.

**Regler:**
* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

---

### Uppgift 1: Starta raketen

**Uppgift:** Skapa en funktion som heter `starta_raket()`. När funktionen körs ska den skriva ut texten `"Raketen är redo för start!"`. Funktionen ska inte ha några argument. Anropa funktionen en gång.

**Exempel på körning:**
```text
Raketen är redo för start!
```

**Facit:**
```python
def starta_raket():
    print("Raketen är redo för start!")

starta_raket()
```

---

### Uppgift 2: Nedräkning

**Uppgift:** Skapa en funktion som heter `pip()`. Funktionen ska skriva ut texten `"Pip!"`. Anropa funktionen **tre gånger i rad**.

**Exempel på körning:**
```text
Pip!
Pip!
Pip!
```

**Facit:**
```python
def pip():
    print("Pip!")

pip()
pip()
pip()
```

---

### Uppgift 3: Uppdrag i tre steg

**Uppgift:** Skapa tre olika funktioner för ett rymduppdrag:

1. `ta_av()` som skriver ut `"Raketen lyfter!"`
2. `kretsa()` som skriver ut `"Vi kretsar runt jorden..."`
3. `landa()` som skriver ut `"Landning lyckades!"`

Anropa alla tre i rätt ordning.

**Exempel på körning:**
```text
Raketen lyfter!
Vi kretsar runt jorden...
Landning lyckades!
```

**Facit:**
```python
def ta_av():
    print("Raketen lyfter!")

def kretsa():
    print("Vi kretsar runt jorden...")

def landa():
    print("Landning lyckades!")

ta_av()
kretsa()
landa()
```

---

### Uppgift 4: Hälsa astronaut

**Uppgift:** Skapa en funktion som heter `halsa_astronaut(namn)`. Funktionen ska ta emot **ett argument** och skriva ut en hälsning. Anropa funktionen med ett valfritt namn.

**Exempel på körning:**
```text
Välkommen ombord, Neil!
```

**Facit:**
```python
def halsa_astronaut(namn):
    print("Välkommen ombord,", namn + "!")

halsa_astronaut("Neil")
```

---

### Uppgift 5: Bränsleberäkning

**Uppgift:** Skapa en funktion som heter `berakna_bransle(distans, forbrukning)`. Funktionen ska ta emot **två argument**, multiplicera dem för att beräkna total bränsleåtgång och skriva ut resultatet med en **f-sträng**. Anropa funktionen med två valfria värden.

**Exempel på körning:**
```text
En resa på 500 ljusår kräver 2500 enheter bränsle.
```

**Facit:**
```python
def berakna_bransle(distans, forbrukning):
    totalt = distans * forbrukning
    print(f"En resa på {distans} ljusår kräver {totalt} enheter bränsle.")

berakna_bransle(500, 5)
```
