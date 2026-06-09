# Kursprov: Rymdstationen – A-nivå

Kursprov som täcker alla moment från K1–K7. Du får en övergripande problembeskrivning – **hur** du löser det med kod är upp till dig. Du designar datastrukturer, menyer och logik själv.

**Tema:** Du bygger en simulator för en rymdstation. Stationen har en besättning, resurser och kan skickas på uppdrag.

**Bedömning:** 3 uppgifter, totalt 20 poäng. Varje uppgift bygger vidare på den föregående.

---

### Uppgift 1: Besättning och resurser (7p)

**Uppgift:** Programmet ska hantera rymdstationens besättning och resurser. Du bestämmer själv hur informationen organiseras i listor.

Besättningen ska bestå av **minst fyra personer**. För varje person ska du ha namn, roll (t.ex. kapten, ingenjör, läkare, pilot) och en färdighetspoäng (1–10). Du bestämmer själv namnen och poängen.

Resurserna ska bestå av **minst tre resurstyper** (t.ex. syre, bränsle, mat). Varje resurs har ett namn och en mängd (ett tal). Du bestämmer själv resurserna och startmängderna.

När programmet körs ska det skriva ut en rubrik och sedan presentera både besättning och resurser på ett överskådligt sätt. Använd f-strängar och snygg formatering. Du bestämmer själv layout.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== RYMDSTATIONEN ODYSSÉE ===
--- Besättning ---
Kapten: Sara (färdighet: 9)
Ingenjör: Marcus (färdighet: 7)
Läkare: Lena (färdighet: 6)
Pilot: Ahmed (färdighet: 8)

--- Resurser ---
Syre: 500 enheter
Bränsle: 800 liter
Mat: 300 portioner
```

**Facit:**
```python
namn = ["Sara", "Marcus", "Lena", "Ahmed"]
roller = ["Kapten", "Ingenjör", "Läkare", "Pilot"]
fardighet = [9, 7, 6, 8]

resurser = ["Syre", "Bränsle", "Mat"]
mangder = [500, 800, 300]
enheter = ["enheter", "liter", "portioner"]

print("=== RYMDSTATIONEN ODYSSÉE ===")
print("--- Besättning ---")
for i in range(4):
    print(f"{roller[i]}: {namn[i]} (färdighet: {fardighet[i]})")

print()
print("--- Resurser ---")
for i in range(3):
    print(f"{resurser[i]}: {mangder[i]} {enheter[i]}")
```

---

### Uppgift 7: Uppdragskontroll (7p)

**Uppgift:** Bygg vidare på programmet från uppgift 1. Nu ska rymdstationen bli interaktiv. Programmet ska ha en `while`-loop med en meny där användaren kan:

1. **Inspektera besättningsmedlem** – användaren anger ett index för att se detaljer om en person.
2. **Skicka på uppdrag** – användaren väljer en besättningsmedlem (index). Programmet ska slumpa fram om uppdraget lyckas eller misslyckas (använd `random.randint`). Chansen att lyckas ska bero på personens färdighetspoäng: om färdigheten är 8–10 är chansen hög (t.ex. 80 %), om 5–7 är chansen medel (t.ex. 50 %), annars låg (t.ex. 30 %). Skriv ut resultatet.
3. **Visa status** – visa besättning och resurser (samma som i uppgift 1).
4. **Avsluta** – avsluta programmet.

Du bestämmer själv exakta procentsatser, texter och layout. Använd f-strängar.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== RYMDSTATIONEN ODYSSÉE ===
--- Besättning ---
Kapten: Sara (färdighet: 9)
...

1. Inspektera besättning
2. Skicka på uppdrag
3. Visa status
4. Avsluta
Val: 2
Välj besättningsmedlem (0-3): 0
Sara (Kapten) skickas på uppdrag...
Uppdraget lyckades! Sara är tillbaka oskadd.

1. Inspektera besättning
...
Val: 1
Välj besättningsmedlem (0-3): 3
Pilot: Ahmed | Färdighet: 8

1. Inspektera besättning
...
Val: 4
Rymdstationen går i viloläge...
```

**Facit:**
```python
import random

namn = ["Sara", "Marcus", "Lena", "Ahmed"]
roller = ["Kapten", "Ingenjör", "Läkare", "Pilot"]
fardighet = [9, 7, 6, 8]

resurser = ["Syre", "Bränsle", "Mat"]
mangder = [500, 800, 300]
enheter = ["enheter", "liter", "portioner"]

print("=== RYMDSTATIONEN ODYSSÉE ===")
print("--- Besättning ---")
for i in range(4):
    print(f"{roller[i]}: {namn[i]} (färdighet: {fardighet[i]})")
print()
print("--- Resurser ---")
for i in range(3):
    print(f"{resurser[i]}: {mangder[i]} {enheter[i]}")

while True:
    print()
    print("1. Inspektera besättning")
    print("2. Skicka på uppdrag")
    print("3. Visa status")
    print("4. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj besättningsmedlem (0-3): "))
        print(f"{roller[index]}: {namn[index]} | Färdighet: {fardighet[index]}")
    elif val == "2":
        index = int(input("Välj besättningsmedlem (0-3): "))
        print(f"{namn[index]} ({roller[index]}) skickas på uppdrag...")
        if fardighet[index] >= 8:
            chans = 80
        elif fardighet[index] >= 5:
            chans = 50
        else:
            chans = 30
        slag = random.randint(1, 100)
        if slag <= chans:
            print(f"Uppdraget lyckades! {namn[index]} är tillbaka oskadd.")
        else:
            print(f"Uppdraget misslyckades... {namn[index]} behöver vila.")
    elif val == "3":
        print("--- Besättning ---")
        for i in range(4):
            print(f"{roller[i]}: {namn[i]} (färdighet: {fardighet[i]})")
        print()
        print("--- Resurser ---")
        for i in range(3):
            print(f"{resurser[i]}: {mangder[i]} {enheter[i]}")
    elif val == "4":
        print("Rymdstationen går i viloläge...")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 3: Överlevnadssimulering (6p)

**Uppgift:** Bygg vidare på programmet från uppgift 2 med två förändringar:

1. **Resursförbrukning.** Varje gång ett uppdrag genomförs (val 2) ska resurser förbrukas oavsett om uppdraget lyckas eller inte. Du bestämmer själv hur mycket av varje resurs som går åt (t.ex. 50 syre, 100 bränsle, 30 mat per uppdrag). Uppdatera resursmängderna och skriv ut vad som förbrukades. Om uppdraget misslyckas förbrukas dubbelt så mycket.

2. **Game over.** Om någon resurs når 0 eller lägre ska programmet meddela att stationen inte kan fortsätta och stanna.

3. **Paketera i en funktion.** Hela programmet ska paketeras i en funktion som heter `rymdstation(stationsnamn)`. Funktionen tar emot stationens namn som argument. Anropa funktionen med ett valfritt namn.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== RYMDSTATIONEN ODYSSÉE ===
...

1. Inspektera besättning
2. Skicka på uppdrag
3. Visa status
4. Avsluta
Val: 2
Välj besättningsmedlem (0-3): 1
Marcus (Ingenjör) skickas på uppdrag...
Uppdraget lyckades! Marcus är tillbaka oskadd.
Resurser förbrukade: Syre -50, Bränsle -100, Mat -30

1. Inspektera besättning
...
Val: 3
--- Resurser ---
Syre: 450 enheter
Bränsle: 700 liter
Mat: 270 portioner
```

**Facit:**
```python
def rymdstation(stationsnamn):
    import random

    namn = ["Sara", "Marcus", "Lena", "Ahmed"]
    roller = ["Kapten", "Ingenjör", "Läkare", "Pilot"]
    fardighet = [9, 7, 6, 8]

    resurser = ["Syre", "Bränsle", "Mat"]
    mangder = [500, 800, 300]
    enheter = ["enheter", "liter", "portioner"]
    forbrukning = [50, 100, 30]

    print(f"=== RYMDSTATIONEN {stationsnamn.upper()} ===")
    print("--- Besättning ---")
    for i in range(4):
        print(f"{roller[i]}: {namn[i]} (färdighet: {fardighet[i]})")
    print()
    print("--- Resurser ---")
    for i in range(3):
        print(f"{resurser[i]}: {mangder[i]} {enheter[i]}")

    while True:
        # Kontrollera resurser
        game_over = False
        for i in range(3):
            if mangder[i] <= 0:
                game_over = True
        if game_over:
            print("Resurserna är slut! Rymdstationen kan inte fortsätta.")
            break

        print()
        print("1. Inspektera besättning")
        print("2. Skicka på uppdrag")
        print("3. Visa status")
        print("4. Avsluta")
        val = input("Val: ")
        if val == "1":
            index = int(input("Välj besättningsmedlem (0-3): "))
            print(f"{roller[index]}: {namn[index]} | Färdighet: {fardighet[index]}")
        elif val == "2":
            index = int(input("Välj besättningsmedlem (0-3): "))
            print(f"{namn[index]} ({roller[index]}) skickas på uppdrag...")
            if fardighet[index] >= 8:
                chans = 80
            elif fardighet[index] >= 5:
                chans = 50
            else:
                chans = 30
            slag = random.randint(1, 100)
            if slag <= chans:
                print(f"Uppdraget lyckades! {namn[index]} är tillbaka oskadd.")
                faktor = 1
            else:
                print(f"Uppdraget misslyckades... {namn[index]} behöver vila.")
                faktor = 2
            for i in range(3):
                mangder[i] = mangder[i] - forbrukning[i] * faktor
            print(f"Resurser förbrukade: {resurser[0]} -{forbrukning[0] * faktor}, {resurser[1]} -{forbrukning[1] * faktor}, {resurser[2]} -{forbrukning[2] * faktor}")
        elif val == "3":
            print("--- Besättning ---")
            for i in range(4):
                print(f"{roller[i]}: {namn[i]} (färdighet: {fardighet[i]})")
            print()
            print("--- Resurser ---")
            for i in range(3):
                print(f"{resurser[i]}: {mangder[i]} {enheter[i]}")
        elif val == "4":
            print("Rymdstationen går i viloläge...")
            break
        else:
            print("Ogiltigt val.")

rymdstation("Odyssée")
```
