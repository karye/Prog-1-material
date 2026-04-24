# Träning inför prov 5b: listor, loopar och slump

Här får du träna på att kombinera loopar med listor, lägga till nya saker i listor, och låta datorn slumpa fram värden. Allt detta hittar du under rubrikerna "Loopar" och "Listor" i din lathund.

### Uppgift 1: loopa igenom en lista (for-loop)

**Uppgift:** Skapa en lista som heter `ryggsack` och fyll den med tre föremål: `"karta"`, `"kompass"` och `"ficklampa"`. Använd en `for`-loop för att gå igenom listan och skriva ut varje sak på en egen rad tillsammans med texten "Du har en: ".

**Exempel på körning:**
```text
Du har en: karta
Du har en: kompass
Du har en: ficklampa
```

**Facit:**
```python
ryggsack = ["karta", "kompass", "ficklampa"]

for sak in ryggsack:
    print("Du har en:", sak)
```

### Uppgift 2: loopa med siffror (for-loop och range)

**Uppgift:** Din karaktär går upp i level. Använd en `for`-loop och funktionen `range()` för att skriva ut nivåerna 1 till 5 på varsin rad. Skriv ordet "Level" framför varje siffra.

**Exempel på körning:**
```text
Level 1
Level 2
Level 3
Level 4
Level 5
```

**Facit:**
```python
for i in range(1, 6): # Kom ihåg att den stannar innan sista siffran
    print("Level", i)
```

### Uppgift 3: lägg till i lista och räkna (append och len)

**Uppgift:** Skapa en lista med två skatter: `["guldmynt", "diamant"]`. 
1. Använd `.append()` för att lägga till `"trollstav"` i listan.
2. Skriv ut ett meddelande med hjälp av `len()` som berättar exakt hur många skatter du har hittat totalt.

**Exempel på körning:**
```text
Grattis, du har nu hittat 3 skatter!
```

**Facit:**
```python
skatter = ["guldmynt", "diamant"]
skatter.append("trollstav")

antal = len(skatter)
print(f"Grattis, du har nu hittat {antal} skatter!")
```

### Uppgift 4: slumpa från en lista (random)

**Uppgift:** Börja med att skriva `import random` högst upp. Skapa sedan en lista med tre olika fiender: `["troll", "drake", "spöke"]`. Låt datorn slumpa fram vilken fiende som dyker upp med hjälp av `random.choice()` och spara den i en variabel. Skriv ut resultatet.

**Exempel på körning (resultatet kan variera):**
```text
Se upp! Ett vilt troll dyker plötsligt upp!
```

**Facit:**
```python
import random

fiender = ["troll", "drake", "spöke"]
monster = random.choice(fiender)

print(f"Se upp! Ett vilt {monster} dyker plötsligt upp!")
```

### Uppgift 5: samla föremål tills du är klar (while, append och break)

**Uppgift:** Skapa en helt tom lista som heter `ficka = []`. 
Skapa en oändlig loop (`while True:`) där användaren får frågan "Vad vill du plocka upp? ". 
* Om användaren skriver "inget", ska loopen avslutas direkt med `break`. 
* Om användaren skriver något annat, ska det läggas till i listan `ficka` med `.append()`.
När loopen är avslutad ska programmet skriva ut hela listan.

**Exempel på körning:**
```text
Vad vill du plocka upp? en sten
Vad vill du plocka upp? ett äpple
Vad vill du plocka upp? inget
I din ficka finns nu: ['en sten', 'ett äpple']
```

**Facit:**
```python
ficka = []

while True:
    sak = input("Vad vill du plocka upp? ")
    
    if sak == "inget":
        break
    else:
        ficka.append(sak)

print("I din ficka finns nu:", ficka)
```
