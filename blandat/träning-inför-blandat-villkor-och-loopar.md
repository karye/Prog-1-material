# Träningsuppgifter inför prov 4: loopar och villkor

Här får du träna på att styra ditt program med hjälp av villkor (`if`, `elif`, `else`) och att upprepa kod med loopar (`for` och `while`). Detta bygger på de kunskaper som finns i din Python-lathund.

### Uppgift 1: ålderskontroll (if och else)

**Uppgift:** Skriv ett program som frågar användaren efter deras ålder. Använd `int()` och `input()`. Om åldern är 18 eller högre, skriv ut "Du är vuxen.". Annars (`else`), skriv ut "Du är minderårig.".

**Exempel på körning 1:**
```text
Ålder: 15
Du är minderårig.
```

**Exempel på körning 2:**
```text
Ålder: 20
Du är vuxen.
```

**Facit:**
```python
alder = int(input("Ålder: "))

if alder >= 18:
    print("Du är vuxen.")
else:
    print("Du är minderårig.")
```

### Uppgift 2: flera val (if, elif och else)

**Uppgift:** Fråga användaren efter en färg. Om färgen är "röd", skriv ut "Du valde röd". Om färgen är "blå", skriv ut "Du valde blå". För alla andra färger, skriv ut "Okänd färg". 

**Exempel på körning:**
```text
Färg: grön
Okänd färg
```

**Facit:**
```python
farg = input("Färg: ")

if farg == "röd":
    print("Du valde röd")
elif farg == "blå":
    print("Du valde blå")
else:
    print("Okänd färg")
```

### Uppgift 3: loopa igenom en lista (for-loop)

**Uppgift:** Skapa en lista med tre frukter: `["äpple", "banan", "kiwi"]`. Använd en `for`-loop för att gå igenom listan och skriva ut en mening för varje frukt.

**Exempel på körning:**
```text
Jag gillar äpple
Jag gillar banan
Jag gillar kiwi
```

**Facit:**
```python
frukter = ["äpple", "banan", "kiwi"]

for frukt in frukter:
    print("Jag gillar", frukt)
```

### Uppgift 4: räkna med range (for-loop)

**Uppgift:** Använd en `for`-loop tillsammans med `range()` för att skriva ut siffrorna 1, 2 och 3 på varsin rad. Skriv ut ordet "Tal" framför siffran.

**Exempel på körning:**
```text
Tal 1
Tal 2
Tal 3
```

**Facit:**
```python
for i in range(1, 4):
    print("Tal", i)
```

### Uppgift 5: lösenord med avbrott (while-loop och break)

**Uppgift:** Skapa en `while True:`-loop (en oändlig loop) som frågar användaren efter ett lösenord. Om användaren skriver in "hemligt", skriv ut "Inloggad!" och använd `break` för att avsluta loopen. Om de skriver fel, låt loopen fråga igen.

**Exempel på körning:**
```text
Lösenord: 1234
Lösenord: qwerty
Lösenord: hemligt
Inloggad!
```

**Facit:**
```python
while True:
    losenord = input("Lösenord: ")
    
    if losenord == "hemligt":
        print("Inloggad!")
        break
```
