# Träning inför prov 5: listor, loopar och slump

Här får du träna på att kombinera loopar med listor, lägga till nya saker i listor, och låta datorn slumpa fram värden. Allt detta hittar du under rubrikerna "Loopar" och "Listor" i din lathund.

### Uppgift 1: loopa igenom en lista (for-loop)

**Uppgift:** Skapa en lista som heter `matratter` och fyll den med tre favoriter: `"pizza"`, `"tacos"` och `"sushi"`. Använd en `for`-loop för att gå igenom listan och skriva ut varje rätt på en egen rad tillsammans med texten "Jag gillar: ".

**Exempel på körning:**
```text
Jag gillar: pizza
Jag gillar: tacos
Jag gillar: sushi
```

**Facit:**
```python
matratter = ["pizza", "tacos", "sushi"]

for mat in matratter:
    print("Jag gillar:", mat)
```

### Uppgift 2: loopa med siffror (for-loop och range)

**Uppgift:** Du vill skriva ut en nedräkning, eller en sekvens av nummer. Använd en `for`-loop och funktionen `range()` för att skriva ut siffrorna 1 till 5 på varsin rad. Skriv ordet "Nummer" framför varje siffra.

**Exempel på körning:**
```text
Nummer 1
Nummer 2
Nummer 3
Nummer 4
Nummer 5
```

**Facit:**
```python
for i in range(1, 6): # Kom ihåg att den stannar innan sista siffran
    print("Nummer", i)
```

### Uppgift 3: lägg till i lista och räkna (append och len)

**Uppgift:** Skapa en lista med två namn: `["Anna", "Björn"]`.
1. Använd `.append()` för att lägga till `"Cissi"` i listan.
2. Skriv ut ett meddelande med hjälp av `len()` som berättar exakt hur många personer som finns på listan totalt.

**Exempel på körning:**
```text
Det finns nu 3 personer på listan.
```

**Facit:**
```python
namnlista = ["Anna", "Björn"]
namnlista.append("Cissi")

antal = len(namnlista)
print(f"Det finns nu {antal} personer på listan.")
```

### Uppgift 4: slumpa från en lista (random)

**Uppgift:** Börja med att skriva `import random` högst upp. Skapa sedan en lista med tre priser: `["en cykel", "1000 kr", "en biobiljett"]`. Låt datorn slumpa fram vilket pris användaren vinner med hjälp av `random.choice()` och spara det i en variabel. Skriv ut resultatet.

**Exempel på körning (resultatet kan variera):**
```text
Grattis! Du vann: en biobiljett
```

**Facit:**
```python
import random

priser = ["en cykel", "1000 kr", "en biobiljett"]
vinst = random.choice(priser)

print(f"Grattis! Du vann: {vinst}")
```

### Uppgift 5: samla inköp tills du är klar (while, append och break)

**Uppgift:** Skapa en helt tom lista som heter `inkopslista = []`.
Skapa en oändlig loop (`while True:`) där användaren får frågan "Vad vill du köpa? ".
* Om användaren skriver "klar", ska loopen avslutas direkt med `break`.
* Om användaren skriver något annat, ska det läggas till i listan `inkopslista` med `.append()`.
När loopen är avslutad ska programmet skriva ut hela listan.

**Exempel på körning:**
```text
Vad vill du köpa? mjölk
Vad vill du köpa? bröd
Vad vill du köpa? klar
Din inköpslista: ['mjölk', 'bröd']
```

**Facit:**
```python
inkopslista = []

while True:
    vara = input("Vad vill du köpa? ")
    
    if vara == "klar":
        break
    else:
        inkopslista.append(vara)

print("Din inköpslista:", inkopslista)
```
