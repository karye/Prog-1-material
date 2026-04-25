# Träning inför prov 2b: villkor

Här får du träna på samma moment som kommer på Prov 2b. Temat är **sport**.

---

### Uppgift 1: Fotboll eller inte?

**Uppgift:** Fråga användaren vilken sport de gillar. Om svaret är `"fotboll"` ska programmet skriva `"Mål! En fotbollsfantast!"`. Annars ska det skriva `"En annan sport, också kul!"`.

**Exempel på körning 1:**
```text
Vilken sport gillar du? fotboll
Mål! En fotbollsfantast!
```

**Exempel på körning 2:**
```text
Vilken sport gillar du? tennis
En annan sport, också kul!
```

**Facit:**
```python
sport = input("Vilken sport gillar du? ")
if sport == "fotboll":
    print("Mål! En fotbollsfantast!")
else:
    print("En annan sport, också kul!")
```

---

### Uppgift 2: Vann eller förlorade?

**Uppgift:** Fråga användaren hur många poäng laget fick. Om poängen är 3 eller mer ska programmet skriva `"Laget vann!"`. Annars ska det skriva `"Laget förlorade."`.

**Exempel på körning 1:**
```text
Poäng: 4
Laget vann!
```

**Exempel på körning 2:**
```text
Poäng: 1
Laget förlorade.
```

**Facit:**
```python
poang = int(input("Poäng: "))
if poang >= 3:
    print("Laget vann!")
else:
    print("Laget förlorade.")
```

---

### Uppgift 3: Inomhus eller utomhus?

**Uppgift:** Fråga användaren vilken sport de spelar. Om det är `"simning"` skriv `"Inomhussport, bra!"`. Om det är `"fotboll"` skriv `"Utomhussport, kul!"`. Annars skriv `"En fin sport!"`.

**Exempel på körning 1:**
```text
Sport: simning
Inomhussport, bra!
```

**Exempel på körning 2:**
```text
Sport: fotboll
Utomhussport, kul!
```

**Exempel på körning 3:**
```text
Sport: tennis
En fin sport!
```

**Facit:**
```python
sport = input("Sport: ")
if sport == "simning":
    print("Inomhussport, bra!")
elif sport == "fotboll":
    print("Utomhussport, kul!")
else:
    print("En fin sport!")
```

---

### Uppgift 4: Träningsnivå

**Uppgift:** Fråga användaren hur många timmar i veckan de tränar. Skriv ut vilken nivå det är:
- Under 2 timmar: `"Nybörjare"`
- 2–4 timmar: `"Motionär"`
- 5–9 timmar: `"Aktiv"`
- 10 timmar eller mer: `"Elit"`

**Exempel på körning 1:**
```text
Träning (timmar/vecka): 1
Nybörjare
```

**Exempel på körning 2:**
```text
Träning (timmar/vecka): 3
Motionär
```

**Exempel på körning 3:**
```text
Träning (timmar/vecka): 7
Aktiv
```

**Exempel på körning 4:**
```text
Träning (timmar/vecka): 12
Elit
```

**Facit:**
```python
timmar = int(input("Träning (timmar/vecka): "))
if timmar < 2:
    print("Nybörjare")
elif timmar < 5:
    print("Motionär")
elif timmar < 10:
    print("Aktiv")
else:
    print("Elit")
```

---

### Uppgift 5: Träningsplan

**Uppgift:** Fråga användaren om sport och träningsdagar per vecka. Om sporten är `"löpning"`: kontrollera dagarna — om 5 eller fler skriv `"Imponerande, du är en löpare!"`, annars skriv `"Bra start, fortsätt så!"`. Om sporten inte är `"löpning"` ska programmet med en **f-sträng** skriva ut ett uppmuntrande meddelande för den sporten.

**Exempel på körning 1:**
```text
Sport: löpning
Dagar per vecka: 6
Imponerande, du är en löpare!
```

**Exempel på körning 2:**
```text
Sport: löpning
Dagar per vecka: 2
Bra start, fortsätt så!
```

**Exempel på körning 3:**
```text
Sport: cykling
Dagar per vecka: 3
Kör hårt med cykling!
```

**Facit:**
```python
sport = input("Sport: ")
dagar = int(input("Dagar per vecka: "))
if sport == "löpning":
    if dagar >= 5:
        print("Imponerande, du är en löpare!")
    else:
        print("Bra start, fortsätt så!")
else:
    print(f"Kör hårt med {sport}!")
```
