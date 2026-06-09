# Prov 6d: For-loopar och slump – C-nivå

Detta prov testar din förmåga att självständigt använda `for`-loopar, `range()`, `.append()` och `random`. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Analys och statistik.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Betygsräknare (7p)

**Uppgift:** Programmet ska ha en fördefinierad lista med betyg (bokstäver): `["A", "C", "A", "B", "C", "A", "B"]`. Använd en `for`-loop för att gå igenom listan och räkna:

* Hur många gånger betyget `"A"` förekommer
* Hur många gånger betyget `"B"` förekommer
* Hur många gånger betyget `"C"` förekommer

Efter loopen ska programmet skriva ut statistiken med en rubrik och f-strängar.

**Exempel på körning:**
```text
=== BETYGSSTATISTIK ===
A: 3
B: 2
C: 2
```

**Facit:**
```python
betyg = ["A", "C", "A", "B", "C", "A", "B"]
antal_a = 0
antal_b = 0
antal_c = 0

for b in betyg:
    if b == "A":
        antal_a = antal_a + 1
    elif b == "B":
        antal_b = antal_b + 1
    elif b == "C":
        antal_c = antal_c + 1

print("=== BETYGSSTATISTIK ===")
print(f"A: {antal_a}")
print(f"B: {antal_b}")
print(f"C: {antal_c}")
```

---

### Uppgift 2: Slumpgenerator (7p)

**Uppgift:** Programmet ska använda `random.randint(1, 100)` i en `for`-loop för att generera **fem slumpmässiga tal**. Varje tal ska läggas till i en lista med `.append()`. Efter loopen ska programmet skriva ut:

* Hela listan
* Det högsta värdet (använd `max()`)
* Det lägsta värdet (använd `min()`)
* Summan av alla tal (använd `sum()`)

Använd f-strängar för utskrifterna.

**Exempel på körning (resultatet varierar):**
```text
=== SLUMPGENERATOR ===
Tal: [42, 17, 89, 3, 55]
Högst: 89
Lägst: 3
Summa: 206
```

**Facit:**
```python
import random

tal = []
for i in range(5):
    tal.append(random.randint(1, 100))

print("=== SLUMPGENERATOR ===")
print(f"Tal: {tal}")
print(f"Högst: {max(tal)}")
print(f"Lägst: {min(tal)}")
print(f"Summa: {sum(tal)}")
```

---

### Uppgift 3: Filtrerad inköpslista (6p)

**Uppgift:** Programmet ska ha en fördefinierad lista med varor: `["Mjölk", "Bröd", "Äpplen", "Ost", "Smör", "Juice"]`. Använd en `for`-loop för att gå igenom listan. För varje vara ska programmet skriva ut varans namn och antal bokstäver varunamnet har (använd `len()`). Dessutom ska programmet **bara** skriva ut varor vars namn är **längre än 4 bokstäver**.

Använd f-strängar för utskrifterna.

**Exempel på körning:**
```text
=== VAROR MED LÅNGA NAMN ===
Mjölk (5 bokstäver)
Äpplen (6 bokstäver)
Juice (5 bokstäver)
```

**Facit:**
```python
varor = ["Mjölk", "Bröd", "Äpplen", "Ost", "Smör", "Juice"]

print("=== VAROR MED LÅNGA NAMN ===")
for vara in varor:
    if len(vara) > 4:
        print(f"{vara} ({len(vara)} bokstäver)")
```
