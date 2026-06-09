# Prov 1e: Input och print – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med `print()`, `input()` och f-strängar. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Information och presentation.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både funktionalitet och presentation.

---

### Uppgift 1: Evenemangsaffisch (10p)

**Uppgift:** Bygg ett program som frågar användaren efter information om ett evenemang och sedan skriver ut en affisch. Programmet ska fråga efter **minst fyra** av följande saker (du väljer själva vilka):

* Evenemangets namn
* Datum
* Tid
* Plats
* Pris
* Arrangör
* Åldersgräns

Affischen som skrivs ut ska vara tydligt formaterad med:

* En rubrik i versaler (`.upper()`)
* En inramning eller skiljelinjer
* All information presenterad på ett överskådligt sätt
* En avslutande fras

Du bestämmer själv exakt layout, men den ska se genomtänkt ut och innehålla all information som matades in.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Evenemang: Höstlovsdisco
Datum: 3 november
Tid: 19:00-22:00
Plats: Fritidsgården
Åldersgräns: 13-16 år
========== HÖSTLOVSDISCO ==========
Datum: 3 november
Tid: 19:00-22:00
Plats: Fritidsgården
Åldersgräns: 13-16 år
-----------------------------------
Välkomna – vi ses där!
```

**Facit:**
```python
namn = input("Evenemang: ")
datum = input("Datum: ")
tid = input("Tid: ")
plats = input("Plats: ")
alder = input("Åldersgräns: ")

print(f"========== {namn.upper()} ==========")
print(f"Datum: {datum}")
print(f"Tid: {tid}")
print(f"Plats: {plats}")
print(f"Åldersgräns: {alder}")
print("-----------------------------------")
print("Välkomna – vi ses där!")
```

---

### Uppgift 2: Kvittogenerator (10p)

**Uppgift:** Bygg ett program som genererar ett kvitto för ett köp. Programmet ska fråga efter:

* Kundens namn
* Tre olika varor (namn och pris per vara)
* Betalningsmetod

Programmet ska sedan skriva ut ett kvitto som innehåller:

* Butikens namn som rubrik (hitta på ett själv)
* Kundens namn
* De tre varorna listade med pris
* En totalsumma (räkna själv ut den i förväg och skriv in som text – inga matematiska uträkningar krävs i koden)
* Betalningsmetod
* En tack-fras

Du bestämmer själv layout, ordning och utsmyckning. Kvittot ska vara lättläst och se professionellt ut.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Kundens namn: Ali
Vara 1: Limpa
Pris vara 1: 25
Vara 2: Mjölk
Pris vara 2: 15
Vara 3: Smör
Pris vara 3: 45
Betalningsmetod: Kort
========== TEKNIKBODEN ==========
Kund: Ali
-----------------------------------
Limpa ............. 25 kr
Mjölk ............. 15 kr
Smör .............. 45 kr
-----------------------------------
Totalt: 85 kr
Betalsätt: Kort
===================================
Tack för ditt köp, Ali!
```

**Facit:**
```python
kund = input("Kundens namn: ")

vara1 = input("Vara 1: ")
pris1 = input("Pris vara 1: ")

vara2 = input("Vara 2: ")
pris2 = input("Pris vara 2: ")

vara3 = input("Vara 3: ")
pris3 = input("Pris vara 3: ")

betalning = input("Betalningsmetod: ")

print("========== TEKNIKBODEN ==========")
print(f"Kund: {kund}")
print("-----------------------------------")
print(f"{vara1} ............. {pris1} kr")
print(f"{vara2} ............. {pris2} kr")
print(f"{vara3} .............. {pris3} kr")
print("-----------------------------------")
print("Totalt: 85 kr")
print(f"Betalsätt: {betalning}")
print("===================================")
print(f"Tack för ditt köp, {kund}!")
```
