# Prov 6e: For-loopar och slump – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med `for`-loopar och `random`. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Simuleringar och analys.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt loop-logik och genomtänkt struktur.

---

### Uppgift 1: Tärningssimulatorn (10p)

**Uppgift:** Bygg ett program som simulerar tärningskast och sammanställer resultat. Programmet ska:

* Fråga användaren hur många tärningskast som ska simuleras.
* Använda en `for`-loop med `range()` för att slå en tärning (`random.randint(1, 6)`) så många gånger som användaren angav.
* Hålla reda på **hur många gånger varje siffra** (1–6) förekommer. Du behöver sex räknare.
* Efter loopen ska programmet skriva ut en statistikrapport med rubrik, antal kast, och hur många gånger varje siffra kom upp. Använd f-strängar.
* Programmet ska också skriva ut vilken siffra som var **vanligast**.

Du bestämmer själv layout och variabelnamn.

**Exempel på körning (resultatet varierar):**
```text
Hur många kast? 100
=== TÄRNINGSSTATISTIK (100 kast) ===
Etta: 14
Tvåa: 19
Trea: 15
Fyra: 18
Femma: 16
Sexa: 18
Vanligast: Tvåa (19 gånger)
```

**Facit:**
```python
import random

kast = int(input("Hur många kast? "))

ettor = 0
tvaor = 0
treor = 0
fyror = 0
femmor = 0
sexor = 0

for i in range(kast):
    tarning = random.randint(1, 6)
    if tarning == 1:
        ettor = ettor + 1
    elif tarning == 2:
        tvaor = tvaor + 1
    elif tarning == 3:
        treor = treor + 1
    elif tarning == 4:
        fyror = fyror + 1
    elif tarning == 5:
        femmor = femmor + 1
    else:
        sexor = sexor + 1

print(f"=== TÄRNINGSSTATISTIK ({kast} kast) ===")
print(f"Etta: {ettor}")
print(f"Tvåa: {tvaor}")
print(f"Trea: {treor}")
print(f"Fyra: {fyror}")
print(f"Femma: {femmor}")
print(f"Sexa: {sexor}")

# Hitta vanligast
vanligast_siffra = 1
vanligast_antal = ettor
if tvaor > vanligast_antal:
    vanligast_siffra = 2
    vanligast_antal = tvaor
if treor > vanligast_antal:
    vanligast_siffra = 3
    vanligast_antal = treor
if fyror > vanligast_antal:
    vanligast_siffra = 4
    vanligast_antal = fyror
if femmor > vanligast_antal:
    vanligast_siffra = 5
    vanligast_antal = femmor
if sexor > vanligast_antal:
    vanligast_siffra = 6
    vanligast_antal = sexor

siffror_namn = ["Etta", "Tvåa", "Trea", "Fyra", "Femma", "Sexa"]
print(f"Vanligast: {siffror_namn[vanligast_siffra - 1]} ({vanligast_antal} gånger)")
```

---

### Uppgift 2: Ordräknaren (10p)

**Uppgift:** Bygg ett program som analyserar en lista med ord. Programmet ska:

* Ha en fördefinierad lista med **minst åtta ord** som du själv hittar på. Blanda korta och långa ord.
* Använda en `for`-loop för att gå igenom listan och kategorisera varje ord:
  - **Korta ord:** färre än 5 bokstäver
  - **Långa ord:** 5 bokstäver eller fler
* Lägg korta ord i en lista och långa ord i en annan lista med `.append()`.
* Efter loopen ska programmet skriva ut:
  - Alla ord
  - Antal korta ord och vilka de är
  - Antal långa ord och vilka de är
  - Medellängden på alla ord (totalt antal bokstäver delat med antal ord)
* Använd f-strängar och snygg formatering. Du bestämmer själv layout.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== ORDRÄKNAREN ===
Alla ord: ['kod', 'programmering', 'hej', 'dator', 'python', 'AI', 'variabel', 'loop']
Korta ord (3 st): ['kod', 'hej', 'AI']
Långa ord (5 st): ['programmering', 'dator', 'python', 'variabel', 'loop']
Medellängd: 5.1 bokstäver
```

**Facit:**
```python
ordlista = ["kod", "programmering", "hej", "dator", "python", "AI", "variabel", "loop"]

korta = []
langa = []
total_langd = 0

for ordet in ordlista:
    total_langd = total_langd + len(ordet)
    if len(ordet) < 5:
        korta.append(ordet)
    else:
        langa.append(ordet)

medel = total_langd / len(ordlista)

print("=== ORDRÄKNAREN ===")
print(f"Alla ord: {ordlista}")
print(f"Korta ord ({len(korta)} st): {korta}")
print(f"Långa ord ({len(langa)} st): {langa}")
print(f"Medellängd: {medel} bokstäver")
```
