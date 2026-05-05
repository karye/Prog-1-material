# Kursprov: Pizzabeställningen

Kursprov som täcker alla moment från K1–K7. Varje uppgift beskriver **vad programmet ska göra** — du som elev ska själv komma på hur du löser det med kod.

**Tema:** Du bygger ett program för en pizzeria. Kunderna kan bläddra i menyn, beställa pizzor och hålla koll på sin budget.

**Bedömning:** 5 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Pizzamenyn (4p)

**Uppgift:** Programmet ska innehålla fyra pizzor: Margherita, Hawaii, Kebab och Vesuvio. När programmet körs ska det skriva ut en rubrik och visa menyn. Därefter ska programmet fråga kunden vilken pizza hen vill veta priset på (ange en siffra 0–3). Beroende på vilken pizza kunden väljer ska programmet skriva ut pizzans namn och vad den kostar. Varje pizza ska ha ett eget pris och ett eget svar.

**Exempel på körning:**
```text
=== PIZZERIA KODEN ===
Meny: ['Margherita', 'Hawaii', 'Kebab', 'Vesuvio']
Vilken pizza (0-3)? 2
Kebab kostar 105 kr.
```

**Facit:**
```python
pizzor = ["Margherita", "Hawaii", "Kebab", "Vesuvio"]
print("=== PIZZERIA KODEN ===")
print("Meny:", pizzor)

val = int(input("Vilken pizza (0-3)? "))
if val == 0:
    print("Margherita kostar 85 kr.")
elif val == 1:
    print("Hawaii kostar 95 kr.")
elif val == 2:
    print("Kebab kostar 105 kr.")
elif val == 3:
    print("Vesuvio kostar 110 kr.")
else:
    print("Ogiltigt val!")
```

---

### Uppgift 2: Beställningsdisk (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 1. När programmet körs ska det upprepade gånger visa en meny med fyra val:

1. Se pris på en pizza (samma sökning som i uppgift 1)
2. Visa hela menyn
3. Avsluta och betala

Efter varje menyval ska programmet utföra rätt åtgärd och sedan visa menyn igen — utom vid val 3 då programmet ska skriva en avslutningsfras och stanna.

**Exempel på körning:**
```text
=== PIZZERIA KODEN ===
Meny: ['Margherita', 'Hawaii', 'Kebab', 'Vesuvio']

1. Se pris
2. Visa menyn
3. Avsluta
Val: 2
['Margherita', 'Hawaii', 'Kebab', 'Vesuvio']

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 0
Margherita kostar 85 kr.

1. Se pris
2. Visa menyn
3. Avsluta
Val: 3
Tack för ditt besök!
```

**Facit:**
```python
pizzor = ["Margherita", "Hawaii", "Kebab", "Vesuvio"]
print("=== PIZZERIA KODEN ===")
print("Meny:", pizzor)

while True:
    print()
    print("1. Se pris")
    print("2. Visa menyn")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Vilken pizza (0-3)? "))
        if index == 0:
            print("Margherita kostar 85 kr.")
        elif index == 1:
            print("Hawaii kostar 95 kr.")
        elif index == 2:
            print("Kebab kostar 105 kr.")
        elif index == 3:
            print("Vesuvio kostar 110 kr.")
        else:
            print("Ogiltigt val!")
    elif val == "2":
        print(pizzor)
    elif val == "3":
        print("Tack för ditt besök!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 3: Dagens pizza (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 2, men med två förändringar:

1. **Dagens pizza.** Varje gång programmet startar ska en av de fyra pizzorna slumpas fram som "dagens pizza". Den pizzan ska ha ett extrapris på 69 kr istället för sitt ordinarie pris. Spelaren ska inte veta vilken pizza som är dagens.

2. **Menyn visas snyggare.** När kunden väljer att visa menyn ska den inte längre se ut som en lista. Istället ska varje pizza skrivas ut på en egen rad med sitt nummer framför.

3. **Priskollen förenklas.** Programmet ska inte längre skriva ut ett unikt svar för varje pizza. Istället: om kundens val matchar dagens pizza skrivs extrapriset ut, annars skrivs ordinarie pris (95 kr) och pizzans namn.

**Exempel på körning:**
```text
=== PIZZERIA KODEN ===
Dagens pizza är hemlig... extrapris 69 kr!

1. Se pris
2. Visa menyn
3. Avsluta
Val: 2
Pizza 0: Margherita
Pizza 1: Hawaii
Pizza 2: Kebab
Pizza 3: Vesuvio

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 2
Kebab kostar 95 kr (ordinarie)

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 0
Margherita är dagens pizza! 69 kr.
```

**Facit:**
```python
import random

pizzor = ["Margherita", "Hawaii", "Kebab", "Vesuvio"]
dagens = random.randint(0, 3)

print("=== PIZZERIA KODEN ===")
print("Dagens pizza är hemlig... extrapris 69 kr!")

while True:
    print()
    print("1. Se pris")
    print("2. Visa menyn")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Vilken pizza (0-3)? "))
        if index == dagens:
            print(pizzor[index], "är dagens pizza! 69 kr.")
        else:
            print(pizzor[index], "kostar 95 kr (ordinarie)")
    elif val == "2":
        for i in range(4):
            print("Pizza", i, ":", pizzor[i])
    elif val == "3":
        print("Tack för ditt besök!")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 4: Håll koll på budgeten (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 3. Nu ska kunden ha en **budget på 200 kr** att handla för.

- Varje gång kunden ser priset på en pizza (val 1) ska priset dras från budgeten. Dagens pizza kostar 69 kr, övriga 95 kr.
- Efter varje priskoll ska programmet visa hur mycket som är kvar av budgeten.
- När budgeten når 0 kr eller mindre ska programmet meddela att pengarna är slut och stanna.
- Om kunden avslutar innan pengarna är slut (val 3) ska programmet visa hur mycket som blev kvar.

Allt annat i programmet ska fungera som i uppgift 3 (meny, dagens pizza, skattkarta).

**Exempel på körning:**
```text
=== PIZZERIA KODEN ===
Dagens pizza är hemlig... extrapris 69 kr!
Din budget: 200 kr

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 1
Hawaii kostar 95 kr (ordinarie)
Kvar av budgeten: 105 kr

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 0
Margherita är dagens pizza! 69 kr.
Kvar av budgeten: 36 kr

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 3
Vesuvio kostar 95 kr (ordinarie)
Pengarna är slut!
```

**Facit:**
```python
import random

pizzor = ["Margherita", "Hawaii", "Kebab", "Vesuvio"]
dagens = random.randint(0, 3)
budget = 200

print("=== PIZZERIA KODEN ===")
print("Dagens pizza är hemlig... extrapris 69 kr!")
print("Din budget:", budget, "kr")

while True:
    print()
    print("1. Se pris")
    print("2. Visa menyn")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        index = int(input("Vilken pizza (0-3)? "))
        if index == dagens:
            print(pizzor[index], "är dagens pizza! 69 kr.")
            budget = budget - 69
        else:
            print(pizzor[index], "kostar 95 kr (ordinarie)")
            budget = budget - 95
        if budget <= 0:
            print("Pengarna är slut!")
            break
        print("Kvar av budgeten:", budget, "kr")
    elif val == "2":
        for i in range(4):
            print("Pizza", i, ":", pizzor[i])
    elif val == "3":
        print("Tack för ditt besök! Du hade", budget, "kr kvar.")
        break
    else:
        print("Ogiltigt val.")
```

---

### Uppgift 5: Paketera pizzerian (4p)

**Uppgift:** Nu ska hela programmet paketeras så att det enkelt kan startas med olika kunder och olika budget.

- Programmet ska kunna startas genom att ange ett kundnamn och en budget (i kronor).
- När programmet startar ska det hälsa kunden välkommen och skriva ut hur stor budget hen har.
- Därefter ska programmet fungera precis som i uppgift 4, fast med den budget som angavs vid start istället för alltid 200 kr.

Utanför programmet ska du starta det med ett valfritt namn och valfri budget.

**Exempel på körning:**
```text
Välkommen Ali! Din budget är 150 kr.
Dagens pizza är hemlig... extrapris 69 kr!

1. Se pris
2. Visa menyn
3. Avsluta
Val: 1
Vilken pizza (0-3)? 0
Margherita är dagens pizza! 69 kr.
Kvar av budgeten: 81 kr

1. Se pris
2. Visa menyn
3. Avsluta
Val: 3
Tack för ditt besök! Du hade 81 kr kvar.
```

**Facit:**
```python
def pizzeria(kund, budget):
    import random

    pizzor = ["Margherita", "Hawaii", "Kebab", "Vesuvio"]
    dagens = random.randint(0, 3)

    print(f"Välkommen {kund}! Din budget är {budget} kr.")
    print("Dagens pizza är hemlig... extrapris 69 kr!")

    while True:
        print()
        print("1. Se pris")
        print("2. Visa menyn")
        print("3. Avsluta")
        val = input("Val: ")
        if val == "1":
            index = int(input("Vilken pizza (0-3)? "))
            if index == dagens:
                print(pizzor[index], "är dagens pizza! 69 kr.")
                budget = budget - 69
            else:
                print(pizzor[index], "kostar 95 kr (ordinarie)")
                budget = budget - 95
            if budget <= 0:
                print("Pengarna är slut!")
                break
            print("Kvar av budgeten:", budget, "kr")
        elif val == "2":
            for i in range(4):
                print("Pizza", i, ":", pizzor[i])
        elif val == "3":
            print(f"Tack för ditt besök! Du hade {budget} kr kvar.")
            break
        else:
            print("Ogiltigt val.")

pizzeria("Ali", 150)
```
