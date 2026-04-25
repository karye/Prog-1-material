# Prov 7b: funktioner i Python

I det här provet ska du visa att du kan skapa egna funktioner, anropa dem i rätt ordning och skicka in information (argument) till dem.

**Regler:**

* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

---

### Uppgift 1: skapa en enkel funktion och testa

**Uppgift:** Skapa en funktion som heter `vaderprognos()`. När funktionen körs ska den skriva ut texten "Idag blir det strålande sol!". Funktionen ska inte ha några argument. Glöm inte att anropa (köra) funktionen efter att du skapat den för att testa att den fungerar.

**Exempel på körning:**

```text
Idag blir det strålande sol!
```

**Facit:**

```python
def vaderprognos():
    print("Idag blir det strålande sol!")

vaderprognos()
```

---

### Uppgift 2: använda en funktion flera gånger

**Uppgift:** Skapa en funktion som heter `larm()`. Funktionen ska skriva ut texten "Varning! Systemfel!". Anropa därefter funktionen **tre gånger i rad** så att varningen skrivs ut tre gånger.

**Exempel på körning:**

```text
Varning! Systemfel!
Varning! Systemfel!
Varning! Systemfel!
```

**Facit:**

```python
def larm():
    print("Varning! Systemfel!")

larm()
larm()
larm()
```

---

### Uppgift 3: flera funktioner i rätt följd

**Uppgift:** Skapa tre olika funktioner för att baka en tårta:

1. `baka_botten()` som skriver ut "Bakar en fluffig tårtbotten..."
2. `blanda_fyllning()` som skriver ut "Blandar sylt och vaniljkräm..."
3. `dekorera()` som skriver ut "Lägger på grädde och bär..."

När du har skapat alla tre funktionerna ska du anropa dem i en logisk följd så att tårtan görs i rätt ordning.

**Exempel på körning:**

```text
Bakar en fluffig tårtbotten...
Blandar sylt och vaniljkräm...
Lägger på grädde och bär...
```

**Facit:**

```python
def baka_botten():
    print("Bakar en fluffig tårtbotten...")

def blanda_fyllning():
    print("Blandar sylt och vaniljkräm...")

def dekorera():
    print("Lägger på grädde och bär...")

baka_botten()
blanda_fyllning()
dekorera()
```

---

### Uppgift 4: funktion med ett husdjur (argument)

**Uppgift:** Skapa en funktion som heter `klappa_djur(djur)`. Funktionen ska ta emot **ett argument** (ett djur) och skriva ut en mening där djuret är med. Anropa sedan funktionen och skicka in ett valfritt djur i parentesen.

**Exempel på körning:**

```text
Du klappar din mysiga hund.
```

**Facit:**

```python
def klappa_djur(djur):
    print(f"Du klappar din mysiga {djur}.")

klappa_djur("hund")
```

---

### Uppgift 5: funktion för beräkning av kvitto (två argument)

**Uppgift:** Skapa en funktion som heter `kvitto(pris, antal)`. Funktionen ska ta emot **två argument** (siffror), multiplicera dem med varandra för att få fram totalkostnaden och skriva ut en mening med svaret. Anropa sedan funktionen med två valfria siffror.

**Exempel på körning:**

```text
Totalt att betala: 150 kr
```

**Facit:**

```python
def kvitto(pris, antal):
    total = pris * antal
    print(f"Totalt att betala: {total} kr")

kvitto(50, 3)
```
