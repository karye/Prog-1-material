# Träning inför prov 7c: funktioner

Här får du träna på samma moment som kommer på Prov 7c. Temat är **natur och utflykt**.

**Regler:**
* Använd korrekta namn på funktioner.
* Kom ihåg att definiera funktioner med `def`.
* Var noga med indentering (indrag).

---

### Uppgift 1: Dags för utflykt

**Uppgift:** Skapa en funktion som heter `packa_ryggsack()`. När funktionen körs ska den skriva ut texten `"Ryggsäcken är packad!"`. Funktionen ska inte ha några argument. Anropa funktionen en gång.

**Exempel på körning:**
```text
Ryggsäcken är packad!
```

**Facit:**
```python
def packa_ryggsack():
    print("Ryggsäcken är packad!")

packa_ryggsack()
```

---

### Uppgift 2: Fågelläten

**Uppgift:** Skapa en funktion som heter `kvitter()`. Funktionen ska skriva ut texten `"Kvitter!"`. Anropa funktionen **tre gånger i rad**.

**Exempel på körning:**
```text
Kvitter!
Kvitter!
Kvitter!
```

**Facit:**
```python
def kvitter():
    print("Kvitter!")

kvitter()
kvitter()
kvitter()
```

---

### Uppgift 3: Utflykt i tre steg

**Uppgift:** Skapa tre olika funktioner för en utflykt:

1. `ga_till_skogen()` som skriver ut `"Vi går mot skogen..."`
2. `plocka_bar()` som skriver ut `"Plockar blåbär och hallon!"`
3. `ga_hem()` som skriver ut `"Dags att gå hem, vilken fin dag!"`

Anropa alla tre i rätt ordning.

**Exempel på körning:**
```text
Vi går mot skogen...
Plockar blåbär och hallon!
Dags att gå hem, vilken fin dag!
```

**Facit:**
```python
def ga_till_skogen():
    print("Vi går mot skogen...")

def plocka_bar():
    print("Plockar blåbär och hallon!")

def ga_hem():
    print("Dags att gå hem, vilken fin dag!")

ga_till_skogen()
plocka_bar()
ga_hem()
```

---

### Uppgift 4: Hälsa vandrare

**Uppgift:** Skapa en funktion som heter `halsa_vandrare(namn)`. Funktionen ska ta emot **ett argument** och skriva ut en hälsning. Anropa funktionen med ett valfritt namn.

**Exempel på körning:**
```text
Välkommen på vandringen, Sofia!
```

**Facit:**
```python
def halsa_vandrare(namn):
    print("Välkommen på vandringen,", namn + "!")

halsa_vandrare("Sofia")
```

---

### Uppgift 5: Kaloriräknare

**Uppgift:** Skapa en funktion som heter `berakna_kalorier(km, kalorier_per_km)`. Funktionen ska ta emot **två argument**, multiplicera dem för att beräkna totalt antal förbrända kalorier och skriva ut resultatet med en **f-sträng**. Anropa funktionen med två valfria värden.

**Exempel på körning:**
```text
Du gick 8 km och förbrände 480 kalorier!
```

**Facit:**
```python
def berakna_kalorier(km, kalorier_per_km):
    totalt = km * kalorier_per_km
    print(f"Du gick {km} km och förbrände {totalt} kalorier!")

berakna_kalorier(8, 60)
```
