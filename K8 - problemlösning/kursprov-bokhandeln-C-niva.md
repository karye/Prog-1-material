# Kursprov: Bokhandeln – C-nivå

Kursprov som täcker alla moment från K1–K7. Varje uppgift beskriver **vad programmet ska göra** – du som elev ska själv komma på hur du löser det med kod.

**Tema:** Du bygger ett program för en bokhandel. Kunder kan bläddra bland böcker, söka efter titlar och handla med en budget.

**Bedömning:** 4 uppgifter, totalt 20 poäng. Varje uppgift bygger vidare på den föregående.

---

### Uppgift 1: Bokhyllan (5p)

**Uppgift:** Programmet ska innehålla fyra böcker. För varje bok ska du ha en titel, en författare och ett pris. Organisera informationen i listor – du väljer själv hur (parallella listor eller en lista per bok). När programmet körs ska det skriva ut en rubrik och visa alla boktitlar. Därefter ska programmet fråga kunden vilken bok hen vill veta mer om (ange en siffra 0–3). Beroende på vilken bok kunden väljer ska programmet skriva ut titel, författare och pris. Använd f-strängar.

**Exempel på körning:**
```text
=== BOKHANDELN ===
Böcker: ['Narnia', 'Hobbiten', '1984', 'Circe']
Välj bok (0-3): 1
Titel: Hobbiten | Författare: Tolkien | Pris: 120 kr
```

**Facit:**
```python
titlar = ["Narnia", "Hobbiten", "1984", "Circe"]
forfattare = ["C.S. Lewis", "Tolkien", "George Orwell", "Madeline Miller"]
priser = [99, 120, 89, 140]

print("=== BOKHANDELN ===")
print("Böcker:", titlar)
val = int(input("Välj bok (0-3): "))
print(f"Titel: {titlar[val]} | Författare: {forfattare[val]} | Pris: {priser[val]} kr")
```

---

### Uppgift 2: Bläddra i butiken (5p)

**Uppgift:** Bygg vidare på programmet från uppgift 1. När programmet körs ska det upprepade gånger visa en meny med tre val:

1. Visa info om en bok (samma sökning som i uppgift 1)
2. Visa alla böcker (skriv ut alla titlar med författare, en per rad, med en `for`-loop)
3. Avsluta

Efter varje menyval ska programmet utföra rätt åtgärd och sedan visa menyn igen – utom vid val 3 då programmet ska skriva en avslutningsfras och stanna.

**Exempel på körning:**
```text
=== BOKHANDELN ===

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 2
Narnia av C.S. Lewis
Hobbiten av Tolkien
1984 av George Orwell
Circe av Madeline Miller

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 3
Titel: Circe | Författare: Madeline Miller | Pris: 140 kr

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 3
Tack för besöket!
```

**Facit:**
```python
titlar = ["Narnia", "Hobbiten", "1984", "Circe"]
forfattare = ["C.S. Lewis", "Tolkien", "George Orwell", "Madeline Miller"]
priser = [99, 120, 89, 140]

print("=== BOKHANDELN ===")

while True:
    print()
    print("1. Visa info om en bok")
    print("2. Visa alla böcker")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj bok (0-3): "))
        print(f"Titel: {titlar[index]} | Författare: {forfattare[index]} | Pris: {priser[index]} kr")
    elif val == "2":
        for i in range(4):
            print(f"{titlar[i]} av {forfattare[i]}")
    elif val == "3":
        print("Tack för besöket!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 3: Dagens bokrea (5p)

**Uppgift:** Bygg vidare på programmet från uppgift 2, med två förändringar:

1. **Dagens bokrea.** Varje gång programmet startar ska en slumpmässig bok väljas ut som "dagens bok" (använd `random.randint(0, 3)`). Den boken ska ha reapris – halva priset (avrunda nedåt). Kunden ska inte veta vilken bok som är dagens.

2. **Visningen ändras.** När kunden väljer att visa alla böcker ska priserna synas. Om en bok är dagens bok ska reapriset visas och markeras tydligt. Använd en `for`-loop med `range()`.

3. **Priskollen anpassas.** När kunden kollar info om en bok: om boken är dagens bok ska reapriset visas, annars ordinarie pris.

**Exempel på körning:**
```text
=== BOKHANDELN ===
Dagens bokrea! En bok har halva priset...

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 2
Narnia av C.S. Lewis – 99 kr
Hobbiten av Tolkien – 60 kr (REA!)
1984 av George Orwell – 89 kr
Circe av Madeline Miller – 140 kr

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 1
Titel: Hobbiten | Författare: Tolkien | REA-pris: 60 kr

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 0
Titel: Narnia | Författare: C.S. Lewis | Pris: 99 kr
```

**Facit:**
```python
import random

titlar = ["Narnia", "Hobbiten", "1984", "Circe"]
forfattare = ["C.S. Lewis", "Tolkien", "George Orwell", "Madeline Miller"]
priser = [99, 120, 89, 140]
dagens = random.randint(0, 3)

print("=== BOKHANDELN ===")
print("Dagens bokrea! En bok har halva priset...")

while True:
    print()
    print("1. Visa info om en bok")
    print("2. Visa alla böcker")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Välj bok (0-3): "))
        if index == dagens:
            print(f"Titel: {titlar[index]} | Författare: {forfattare[index]} | REA-pris: {priser[index] // 2} kr")
        else:
            print(f"Titel: {titlar[index]} | Författare: {forfattare[index]} | Pris: {priser[index]} kr")
    elif val == "2":
        for i in range(4):
            if i == dagens:
                print(f"{titlar[i]} av {forfattare[i]} – {priser[i] // 2} kr (REA!)")
            else:
                print(f"{titlar[i]} av {forfattare[i]} – {priser[i]} kr")
    elif val == "3":
        print("Tack för besöket!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 4: Handla och paketera (5p)

**Uppgift:** Bygg vidare på programmet från uppgift 3, med två förändringar:

1. **Budget.** Kunden får en budget. Programmet ska startas genom att ange ett kundnamn och en budget. När kunden väljer en bok (val 1) ska priset dras från budgeten. Dagens bok kostar halva priset, övriga fullt pris. Efter köpet visas kvarvarande budget. Om budgeten inte räcker ska programmet meddela det – men loopen fortsätter. När budgeten når 0 eller lägre ska programmet stanna.

2. **Paketera i en funktion.** Hela programmet ska ligga i en funktion som heter `bokhandel(kund, budget)`. Anropa funktionen med ett valfritt namn och en valfri budget.

**Exempel på körning:**
```text
Välkommen Sanna! Din budget är 200 kr.
Dagens bokrea! En bok har halva priset...

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 2
Titel: 1984 | Författare: George Orwell | Pris: 89 kr
Köpet klart! Kvar av budgeten: 111 kr

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 1
Titel: Hobbiten | Författare: Tolkien | REA-pris: 60 kr
Köpet klart! Kvar av budgeten: 51 kr

1. Visa info om en bok
2. Visa alla böcker
3. Avsluta
Val: 1
Välj bok (0-3): 0
Budgeten räcker inte! Du har bara 51 kr.
```

**Facit:**
```python
def bokhandel(kund, budget):
    import random

    titlar = ["Narnia", "Hobbiten", "1984", "Circe"]
    forfattare = ["C.S. Lewis", "Tolkien", "George Orwell", "Madeline Miller"]
    priser = [99, 120, 89, 140]
    dagens = random.randint(0, 3)

    print(f"Välkommen {kund}! Din budget är {budget} kr.")
    print("Dagens bokrea! En bok har halva priset...")

    while True:
        print()
        print("1. Visa info om en bok")
        print("2. Visa alla böcker")
        print("3. Avsluta")
        val = input("Val: ")
        if val == "1":
            index = int(input("Välj bok (0-3): "))
            if index == dagens:
                kostnad = priser[index] // 2
                rea_text = "REA-"
            else:
                kostnad = priser[index]
                rea_text = ""
            if kostnad > budget:
                print(f"Budgeten räcker inte! Du har bara {budget} kr.")
            else:
                budget = budget - kostnad
                print(f"Titel: {titlar[index]} | Författare: {forfattare[index]} | {rea_text}Pris: {kostnad} kr")
                print(f"Köpet klart! Kvar av budgeten: {budget} kr")
                if budget <= 0:
                    print("Pengarna är slut!")
                    break
        elif val == "2":
            for i in range(4):
                if i == dagens:
                    print(f"{titlar[i]} av {forfattare[i]} – {priser[i] // 2} kr (REA!)")
                else:
                    print(f"{titlar[i]} av {forfattare[i]} – {priser[i]} kr")
        elif val == "3":
            print(f"Tack för besöket, {kund}! Du hade {budget} kr kvar.")
            break
        else:
            print("Ogiltigt val.")

bokhandel("Sanna", 200)
```
