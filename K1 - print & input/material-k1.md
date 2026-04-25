# Prov: Input Och Print – 10 Nya Uppgifter (Med Färgade Exempelkörningar)

**Instruktion:** Varje uppgift har uppgiftstext, **exempelkörning** och **facit (för rättning)**.

**Viktigt formatkrav:**

* **Uppgift 1–4:** använd `print("Text", variabel)` (kommatecken), **ingen** f-string.
* **Uppgift 5–7:** **ingen** f-string (använd t.ex. `+`, `.upper()`, `.lower()`).
* **Uppgift 8–10:** f-strings är tillåtna.

**Färgnyckel för exempelkörningarna (ANSI):**

* Användarens inmatning visas i **cyan**: `\x1b[36m…\x1b[0m`
* Programmets utskrift är ofärgad (standard).

---

## Uppgift 1 – Skollunch (2 Input, 1 Print, Kommatecken)

**Uppgift:** Fråga efter **dagens rätt** och **tillbehör**. Skriv sedan ut en rad som presenterar lunchen.

**Exempel på körning:**

```
Skriv dagens rätt: \x1b[36mpasta\x1b[0m
Skriv ett tillbehör: \x1b[36msallad\x1b[0m
Dagens lunch är pasta med sallad.
```

**Facit:**

```python
ratt = input("Skriv dagens rätt: ")
till = input("Skriv ett tillbehör: ")
print("Dagens lunch är", ratt, "med", till + ".")
```

---

## Uppgift 2 – Klassrumsplats (2 Input, 1 Print, Kommatecken)

**Uppgift:** Fråga efter **elevens namn** och **plats i klassrummet** (t.ex. "rad 3, plats 2"). Skriv sedan ut en bekräftelse.

**Exempel på körning:**

```
Skriv elevens namn: \x1b[36mAmina\x1b[0m
Skriv plats i klassrummet: \x1b[36mrad 3, plats 2\x1b[0m
Plats för Amina är rad 3, plats 2.
```

**Facit:**

```python
namn = input("Skriv elevens namn: ")
plats = input("Skriv plats i klassrummet: ")
print("Plats för", namn, "är", plats + ".")
```

---

## Uppgift 3 – Lånekvitto (2 Input, 1 Print, Kommatecken)

**Uppgift:** Fråga efter **boktitel** och **återlämningsdag**. Skriv ut ett enkelt lånekvitto.

**Exempel på körning:**

```
Skriv boktitel: \x1b[36mNarnia\x1b[0m
Skriv återlämningsdag: \x1b[36mmåndag\x1b[0m
Du lånar Narnia till måndag.
```

**Facit:**

```python
titel = input("Skriv boktitel: ")
dag = input("Skriv återlämningsdag: ")
print("Du lånar", titel, "till", dag + ".")
```

---

## Uppgift 4 – Spellista (2 Input, 1 Print, Kommatecken)

**Uppgift:** Fråga efter **låt** och **artist**. Skriv en rad som visar vad som läggs till i spellistan.

**Exempel på körning:**

```
Skriv låt: \x1b[36mBad Habit\x1b[0m
Skriv artist: \x1b[36mSteve Lacy\x1b[0m
Nu lägger vi till Bad Habit av Steve Lacy i spellistan.
```

**Facit:**

```python
lat = input("Skriv låt: ")
artist = input("Skriv artist: ")
print("Nu lägger vi till", lat, "av", artist, "i spellistan.")
```

---

## Uppgift 5 – Receptkort (3 Input, 2 Print, Utan F-String)

**Uppgift:** Fråga efter **rättens namn**, **huvudingrediens** och **tillagningstid**. Skriv en rubrikrad och en sammanfattningsrad.

**Exempel på körning:**

```
Skriv rättens namn: \x1b[36mTomatsoppa\x1b[0m
Skriv huvudingrediens: \x1b[36mtomat\x1b[0m
Skriv tillagningstid: \x1b[36m20 minuter\x1b[0m
=== RECEPT ===
Tomatsoppa | Huvudingrediens: tomat | Tid: 20 minuter
```

**Facit:**

```python
namn = input("Skriv rättens namn: ")
ing = input("Skriv huvudingrediens: ")
tid = input("Skriv tillagningstid: ")
print("=== RECEPT ===")
print(namn + " | Huvudingrediens: " + ing + " | Tid: " + tid)
```

---

## Uppgift 6 – Klubbregistrering (3 Input, 3 Print, Utan F-String)

**Uppgift:** Fråga efter **klubbnamn**, **ditt namn** och **mötesdag**. Skriv ramrad, klubbnamn i versaler och en planrad.

**Exempel på körning:**

```
Skriv klubbnamn: \x1b[36mmakerspace\x1b[0m
Skriv ditt namn: \x1b[36mLeo\x1b[0m
Skriv mötesdag: \x1b[36mtorsdag\x1b[0m
#####################
MAKERSPACE
Leo, vi ses på torsdag!
```

**Facit:**

```python
klubb = input("Skriv klubbnamn: ")
ditt = input("Skriv ditt namn: ")
dag = input("Skriv mötesdag: ")
print("#####################")
print(klubb.upper())
print(ditt + ", vi ses på " + dag + "!")
```

---

## Uppgift 7 – Bibliotekspåminnelse (4 Input, 3 Print, Utan F-String)

**Uppgift:** Fråga efter **namn**, **boktitel**, **hämtplats** och **senaste hämtdag**. Skriv rubrikrad och två inforader (boktitel inom citat).

**Exempel på körning:**

```
Skriv ditt namn: \x1b[36mNoor\x1b[0m
Skriv boktitel: \x1b[36mMördarens apa\x1b[0m
Skriv hämtplats: \x1b[36mBiblioteket, hylla B\x1b[0m
Skriv senaste hämtdag: \x1b[36monsdag\x1b[0m
=== HÄMTNING ===
Noor, din bok "Mördarens apa" väntar.
Plats: Biblioteket, hylla B | Senast: onsdag
```

**Facit:**

```python
namn = input("Skriv ditt namn: ")
bok = input("Skriv boktitel: ")
plats = input("Skriv hämtplats: ")
dag = input("Skriv senaste hämtdag: ")
print("=== HÄMTNING ===")
print(namn + ", din bok \"" + bok + "\" väntar.")
print("Plats: " + plats + " | Senast: " + dag)
```

---

## Uppgift 8 – Teaterinbjudan (3 Input, 3 Print, F-Strings Tillåtna)

**Uppgift:** Fråga efter **pjäsens titel**, **sal** och **tid**. Skriv ramrad, rubrik och plats/tid.

**Exempel på körning:**

```
Skriv pjäsens titel: \x1b[36mRonja Rövardotter\x1b[0m
Skriv sal: \x1b[36mAulan\x1b[0m
Skriv tid: \x1b[36mlördag 16:00\x1b[0m
######################
TEATER: Ronja Rövardotter
Plats: Aulan | Tid: lördag 16:00
```

**Facit:**

```python
titel = input("Skriv pjäsens titel: ")
sal = input("Skriv sal: ")
tid = input("Skriv tid: ")
print("######################")
print(f"TEATER: {titel}")
print(f"Plats: {sal} | Tid: {tid}")
```

---

## Uppgift 9 – Speldesign-Pitch (4 Input, 3 Print, F-Strings)

**Uppgift:** Fråga efter **spelnamn**, **genre**, **hjältenamn** och **mål**. Skriv rubrik och två sammanfattningsrader.

**Exempel på körning:**

```
Skriv spelnamn: \x1b[36mSkuggspringaren\x1b[0m
Skriv genre: \x1b[36mplattform\x1b[0m
Skriv hjältenamn: \x1b[36mLio\x1b[0m
Skriv mål: \x1b[36mrädda staden\x1b[0m
=== PITCH ===
Skuggspringaren är ett plattform-spel.
Hjälten Lio ska rädda staden.
```

**Facit:**

```python
spel = input("Skriv spelnamn: ")
genre = input("Skriv genre: ")
hjalte = input("Skriv hjältenamn: ")
mal = input("Skriv mål: ")
print("=== PITCH ===")
print(f"{spel} är ett {genre}-spel.")
print(f"Hjälten {hjalte} ska {mal}.")
```

---

## Uppgift 10 – Science Fair (4 Input, 4 Print, F-Strings)

**Uppgift:** Fråga efter **experimentnamn**, **ämnesområde**, **labpartner** och **dag**. Skriv ramrad, rubrik, ämnesrad och tidsrad.

**Exempel på körning:**

```
Skriv experimentnamn: \x1b[36mLjudvågor i rör\x1b[0m
Skriv ämnesområde: \x1b[36mfysik\x1b[0m
Skriv labpartner: \x1b[36mSam\x1b[0m
Skriv dag: \x1b[36mtisdag\x1b[0m
========================
SCIENCE FAIR: Ljudvågor i rör
Ämne: fysik | Partner: Sam
Redovisning: tisdag
```

**Facit:**

```python
exp = input("Skriv experimentnamn: ")
amne = input("Skriv ämnesområde: ")
partner = input("Skriv labpartner: ")
dag = input("Skriv dag: ")
print("========================")
print(f"SCIENCE FAIR: {exp}")
print(f"Ämne: {amne} | Partner: {partner}")
print(f"Redovisning: {dag}")
```
