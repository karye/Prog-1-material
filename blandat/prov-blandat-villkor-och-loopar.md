# Prov 4: loopar och villkor

Detta prov testar dina kunskaper i att styra programmet med villkor (`if`, `elif`, `else`) samt att upprepa kod med loopar (`for` och `while`).

### Uppgift 1: temperaturkontroll (if och else)

**Uppgift:** Skriv ett program som frågar användaren efter dagens temperatur. Använd `int()` och `input()`. Om temperaturen är mindre än 0, skriv ut "Det är minusgrader!". Annars (`else`), skriv ut "Det är plusgrader!".

**Exempel på körning 1:**
```text
Temperatur: -5
Det är minusgrader!
```

**Exempel på körning 2:**
```text
Temperatur: 12
Det är plusgrader!
```

**Facit:**
```python
temperatur = int(input("Temperatur: "))

if temperatur < 0:
    print("Det är minusgrader!")
else:
    print("Det är plusgrader!")
```

### Uppgift 2: trafikljuset (if, elif och else)

**Uppgift:** Fråga användaren vilken färg trafikljuset visar. Om färgen är "grön", skriv ut "Du kan köra". Om färgen är "röd", skriv ut "Du måste stanna". För alla andra inmatningar, skriv ut "Vänta på din tur". 

**Exempel på körning:**
```text
Färg på trafikljuset: grön
Du kan köra
```

**Facit:**
```python
farg = input("Färg på trafikljuset: ")

if farg == "grön":
    print("Du kan köra")
elif farg == "röd":
    print("Du måste stanna")
else:
    print("Vänta på din tur")
```

### Uppgift 3: loopa igenom en lista (for-loop)

**Uppgift:** Skapa en lista med tre sporter: `["fotboll", "tennis", "simning"]`. Använd en `for`-loop för att gå igenom listan och skriva ut en mening för varje sport.

**Exempel på körning:**
```text
Idag ska jag träna fotboll
Idag ska jag träna tennis
Idag ska jag träna simning
```

**Facit:**
```python
sporter = ["fotboll", "tennis", "simning"]

for sport in sporter:
    print("Idag ska jag träna", sport)
```

### Uppgift 4: räkna med range (for-loop)

**Uppgift:** Använd en `for`-loop tillsammans med `range()` för att skriva ut siffrorna 1, 2 och 3 på varsin rad. Skriv ordet "Klass" framför siffran.

**Exempel på körning:**
```text
Klass 1
Klass 2
Klass 3
```

**Facit:**
```python
for i in range(1, 4):
    print("Klass", i)
```

### Uppgift 5: gissa djuret (while-loop och break)

**Uppgift:** Skapa en `while True:`-loop (en oändlig loop) som frågar användaren "Vilket djur tänker jag på?". Om användaren gissar "hund", skriv ut "Rätt gissat!" och använd `break` för att avsluta loopen. Om de gissar fel, låt loopen fråga igen.

**Exempel på körning:**
```text
Vilket djur tänker jag på? katt
Vilket djur tänker jag på? häst
Vilket djur tänker jag på? hund
Rätt gissat!
```

**Facit:**
```python
while True:
    gissning = input("Vilket djur tänker jag på? ")
    
    if gissning == "hund":
        print("Rätt gissat!")
        break
```
