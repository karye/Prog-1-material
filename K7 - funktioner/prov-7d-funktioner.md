# Prov 7d: Funktioner – C-nivå

Detta prov testar din förmåga att självständigt skapa funktioner med argument och villkorslogik. Du får veta **vad** funktionerna ska göra – men **hur** du löser det är upp till dig.

**Tema:** Beräkningar och beslutsstöd.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Betygsfunktion (7p)

**Uppgift:** Skapa en funktion som heter `betyg(poang)` och tar emot ett heltal (0–100). Funktionen ska **inte** returnera något, utan skriva ut betyget baserat på poängen:

* 90–100: `"Betyg: A"`
* 75–89: `"Betyg: B"`
* 60–74: `"Betyg: C"`
* 0–59: `"Betyg: F"`

Efter funktionen ska du anropa den med **tre olika poäng** för att testa att den fungerar korrekt. Använd f-strängar i utskriften.

**Exempel på körning:**
```text
Betyg: B
Betyg: A
Betyg: F
```

**Facit:**
```python
def betyg(poang):
    if poang >= 90:
        print("Betyg: A")
    elif poang >= 75:
        print("Betyg: B")
    elif poang >= 60:
        print("Betyg: C")
    else:
        print("Betyg: F")

betyg(82)
betyg(95)
betyg(45)
```

---

### Uppgift 2: Rabattberäknare (7p)

**Uppgift:** Skapa en funktion som heter `rabatt(pris, medlem)`. Funktionen tar emot ett pris (heltal) och en medlemsstatus (text, `"ja"` eller `"nej"`). Funktionen ska räkna ut slutpriset enligt följande regler:

* Om medlem (`"ja"`) och priset överstiger 500 kr: **20 % rabatt**.
* Om medlem (`"ja"`) och priset är 500 kr eller lägre: **10 % rabatt**.
* Om inte medlem (`"nej"`): **ingen rabatt**.

Funktionen ska skriva ut slutpriset med en f-sträng (inga decimaler krävs). Anropa funktionen med **tre olika kombinationer** för att testa.

**Exempel på körning:**
```text
Slutpris: 640 kr
Slutpris: 270 kr
Slutpris: 400 kr
```

**Facit:**
```python
def rabatt(pris, medlem):
    if medlem == "ja" and pris > 500:
        slutpris = pris * 0.8
    elif medlem == "ja":
        slutpris = pris * 0.9
    else:
        slutpris = pris
    print(f"Slutpris: {int(slutpris)} kr")

rabatt(800, "ja")
rabatt(300, "ja")
rabatt(400, "nej")
```

---

### Uppgift 3: Spelmeny (6p)

**Uppgift:** Skapa tre funktioner för ett spel:

* `visa_status(spelare, liv)` – tar emot ett spelarnamn och antal liv, skriver ut båda med f-sträng.
* `attackera(spelare, skada)` – tar emot spelarnamn och skada, skriver ut hur mycket skada spelaren gör.
* `game_over()` – tar inga argument, skriver ut `"Game Over!"`.

Skriv sedan ett huvudprogram som anropar funktionerna i logisk ordning för att simulera en spelrunda. Anropa `visa_status`, `attackera` och avsluta med `game_over`. Välj själv lämpliga argumentvärden.

**Exempel på körning:**
```text
Spelare: Link | Liv: 3
Link gör 15 i skada!
Game Over!
```

**Facit:**
```python
def visa_status(spelare, liv):
    print(f"Spelare: {spelare} | Liv: {liv}")

def attackera(spelare, skada):
    print(f"{spelare} gör {skada} i skada!")

def game_over():
    print("Game Over!")

visa_status("Link", 3)
attackera("Link", 15)
game_over()
```
