# Prov 5e: Listor och index – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med listor och index. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Databaser och simuleringar.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt indexhantering och genomtänkt struktur.

---

### Uppgift 1: Minidatabasen (10p)

**Uppgift:** Bygg ett program som fungerar som en enkel databas för ett ämne du väljer själv – till exempel filmer, böcker, spel, eller länder. Programmet ska:

* Innehålla **minst fyra poster**. Varje post består av en lista med **minst tre egenskaper** (blandat text och tal).
* Organisera posterna som du vill – exempelvis en stor lista med smålistor, eller parallella listor för varje egenskap.
* Skriva ut alla poster och låta användaren välja **en post** med ett index.
* När användaren valt en post ska programmet skriva ut **all information** om den posten, uppdelat på egna rader med förklarande text. Använd index för att plocka ut varje egenskap.
* Använd f-strängar för utskrifterna.

Du bestämmer själv layout och struktur.

**Exempel på körning (filmdatabas – ditt program kan se annorlunda ut):**
```text
=== FILMDATABASEN ===
Filmer: [['Lejonkungen', 1994, 5], ['Inception', 2010, 4], ['Frost', 2013, 3], ['Dune', 2021, 5]]
Välj film (0-3): 1
=== VALD FILM ===
Titel: Inception
År: 2010
Betyg: 4
```

**Facit:**
```python
filmer = [
    ["Lejonkungen", 1994, 5],
    ["Inception", 2010, 4],
    ["Frost", 2013, 3],
    ["Dune", 2021, 5]
]

print("=== FILMDATABASEN ===")
print("Filmer:", filmer)
val = int(input("Välj film (0-3): "))

film = filmer[val]
print("=== VALD FILM ===")
print(f"Titel: {film[0]}")
print(f"År: {film[1]}")
print(f"Betyg: {film[2]}")
```

---

### Uppgift 2: Kortspelet (10p)

**Uppgift:** Bygg ett program som drar två kort från en kortlek. Programmet ska:

* Innehålla en lista med **fyra färger**: `["Hjärter", "Ruter", "Klöver", "Spader"]`
* Innehålla en lista med **fyra valörer**: `["Ess", "Knekt", "Dam", "Kung"]`
* Användaren ska **välja en färg** med ett index (0–3) och **välja en valör** med ett index (0–3).
* Programmet ska sedan presentera det dragna kortet som en kombination av valör och färg, till exempel "Knekt i Klöver". Använd f-strängar.
* Därefter ska programmet dra ett **slumpmässigt kort** från samma kortlek (slumpat färgindex och valörindex) och skriva ut det. Använd `import random` och `random.randint(0, 3)`.
* Om de två korten är **identiska** (samma färg och samma valör) ska programmet skriva ut "Par!". Annars skrivs "Inget par.".
* Om användaren anger ett ogiltigt index ska programmet ge ett felmeddelande.

**Exempel på körning:**
```text
=== KORTSPELET ===
Färger: ['Hjärter', 'Ruter', 'Klöver', 'Spader']
Valörer: ['Ess', 'Knekt', 'Dam', 'Kung']
Välj färg (0-3): 1
Välj valör (0-3): 2
Ditt kort: Dam i Ruter
Draget kort: Knekt i Spader
Inget par.
```

```text
Välj färg (0-3): 0
Välj valör (0-3): 0
Ditt kort: Ess i Hjärter
Draget kort: Ess i Hjärter
Par!
```

**Facit:**
```python
import random

farger = ["Hjärter", "Ruter", "Klöver", "Spader"]
valorer = ["Ess", "Knekt", "Dam", "Kung"]

print("=== KORTSPELET ===")
print("Färger:", farger)
print("Valörer:", valorer)

farg_val = int(input("Välj färg (0-3): "))
valor_val = int(input("Välj valör (0-3): "))

if farg_val < 0 or farg_val > 3 or valor_val < 0 or valor_val > 3:
    print("Ogiltigt index! Välj 0-3.")
else:
    print(f"Ditt kort: {valorer[valor_val]} i {farger[farg_val]}")

    slump_farg = random.randint(0, 3)
    slump_valor = random.randint(0, 3)
    print(f"Draget kort: {valorer[slump_valor]} i {farger[slump_farg]}")

    if farg_val == slump_farg and valor_val == slump_valor:
        print("Par!")
    else:
        print("Inget par.")
```
