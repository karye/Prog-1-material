# Prov 1b: Input, print och variabler

I det här provet testas din förmåga att skriva ut text till skärmen, hämta information från användaren och spara i variabler, samt bygga meningar med f-strängar. Temat för provet är **café och restaurang**.

---

### Uppgift 1: Välkomstskylt

**Uppgift:** Skriv ett program som använder `print()` två gånger. Programmet ska först skriva ut en rubrik för caféet, och sedan en välkomstmening på raden under.

**Exempel på körning:**
```text
Välkommen till Kodcaféet!
Här serverar vi stans bästa bullar.
```

**Facit:**
```python
print("Välkommen till Kodcaféet!")
print("Här serverar vi stans bästa bullar.")
```

---

### Uppgift 2: Kvittoutskrift

**Uppgift:** Skriv ett program som skriver ut ett kvitto på fyra rader med hjälp av `print()`. Det ska se ut exakt som i exemplet nedan, med bindestreck på översta och nedersta raden.

**Exempel på körning:**
```text
----------------
Kaffe: 35 kr
Kanelbulle: 25 kr
----------------
```

**Facit:**
```python
print("----------------")
print("Kaffe: 35 kr")
print("Kanelbulle: 25 kr")
print("----------------")
```

---

### Uppgift 3: Fråga efter namn

**Uppgift:** Skriv ett program som använder `input()` för att fråga kunden vad de heter. Spara svaret i en variabel som heter `namn`. Använd sedan `print()` för att skriva ut ordet "Varsågod", följt av kundens namn, följt av texten "här är din beställning".

**Exempel på körning:**
```text
Vad heter du? Anna
Varsågod Anna här är din beställning
```

**Facit:**
```python
namn = input("Vad heter du? ")
print("Varsågod", namn, "här är din beställning")
```

---

### Uppgift 4: Kaffe eller te?

**Uppgift:** Skriv ett program som ber kunden mata in två saker med `input()`:
1. Vilken varm dryck de vill ha (spara i en variabel).
2. Vilket bakverk de vill ha (spara i en annan variabel).

Använd sedan en **f-sträng** för att skriva ut en mening som inkluderar båda variablerna.

**Exempel på körning:**
```text
Vilken varm dryck vill du ha? Te
Vilket bakverk vill du ha? Chokladboll
Du har beställt Te och en Chokladboll.
```

**Facit:**
```python
dryck = input("Vilken varm dryck vill du ha? ")
bakverk = input("Vilket bakverk vill du ha? ")
print(f"Du har beställt {dryck} och en {bakverk}.")
```

---

### Uppgift 5: Det stora fikasällskapet

**Uppgift:** Skriv ett program som använder tre stycken `input()` för att fråga:
1. Vem som beställer.
2. Hur många vänner de har med sig.
3. Vilken tid de vill boka bord.

Använd sedan tre stycken `print()` med **f-strängar** för att presentera bokningen snyggt, rad för rad.

**Exempel på körning:**
```text
Vem står för bokningen? Karim
Hur många vänner har du med dig? 4
Vilken tid vill ni komma? 15:00
Bokning bekräftad för Karim!
Ni är ett sällskap på 4 vänner.
Bordet är reserverat till kl 15:00.
```

**Facit:**
```python
namn = input("Vem står för bokningen? ")
antal = input("Hur många vänner har du med dig? ")
tid = input("Vilken tid vill ni komma? ")

print(f"Bokning bekräftad för {namn}!")
print(f"Ni är ett sällskap på {antal} vänner.")
print(f"Bordet är reserverat till kl {tid}.")
```
