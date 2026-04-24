# Prov 6c: funktioner i Python

I det här provet ska du visa att du kan skapa egna funktioner, anropa dem i rätt ordning och skicka in information (argument) till dem.

**Regler:**

* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

### Uppgift 1: skapa en enkel funktion och testa

**Uppgift:** Skapa en funktion som heter `hejaklack()`. När funktionen körs ska den skriva ut texten "Kämpa, kämpa, ge aldrig upp!". Funktionen ska inte ha några argument. Glöm inte att anropa (köra) funktionen efter att du skapat den för att testa att den fungerar.

**Exempel på körning:**

```text
Kämpa, kämpa, ge aldrig upp!
```

**Facit:**

```python
def hejaklack():
    print("Kämpa, kämpa, ge aldrig upp!")

hejaklack()
```

### Uppgift 2: använda en funktion flera gånger

**Uppgift:** Skapa en funktion som heter `trollformel()`. Funktionen ska skriva ut texten "Abrakadabra!". Anropa därefter funktionen **tre gånger i rad** så att den magiska formeln skrivs ut tre gånger.

**Exempel på körning:**

```text
Abrakadabra!
Abrakadabra!
Abrakadabra!
```

**Facit:**

```python
def trollformel():
    print("Abrakadabra!")

trollformel()
trollformel()
trollformel()
```

### Uppgift 3: flera funktioner i rätt följd

**Uppgift:** Skapa tre olika funktioner för en morgonrutin:

1. `vakna()` som skriver ut "Stänger av väckarklockan..."
2. `ata_frukost()` som skriver ut "Äter mackor och dricker juice..."
3. `ga_till_skolan()` som skriver ut "Tar på mig skorna och går hemifrån..."

När du har skapat alla tre funktionerna ska du anropa dem i en logisk följd så att morgonen görs i rätt ordning.

**Exempel på körning:**

```text
Stänger av väckarklockan...
Äter mackor och dricker juice...
Tar på mig skorna och går hemifrån...
```

**Facit:**

```python
def vakna():
    print("Stänger av väckarklockan...")

def ata_frukost():
    print("Äter mackor och dricker juice...")

def ga_till_skolan():
    print("Tar på mig skorna och går hemifrån...")

vakna()
ata_frukost()
ga_till_skolan()
```

### Uppgift 4: funktion med en spelare (argument)

**Uppgift:** Skapa en funktion som heter `valkommen_spelare(namn)`. Funktionen ska ta emot **ett argument** (ett namn) och skriva ut en mening som välkomnar spelaren till nivå 1. Anropa sedan funktionen och skicka in ett valfritt namn i parentesen.

**Exempel på körning:**

```text
Välkommen till nivå 1, Luigi!
```

**Facit:**

```python
def valkommen_spelare(namn):
    print(f"Välkommen till nivå 1, {namn}!")

valkommen_spelare("Luigi")
```

### Uppgift 5: funktion för biobesök (två argument)

**Uppgift:** Skapa en funktion som heter `biobiljetter(antal, pris)`. Funktionen ska ta emot **två argument** (siffror), multiplicera dem med varandra för att räkna ut den totala kostnaden och skriva ut en mening med svaret. Anropa sedan funktionen med två valfria siffror.

**Exempel på körning:**

```text
Du har köpt 4 biljetter. Totalt pris: 520 kr.
```

**Facit:**

```python
def biobiljetter(antal, pris):
    total = antal * pris
    print(f"Du har köpt {antal} biljetter. Totalt pris: {total} kr.")

biobiljetter(4, 130)
```
