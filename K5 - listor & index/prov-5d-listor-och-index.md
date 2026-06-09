# Prov 5d: Listor och index – C-nivå

Detta prov testar din förmåga att självständigt arbeta med listor, index och blandade datatyper. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Uppslag och register.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Spellistan (7p)

**Uppgift:** Programmet ska innehålla **två parallella listor** med fyra låtar och deras artister:

* `latar = ["Blinding Lights", "Shape of You", "Dance Monkey", "Levitera"]`
* `artister = ["The Weeknd", "Ed Sheeran", "Tones and I", "Daniela Rathana"]`

Programmet ska skriva ut låtlistan och be användaren välja en låt med ett index (0–3). Därefter ska programmet skriva ut både låtens namn och artistens namn med hjälp av index. Använd f-strängar.

**Exempel på körning:**
```text
=== SPELLISTAN ===
Låtar: ['Blinding Lights', 'Shape of You', 'Dance Monkey', 'Levitera']
Välj låt (0-3): 2
Spelar: Dance Monkey av Tones and I
```

**Facit:**
```python
latar = ["Blinding Lights", "Shape of You", "Dance Monkey", "Levitera"]
artister = ["The Weeknd", "Ed Sheeran", "Tones and I", "Daniela Rathana"]

print("=== SPELLISTAN ===")
print("Låtar:", latar)
val = int(input("Välj låt (0-3): "))
print(f"Spelar: {latar[val]} av {artister[val]}")
```

---

### Uppgift 2: Menypriser (7p)

**Uppgift:** Programmet ska innehålla två parallella listor för en restaurangmeny:

* `ratter = ["Pasta", "Pizza", "Sallad", "Soppa"]`
* `priser = [120, 95, 85, 75]`

Programmet ska skriva ut meny och priser, och sedan låta användaren beställa **två rätter** genom att ange två index. Därefter ska programmet:

1. Skriva ut de två valda rätterna med deras priser.
2. Skriva ut den totala summan (addera priserna och skriv ut med f-sträng).

**Exempel på körning:**
```text
=== MENY ===
Rätter: ['Pasta', 'Pizza', 'Sallad', 'Soppa']
Priser: [120, 95, 85, 75]
Välj första rätten (0-3): 0
Välj andra rätten (0-3): 3
Du har valt: Pasta (120 kr) och Soppa (75 kr)
Totalt: 195 kr
```

**Facit:**
```python
ratter = ["Pasta", "Pizza", "Sallad", "Soppa"]
priser = [120, 95, 85, 75]

print("=== MENY ===")
print("Rätter:", ratter)
print("Priser:", priser)

val1 = int(input("Välj första rätten (0-3): "))
val2 = int(input("Välj andra rätten (0-3): "))

print(f"Du har valt: {ratter[val1]} ({priser[val1]} kr) och {ratter[val2]} ({priser[val2]} kr)")
print(f"Totalt: {priser[val1] + priser[val2]} kr")
```

---

### Uppgift 3: Personregistret (6p)

**Uppgift:** Programmet ska innehålla en lista med fyra personnamn:

* `personer = ["Ahmed", "Bea", "Clara", "David"]`

Programmet ska skriva ut listan och sedan låta användaren välja **första** eller **sista** personen. Användaren ska skriva `"f"` för första eller `"s"` för sista.

* Om `"f"` – skriv ut första namnet med index.
* Om `"s"` – skriv ut sista namnet. Använd `len()` för att dynamiskt hitta sista indexet (så att programmet fungerar även om listan ändras).
* Annars – skriv `"Ogiltigt val"`.

Använd f-strängar för utskrifterna.

**Exempel på körning:**
```text
=== PERSONREGISTER ===
Personer: ['Ahmed', 'Bea', 'Clara', 'David']
Visa första eller sista? (f/s): s
Sista personen: David
```

```text
Visa första eller sista? (f/s): f
Första personen: Ahmed
```

**Facit:**
```python
personer = ["Ahmed", "Bea", "Clara", "David"]

print("=== PERSONREGISTER ===")
print("Personer:", personer)

val = input("Visa första eller sista? (f/s): ")
if val == "f":
    print(f"Första personen: {personer[0]}")
elif val == "s":
    print(f"Sista personen: {personer[len(personer) - 1]}")
else:
    print("Ogiltigt val")
```
