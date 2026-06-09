# Prov 3e: While-loopar – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med `while`-loopar. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Simuleringar och verktyg.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt loop-logik och genomtänkt struktur.

---

### Uppgift 1: Enkätverktyget (10p)

**Uppgift:** Bygg ett program som samlar in svar i en enkät. Programmet ska fungera så här:

* Programmet startar med att be användaren skriva en **enkätfråga** (en enda fråga, valfri text).
* Därefter går programmet in i en `while`-loop där användaren kan mata in svar på frågan – ett svar per varv.
* Loopen avslutas när användaren skriver `"klar"`.
* Efter att loopen avslutats ska programmet skriva ut en **sammanställning**: frågan, hur många svar som samlades in, och alla svar listade med numrering.
* Använd f-strängar för utskrifterna.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Skriv din enkätfråga: Vilken är din favoritfärg?
Svar (skriv "klar" för att avsluta): Blå
Svar (skriv "klar" för att avsluta): Grön
Svar (skriv "klar" för att avsluta): Röd
Svar (skriv "klar" för att avsluta): klar
=== ENKÄTRESULTAT ===
Fråga: Vilken är din favoritfärg?
Antal svar: 3
Svar 1: Blå
Svar 2: Grön
Svar 3: Röd
```

**Facit:**
```python
fraga = input("Skriv din enkätfråga: ")
svar_lista = ""

while True:
    svar = input('Svar (skriv "klar" för att avsluta): ')
    if svar == "klar":
        break
    if svar_lista == "":
        svar_lista = svar
    else:
        svar_lista = svar_lista + "|" + svar

print("=== ENKÄTRESULTAT ===")
print(f"Fråga: {fraga}")

svar_array = svar_lista.split("|") if svar_lista != "" else []
antal = len(svar_array)
print(f"Antal svar: {antal}")
for i in range(antal):
    print(f"Svar {i + 1}: {svar_array[i]}")
```

---

### Uppgift 2: Hissimulatorn (10p)

**Uppgift:** Bygg ett program som simulerar en hiss i ett hus med 10 våningar (0–9). Programmet ska fungera så här:

* Hissen börjar på våning 0.
* Programmet visar en meny i en `while`-loop med följande val:
  - `1`: Åk till en våning – användaren anger vilken våning (0–9). Hissen "åker" dit (skriv ut den nya våningen).
  - `2`: Visa nuvarande våning.
  - `3`: Avsluta hissen.
* Om användaren försöker åka till en våning utanför 0–9 ska programmet skriva ett felmeddelande – men loopen ska fortsätta.
* Om användaren väljer att åka till den våning hissen redan står på ska programmet påpeka det.
* Använd f-strängar och snygg formatering. Du bestämmer själv exakta texter och layout.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== HISSEN ===
Våning: 0

1. Åk till våning
2. Visa våning
3. Avsluta
Val: 1
Vilken våning? 5
Hissen åker... Våning 5!

1. Åk till våning
2. Visa våning
3. Avsluta
Val: 1
Vilken våning? 11
Fel: Våning 11 finns inte (0–9).

1. Åk till våning
2. Visa våning
3. Avsluta
Val: 2
Du är på våning 5.

1. Åk till våning
2. Visa våning
3. Avsluta
Val: 3
Hissen stängs av. Hejdå!
```

**Facit:**
```python
vaning = 0
print("=== HISSEN ===")

while True:
    print(f"Våning: {vaning}")
    print()
    print("1. Åk till våning")
    print("2. Visa våning")
    print("3. Avsluta")
    val = input("Val: ")

    if val == "1":
        mal = int(input("Vilken våning? "))
        if mal < 0 or mal > 9:
            print(f"Fel: Våning {mal} finns inte (0–9).")
        elif mal == vaning:
            print(f"Du är redan på våning {vaning}.")
        else:
            vaning = mal
            print(f"Hissen åker... Våning {vaning}!")
    elif val == "2":
        print(f"Du är på våning {vaning}.")
    elif val == "3":
        print("Hissen stängs av. Hejdå!")
        break
    else:
        print("Ogiltigt val – försök igen.")
```
