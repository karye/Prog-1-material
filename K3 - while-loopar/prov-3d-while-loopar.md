# Prov 3d: While-loopar – C-nivå

Detta prov testar din förmåga att självständigt använda `while`-loopar i kombination med `input()`, `if` och `break`. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Interaktiva program.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Gissa talet (7p)

**Uppgift:** Programmet ska slumpa fram ett hemligt tal mellan 1 och 20. Spelaren ska sedan gissa talet i en `while`-loop. Efter varje gissning ska programmet ge en ledtråd: `"För högt!"` eller `"För lågt!"`. När spelaren gissar rätt ska programmet skriva ut en gratulationsfras och hur många gissningar som behövdes – sedan avslutas loopen.

* Använd `import random` och `random.randint(1, 20)` för att slumpa talet.
* Räkna antalet gissningar i en variabel som ökar med 1 för varje varv.
* Använd f-strängar för utskrifterna.

**Exempel på körning:**
```text
Jag tänker på ett tal mellan 1 och 20...
Gissa: 10
För lågt!
Gissa: 15
För högt!
Gissa: 12
Grattis! Du gissade rätt på 3 försök.
```

**Facit:**
```python
import random

hemligt = random.randint(1, 20)
forsok = 0

print("Jag tänker på ett tal mellan 1 och 20...")
while True:
    gissning = int(input("Gissa: "))
    forsok = forsok + 1
    if gissning == hemligt:
        print(f"Grattis! Du gissade rätt på {forsok} försök.")
        break
    elif gissning < hemligt:
        print("För lågt!")
    else:
        print("För högt!")
```

---

### Uppgift 2: Poängräknare (7p)

**Uppgift:** Programmet ska låta användaren mata in poäng om och om igen i en `while`-loop. Programmet ska hålla reda på:

* **Totalpoängen** (summan av alla inmatade poäng).
* **Antal omgångar** (hur många gånger användaren matat in poäng).

Loopen ska avslutas när användaren skriver `-1`. Då ska programmet skriva ut totalpoäng, antal omgångar och medelpoäng per omgång (totalpoäng delat med antal omgångar) – formaterat med f-strängar. Inga decimaler krävs.

**Exempel på körning:**
```text
Ange poäng (-1 för att avsluta): 5
Ange poäng (-1 för att avsluta): 8
Ange poäng (-1 för att avsluta): 3
Ange poäng (-1 för att avsluta): -1
Totalpoäng: 16
Omgångar: 3
Medelpoäng: 5
```

**Facit:**
```python
total = 0
omgangar = 0

while True:
    poang = int(input("Ange poäng (-1 för att avsluta): "))
    if poang == -1:
        break
    total = total + poang
    omgangar = omgangar + 1

print(f"Totalpoäng: {total}")
print(f"Omgångar: {omgangar}")
if omgangar > 0:
    print(f"Medelpoäng: {total // omgangar}")
```

---

### Uppgift 3: Lösenordsporten (6p)

**Uppgift:** Programmet ska be användaren om ett lösenord i en `while`-loop. Användaren har maximalt **tre försök**. Det korrekta lösenordet är `"python"`.

* Om användaren skriver rätt lösenord: skriv `"Åtkomst beviljad!"` och avsluta loopen.
* Om användaren skriver fel: dra av ett försök och skriv hur många försök som är kvar.
* Om försöken tar slut: skriv `"Åtkomst nekad – för många felaktiga försök."` och avsluta loopen.
* Använd f-strängar för utskrifterna.

**Exempel på körning:**
```text
Lösenord: hej
Fel lösenord. Försök kvar: 2
Lösenord: kod
Fel lösenord. Försök kvar: 1
Lösenord: python
Åtkomst beviljad!
```

```text
Lösenord: abc
Fel lösenord. Försök kvar: 2
Lösenord: 123
Fel lösenord. Försök kvar: 1
Lösenord: test
Åtkomst nekad – för många felaktiga försök.
```

**Facit:**
```python
forsok = 3

while True:
    losen = input("Lösenord: ")
    if losen == "python":
        print("Åtkomst beviljad!")
        break
    else:
        forsok = forsok - 1
        if forsok == 0:
            print("Åtkomst nekad – för många felaktiga försök.")
            break
        print(f"Fel lösenord. Försök kvar: {forsok}")
```
