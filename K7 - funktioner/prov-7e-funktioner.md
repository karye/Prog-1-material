# Prov 7e: Funktioner – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med funktioner. Du får en problembeskrivning – resten är upp till dig.

**Tema:** System och hantering.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt funktionsstruktur och genomtänkt design.

---

### Uppgift 1: Plånboken (10p)

**Uppgift:** Bygg ett program med funktioner som hanterar en digital plånbok. Plånboken representeras av ett saldo (en variabel med ett startvärde, t.ex. 500 kr). Programmet ska ha följande funktioner:

* `visa_saldo(saldo)` – tar emot saldot och skriver ut hur mycket pengar som finns kvar.
* `kop(kostnad, saldo)` – tar emot en kostnad och saldot. Drar av kostnaden från saldot och skriver ut att köpet är gjort och hur mycket som är kvar. Om kostnaden överstiger saldot ska funktionen skriva ut att pengarna inte räcker och saldot ska vara oförändrat.
* `tjana(inkomst, saldo)` – tar emot en inkomst och saldot. Lägger till inkomsten till saldot och skriver ut nytt saldo.

Alla funktioner ska använda f-strängar. Skriv ett huvudprogram som anropar funktionerna i en sekvens som visar att plånboken fungerar. Du bestämmer själv ordning och argumentvärden.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Plånbok: 500 kr
Köper för 200 kr...
Kvar: 300 kr
Tjänar 150 kr...
Nytt saldo: 450 kr
Köper för 600 kr...
Pengarna räcker inte! Du har bara 450 kr.
```

**Facit:**
```python
def visa_saldo(saldo):
    print(f"Plånbok: {saldo} kr")

def kop(kostnad, saldo):
    if kostnad > saldo:
        print(f"Pengarna räcker inte! Du har bara {saldo} kr.")
        return saldo
    else:
        saldo = saldo - kostnad
        print(f"Köper för {kostnad} kr...")
        print(f"Kvar: {saldo} kr")
        return saldo

def tjana(inkomst, saldo):
    saldo = saldo + inkomst
    print(f"Tjänar {inkomst} kr...")
    print(f"Nytt saldo: {saldo} kr")
    return saldo

pengar = 500
visa_saldo(pengar)
pengar = kop(200, pengar)
pengar = tjana(150, pengar)
pengar = kop(600, pengar)
```

---

### Uppgift 2: Filmhanteraren (10p)

**Uppgift:** Bygg ett program med funktioner som hanterar en personlig filmlista. Programmet ska ha en lista med filmer som du själv fyller med minst tre titlar från början. Skapa följande funktioner:

* `visa_filmer(lista)` – tar emot filmlistan och skriver ut alla filmer med numrering (1, 2, 3...). Använd en `for`-loop och `range()` för numreringen.
* `lagg_till(lista, film)` – tar emot filmlistan och en ny filmtitel. Lägger till filmen med `.append()` och skriver ut en bekräftelse.
* `ta_bort(lista, index)` – tar emot filmlistan och ett index. Tar bort filmen på det indexet (använd `.pop(index)`) och skriver ut en bekräftelse med filmens titel.

Alla funktioner ska använda f-strängar. Skriv ett huvudprogram som demonstrerar alla funktioner i en tydlig ordning.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
=== FILMHANTERAREN ===
1. Lejonkungen
2. Inception
3. Frost

Lägger till: Dune
1. Lejonkungen
2. Inception
3. Frost
4. Dune

Tar bort film nr 2: Inception
1. Lejonkungen
2. Frost
3. Dune
```

**Facit:**
```python
def visa_filmer(lista):
    for i in range(len(lista)):
        print(f"{i + 1}. {lista[i]}")

def lagg_till(lista, film):
    lista.append(film)
    print(f"Lägger till: {film}")

def ta_bort(lista, index):
    borttagen = lista.pop(index - 1)
    print(f"Tar bort film nr {index}: {borttagen}")

filmer = ["Lejonkungen", "Inception", "Frost"]

print("=== FILMHANTERAREN ===")
visa_filmer(filmer)
print()

lagg_till(filmer, "Dune")
visa_filmer(filmer)
print()

ta_bort(filmer, 2)
visa_filmer(filmer)
```
