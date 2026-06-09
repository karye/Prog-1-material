# Prov 2e: Villkor – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med `if`, `elif` och `else`. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Rekommendationssystem.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt logik och genomtänkt struktur.

---

### Uppgift 1: Restaurangguiden (10p)

**Uppgift:** Bygg ett program som rekommenderar en restaurang baserat på användarens preferenser. Programmet ska fråga efter:

* **Kostpreferens:** `"kött"`, `"vegetarisk"` eller `"fisk"`
* **Prisklass:** `"låg"`, `"mellan"` eller `"hög"`

Baserat på kombinationen ska programmet rekommendera en restaurang. Du ska ha **minst fem olika restauranger** att rekommendera – du bestämmer själv namnen och vilken kombination som ger vilket svar. Varje rekommendation ska skrivas ut med restaurangens namn och en kort beskrivning (hitta på själv).

Om användaren skriver ett ogiltigt alternativ ska programmet hantera det med ett tydligt felmeddelande.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Kostpreferens (kött/vegetarisk/fisk): vegetarisk
Prisklass (låg/mellan/hög): mellan
Vi rekommenderar: Grönboden – en mysig vegetarisk restaurang med schyssta priser.
```

```text
Kostpreferens (kött/vegetarisk/fisk): fisk
Prisklass (låg/mellan/hög): hög
Vi rekommenderar: Havskanten – fine dining med färsk fisk och havsutsikt.
```

**Facit:**
```python
kost = input("Kostpreferens (kött/vegetarisk/fisk): ")
pris = input("Prisklass (låg/mellan/hög): ")

if kost == "kött" and pris == "låg":
    print("Vi rekommenderar: Grillkiosken – burgare och korv till bra pris.")
elif kost == "kött" and pris == "mellan":
    print("Vi rekommenderar: Oxen & Grisen – husmanskost med hög kvalitet.")
elif kost == "kött" and pris == "hög":
    print("Vi rekommenderar: Köttmästaren – premiumkött från lokala gårdar.")
elif kost == "vegetarisk" and pris == "låg":
    print("Vi rekommenderar: Rotfruktsbaren – mättande veganskt till bra pris.")
elif kost == "vegetarisk" and pris == "mellan":
    print("Vi rekommenderar: Grönboden – en mysig vegetarisk restaurang med schyssta priser.")
elif kost == "vegetarisk" and pris == "hög":
    print("Vi rekommenderar: Vego Deluxe – prisbelönt vegetarisk fine dining.")
elif kost == "fisk" and pris == "låg":
    print("Vi rekommenderar: Fiskvagnen – dagens fångst vid hamnen.")
elif kost == "fisk" and pris == "mellan":
    print("Vi rekommenderar: Skaldjurskrogen – färska skaldjur i avslappnad miljö.")
elif kost == "fisk" and pris == "hög":
    print("Vi rekommenderar: Havskanten – fine dining med färsk fisk och havsutsikt.")
else:
    print("Ogiltigt val – försök igen med kött/vegetarisk/fisk och låg/mellan/hög.")
```

---

### Uppgift 2: Reseplaneraren (10p)

**Uppgift:** Bygg ett program som ger en reserekommendation baserat på användarens önskemål. Programmet ska fråga efter:

* **Årstid:** `"vinter"`, `"vår"`, `"sommar"` eller `"höst"`
* **Budget:** `"liten"`, `"mellan"` eller `"stor"`
* **Resesällskap:** `"ensam"`, `"partner"` eller `"familj"`

Baserat på kombinationen ska programmet rekommendera ett resmål med en motivering. Du ska ha **minst sex olika resmål** – fördela dem så att olika kombinationer ger olika svar. Varje svar ska innehålla resmålets namn och en kort motivering.

Om användaren skriver ett ogiltigt alternativ ska programmet ge ett hjälpsamt felmeddelande.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Årstid (vinter/vår/sommar/höst): sommar
Budget (liten/mellan/stor): liten
Sällskap (ensam/partner/familj): partner
Resmål: Gotland – cykelsemester i solen utan att det kostar skjortan!
```

```text
Årstid (vinter/vår/sommar/höst): vinter
Budget (liten/mellan/stor): stor
Sällskap (ensam/partner/familj): familj
Resmål: Lappland – norrsken, hundspann och lyxstuga för hela familjen.
```

**Facit:**
```python
arstid = input("Årstid (vinter/vår/sommar/höst): ")
budget = input("Budget (liten/mellan/stor): ")
sallskap = input("Sällskap (ensam/partner/familj): ")

giltig_arstid = arstid in ("vinter", "vår", "sommar", "höst")
giltig_budget = budget in ("liten", "mellan", "stor")
giltig_sallskap = sallskap in ("ensam", "partner", "familj")

if not (giltig_arstid and giltig_budget and giltig_sallskap):
    print("Ett eller flera val är ogiltiga. Försök igen.")
elif arstid == "sommar" and budget == "liten":
    print("Resmål: Gotland – cykelsemester i solen utan att det kostar skjortan!")
elif arstid == "sommar" and budget == "mellan":
    print("Resmål: Kroatien – kristallklart vatten och prisvärda boenden.")
elif arstid == "sommar" and budget == "stor":
    print("Resmål: Maldiverna – lyxresort med kritvita stränder.")
elif arstid == "vinter" and sallskap == "familj":
    print("Resmål: Åre – skidåkning och afterski för stora och små.")
elif arstid == "vinter" and sallskap == "partner":
    print("Resmål: Island – varma källor och norrsken för två.")
elif arstid == "vinter":
    print("Resmål: Lappland – norrsken, hundspann och lyxstuga.")
elif arstid == "vår" and budget == "stor":
    print("Resmål: Japan – körsbärsblomning och tempel i Kyoto.")
elif arstid == "vår":
    print("Resmål: Amsterdam – tulpaner, kanaler och cykling i vårsolen.")
elif budget == "stor":
    print("Resmål: Nya Zeeland – äventyr och fantastisk höstnatur.")
else:
    print("Resmål: Prag – vackert på hösten, prisvärt och nära.")
```
