# Prov 7a: funktioner i Python

I det här provet ska du visa att du kan skapa egna funktioner, anropa dem i rätt ordning och skicka in information (argument) till dem.

**Regler:**

* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

---

### Uppgift 1: skapa en enkel funktion och testa

**Uppgift:** Skapa en funktion som heter `halsa()`. När funktionen körs ska den skriva ut texten "Hej och välkommen!". Funktionen ska inte ha några argument. Glöm inte att anropa (köra) funktionen efter att du skapat den för att testa att den fungerar.

**Exempel på körning:**

```text
Hej och välkommen!
```

**Facit:**

```python
def halsa():
    print("Hej och välkommen!")

halsa()
```

---

### Uppgift 2: använda en funktion flera gånger

**Uppgift:** Skapa en funktion som heter `hurra()`. Funktionen ska skriva ut texten "Hurra!". Anropa därefter funktionen **tre gånger i rad** så att texten skrivs ut tre gånger.

**Exempel på körning:**

```text
Hurra!
Hurra!
Hurra!
```

**Facit:**

```python
def hurra():
    print("Hurra!")

hurra()
hurra()
hurra()
```

---

### Uppgift 3: flera funktioner i rätt följd

**Uppgift:** Skapa tre olika funktioner för att spela ett spel:

1. `starta()` som skriver ut "Startar spelet..."
2. `spela()` som skriver ut "Spelet är igång!"
3. `avsluta()` som skriver ut "Avslutar och sparar..."

När du har skapat alla tre funktionerna ska du anropa dem i en logisk följd så att texten skrivs ut i rätt ordning.

**Exempel på körning:**

```text
Startar spelet...
Spelet är igång!
Avslutar och sparar...
```

**Facit:**

```python
def starta():
    print("Startar spelet...")

def spela():
    print("Spelet är igång!")

def avsluta():
    print("Avslutar och sparar...")

starta()
spela()
avsluta()
```

---

### Uppgift 4: funktion med ett namn (argument)

**Uppgift:** Skapa en funktion som heter `personlig_halsning(namn)`. Funktionen ska ta emot **ett argument** (ett namn) och skriva ut en trevlig hälsning där namnet är med. Anropa sedan funktionen och skicka in ett valfritt namn i parentesen.

**Exempel på körning:**

```text
Hej Kalle, hoppas du får en bra dag!
```

**Facit:**

```python
def personlig_halsning(namn):
    print(f"Hej {namn}, hoppas du får en bra dag!")

personlig_halsning("Kalle")
```

---

### Uppgift 5: mata monstret (två argument och beräkning)

**Uppgift:** Skapa en funktion som heter `mata_monster(antal_monster, kakor)`. Funktionen ska ta emot **två argument** (siffror), multiplicera dem med varandra för att räkna ut hur många kakor som går åt totalt, och skriva ut en rolig mening med svaret. Anropa sedan funktionen med två valfria siffror.

**Exempel på körning:**

```text
Du matade 3 monster med 5 kakor var. Totalt slukade de 15 kakor... BURRRRP!
```

**Facit:**

```python
def mata_monster(antal_monster, kakor):
    totalt = antal_monster * kakor
    print(f"Du matade {antal_monster} monster med {kakor} kakor var. Totalt slukade de {totalt} kakor... BURRRRP!")

mata_monster(3, 5)
```
