# Kursprov: Skattjakten

Kursprov som täcker alla moment från K1–K7. Varje uppgift beskriver **vad programmet ska göra** — du som elev ska själv komma på hur du löser det med kod.

**Tema:** Du bygger ett skattjaktsprogram. En skatt är gömd på en av fyra platser — spelaren har ett begränsat antal försök att hitta den.

**Bedömning:** 5 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Skattkammaren (4p)

**Uppgift:** Programmet ska innehålla fyra platser: Pyramiden, Vulkanen, Djungeln och Grottan. När programmet körs ska det skriva ut en rubrik och visa alla platser. Därefter ska programmet fråga spelaren vilken plats hen vill undersöka (ange en siffra 0–3). Beroende på vilken plats spelaren väljer ska programmet ge ett unikt svar. Skatten finns på den sista platsen (index 3) — bara där meddelas att skatten är hittad.

**Exempel på körning:**
```text
=== SKATTJAKTEN ===
Platser: ['Pyramiden', 'Vulkanen', 'Djungeln', 'Grottan']
Välj plats (0-3): 1
Du söker i Vulkanen... bara lava här.
```

**Exempel på körning (skatt):**
```text
=== SKATTJAKTEN ===
Platser: ['Pyramiden', 'Vulkanen', 'Djungeln', 'Grottan']
Välj plats (0-3): 3
Du söker i Grottan... SKATTEN! Grattis!
```

**Facit:**
```python
platser = ["Pyramiden", "Vulkanen", "Djungeln", "Grottan"]
print("=== SKATTJAKTEN ===")
print("Platser:", platser)

val = int(input("Välj plats (0-3): "))
if val == 0:
    print("Du söker i Pyramiden... bara sand här.")
elif val == 1:
    print("Du söker i Vulkanen... bara lava här.")
elif val == 2:
    print("Du söker i Djungeln... bara träd här.")
elif val == 3:
    print("Du söker i Grottan... SKATTEN! Grattis!")
else:
    print("Ogiltigt index!")
```

---

### Uppgift 2: Meny för upptäcktsresande (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 1. När programmet körs ska det upprepade gånger visa en meny med tre val:

1. Söka på en plats (samma sökning som i uppgift 1)
2. Visa alla platser
3. Avsluta programmet

Efter varje menyval ska programmet utföra rätt åtgärd och sedan visa menyn igen — utom vid val 3 då programmet ska skriva en avslutningsfras och stanna.

**Exempel på körning:**
```text
=== SKATTJAKTEN ===
Platser: ['Pyramiden', 'Vulkanen', 'Djungeln', 'Grottan']

1. Sök plats
2. Visa alla platser
3. Avsluta
Val: 2
['Pyramiden', 'Vulkanen', 'Djungeln', 'Grottan']

1. Sök plats
2. Visa alla platser
3. Avsluta
Val: 1
Välj plats (0-3): 3
Du söker i Grottan... SKATTEN! Grattis!

1. Sök plats
2. Visa alla platser
3. Avsluta
Val: 3
Jakten avslutad!
```

**Facit:**
```python
platser = ["Pyramiden", "Vulkanen", "Djungeln", "Grottan"]
print("=== SKATTJAKTEN ===")
print("Platser:", platser)

while True:
    print()
    print("1. Sök plats")
    print("2. Visa alla platser")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj plats (0-3): "))
        if index == 0:
            print("Du söker i Pyramiden... bara sand här.")
        elif index == 1:
            print("Du söker i Vulkanen... bara lava här.")
        elif index == 2:
            print("Du söker i Djungeln... bara träd här.")
        elif index == 3:
            print("Du söker i Grottan... SKATTEN! Grattis!")
        else:
            print("Ogiltigt index!")
    elif val == "2":
        print(platser)
    elif val == "3":
        print("Jakten avslutad!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 3: Slumpa skatten (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 2, men med två förändringar:

1. **Skatten ska slumpas.** Varje gång programmet startar ska skatten finnas på en slumpmässig plats (0–3), inte alltid på samma ställe. Spelaren ska inte veta vilken plats som har skatten — programmet ska bara skriva att skatten är gömd.

2. **Skattkarta.** När spelaren väljer att visa platserna ska det inte längre se ut som en vanlig lista. Istället ska varje plats skrivas ut på en egen rad med sitt nummer framför, så här: `Plats 0: Pyramiden`.

3. **Sökningen förenklas.** Programmet ska inte längre skriva ett unikt meddelande för varje plats. Istället: om spelarens val matchar den slumpade platsen skrivs en vinstfras, annars meddelas att det inte fanns någon skatt och vilken plats som söktes.

**Exempel på körning:**
```text
=== SKATTJAKTEN ===
Skatten är gömd... lycka till!

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 2
Plats 0: Pyramiden
Plats 1: Vulkanen
Plats 2: Djungeln
Plats 3: Grottan

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 1
Ingen skatt på Vulkanen

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 0
SKATTEN! Grattis!
```

**Facit:**
```python
import random

platser = ["Pyramiden", "Vulkanen", "Djungeln", "Grottan"]
skatt_plats = random.randint(0, 3)

print("=== SKATTJAKTEN ===")
print("Skatten är gömd... lycka till!")

while True:
    print()
    print("1. Sök plats")
    print("2. Visa skattkarta")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj plats (0-3): "))
        if index == skatt_plats:
            print("SKATTEN! Grattis!")
        else:
            print("Ingen skatt på", platser[index])
    elif val == "2":
        for i in range(4):
            print("Plats", i, ":", platser[i])
    elif val == "3":
        print("Jakten avslutad!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 4: Begränsade försök (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 3. Nu ska spelaren bara få **tre försök** att hitta skatten.

- Efter varje felaktig gissning ska programmet visa hur många försök som är kvar.
- När försöken tar slut ska programmet meddela att spelet är över och stanna.
- Om spelaren hittar skatten ska programmet meddela detta och stanna direkt — inga fler menyval ska visas.

Allt annat i programmet ska fungera som i uppgift 3 (meny, skattkarta, avsluta).

**Exempel på körning:**
```text
=== SKATTJAKTEN ===
Skatten är gömd... lycka till!

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 0
Ingen skatt på Pyramiden
Försök kvar: 2

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 1
Ingen skatt på Vulkanen
Försök kvar: 1

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 2
Ingen skatt på Djungeln
Försök kvar: 0
Slut på försök! Spelet över.
```

**Facit:**
```python
import random

platser = ["Pyramiden", "Vulkanen", "Djungeln", "Grottan"]
skatt_plats = random.randint(0, 3)
forsok_kvar = 3

print("=== SKATTJAKTEN ===")
print("Skatten är gömd... lycka till!")

while True:
    print()
    print("1. Sök plats")
    print("2. Visa skattkarta")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj plats (0-3): "))
        if index == skatt_plats:
            print("SKATTEN! Grattis!")
            break
        else:
            print("Ingen skatt på", platser[index])
            forsok_kvar = forsok_kvar - 1
            print("Försök kvar:", forsok_kvar)
            if forsok_kvar == 0:
                print("Slut på försök! Spelet över.")
                break
    elif val == "2":
        for i in range(4):
            print("Plats", i, ":", platser[i])
    elif val == "3":
        print("Jakten avslutad!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 5: Paketera spelet (4p)

**Uppgift:** Nu ska hela spelet paketeras så att det enkelt kan startas med olika spelare och olika antal försök.

- Spelet ska kunna startas genom att ange ett spelarnamn och ett valfritt antal försök.
- När spelet startar ska det hälsa spelaren välkommen och skriva ut hur många försök hen har.
- Därefter ska spelet fungera precis som i uppgift 4, fast med det antal försök som angavs vid start istället för alltid 3.

Utanför spelet ska du starta det med ett valfritt namn och valfritt antal försök.

**Exempel på körning:**
```text
Välkommen Äventyraren! Du har 2 försök.
Skatten är gömd... lycka till!

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 3
Ingen skatt på Grottan
Försök kvar: 1

1. Sök plats
2. Visa skattkarta
3. Avsluta
Val: 1
Välj plats (0-3): 0
SKATTEN! Grattis!
```

**Facit:**
```python
def skattjakt(spelare, max_forsok):
    import random

    platser = ["Pyramiden", "Vulkanen", "Djungeln", "Grottan"]
    skatt_plats = random.randint(0, 3)
    forsok_kvar = max_forsok

    print(f"Välkommen {spelare}! Du har {max_forsok} försök.")
    print("Skatten är gömd... lycka till!")

    while True:
        print()
        print("1. Sök plats")
        print("2. Visa skattkarta")
        print("3. Avsluta")
        val = input("Val: ")
        if val == "1":
            index = int(input("Välj plats (0-3): "))
            if index == skatt_plats:
                print("SKATTEN! Grattis!")
                break
            else:
                print("Ingen skatt på", platser[index])
                forsok_kvar = forsok_kvar - 1
                print("Försök kvar:", forsok_kvar)
                if forsok_kvar == 0:
                    print("Slut på försök! Spelet över.")
                    break
        elif val == "2":
            for i in range(4):
                print("Plats", i, ":", platser[i])
        elif val == "3":
            print("Jakten avslutad!")
            break
        else:
            print("Ogiltigt val.")

skattjakt("Äventyraren", 2)
```
