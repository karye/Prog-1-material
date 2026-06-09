# Prov 4d: Listor – C-nivå

Detta prov testar din förmåga att självständigt skapa och presentera listor med text och tal. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Samlingar och register.

**Regler:**
* Använd listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Använd f-strängar för utskrifter.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Lagbygge (7p)

**Uppgift:** Programmet ska fråga användaren efter tre spelarnamn och skapa en lista med namnen. Därefter ska programmet skriva ut laget i en snygg presentation med hjälp av f-strängar och variabler. Utskriften ska innehålla en rubrik, listan och antalet spelare.

**Exempel på körning:**
```text
Spelare 1: Zlatan
Spelare 2: Messi
Spelare 3: Ronaldo
=== DITT LAG ===
Spelare: ['Zlatan', 'Messi', 'Ronaldo']
Antal spelare: 3
```

**Facit:**
```python
s1 = input("Spelare 1: ")
s2 = input("Spelare 2: ")
s3 = input("Spelare 3: ")
lag = [s1, s2, s3]
print("=== DITT LAG ===")
print(f"Spelare: {lag}")
print(f"Antal spelare: 3")
```

---

### Uppgift 2: Beställningslista (7p)

**Uppgift:** Programmet ska fråga användaren efter tre varor och deras priser. Skapa **två listor**: en med varunamnen och en med priserna. Skriv sedan ut varorna i en lista och priserna i en lista, med tydlig rubrik och f-strängar. Priserna ska matas in som heltal.

**Exempel på körning:**
```text
Vara 1: Bröd
Pris 1: 25
Vara 2: Mjölk
Pris 2: 15
Vara 3: Ost
Pris 3: 45
=== BESTÄLLNING ===
Varor: ['Bröd', 'Mjölk', 'Ost']
Priser: [25, 15, 45]
```

**Facit:**
```python
v1 = input("Vara 1: ")
p1 = int(input("Pris 1: "))
v2 = input("Vara 2: ")
p2 = int(input("Pris 2: "))
v3 = input("Vara 3: ")
p3 = int(input("Pris 3: "))

varor = [v1, v2, v3]
priser = [p1, p2, p3]

print("=== BESTÄLLNING ===")
print(f"Varor: {varor}")
print(f"Priser: {priser}")
```

---

### Uppgift 3: Spelrecension (6p)

**Uppgift:** Programmet ska fråga användaren efter information om ett spel och samla allt i **en enda lista**. Informationen som ska samlas in är:

* Spelets namn (text)
* Betyg 1–10 (tal)
* Speltid i timmar (tal)
* Favoritkaraktär (text)

Därefter ska programmet skriva ut en recension med rubrik och listans innehåll, formaterat med f-strängar.

**Exempel på körning:**
```text
Spelets namn: Minecraft
Betyg (1-10): 10
Speltid i timmar: 500
Favoritkaraktär: Steve
=== SPELRECENSION ===
Recension: ['Minecraft', 10, 500, 'Steve']
```

**Facit:**
```python
namn = input("Spelets namn: ")
betyg = int(input("Betyg (1-10): "))
tid = int(input("Speltid i timmar: "))
karaktar = input("Favoritkaraktär: ")

recension = [namn, betyg, tid, karaktar]

print("=== SPELRECENSION ===")
print(f"Recension: {recension}")
```
